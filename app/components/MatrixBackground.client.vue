
<script setup>
import { onMounted, onBeforeUnmount, ref } from 'vue'

const canvas = ref(null)

let ctx = null
let animationFrame = null
let width = 0
let height = 0
let drops = []
let columns = 0
let frame = 0

const cellWidth = 11
const cellHeight = 11

const characters =
  '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZアイウエオカキクケコサシスセソタチツテトナニヌネノ'

function randomCharacter() {
  return characters[Math.floor(Math.random() * characters.length)]
}

function createDrop(y = -Math.random() * height) {
  const length = Math.floor(5 + Math.random() * 13)

  return {
    y,
    speed: 0.16 + Math.random() * 0.3,
    length,
    active: Math.random() > 0.2,
    brightness: 0.45 + Math.random() * 0.45,
    chars: Array.from({ length }, randomCharacter),
  }
}

function resizeCanvas() {
  if (!canvas.value) return

  // Lower resolution creates the pixelated appearance.
  width = Math.ceil(window.innerWidth * 0.5)
  height = Math.ceil(window.innerHeight * 0.5)

  canvas.value.width = width
  canvas.value.height = height

  ctx = canvas.value.getContext('2d', { alpha: false })

  if (!ctx) return

  ctx.font = '9px VT323, monospace'
  ctx.textBaseline = 'top'

  columns = Math.ceil(width / cellWidth)

  drops = Array.from({ length: columns }, () =>
    createDrop()
  )

  ctx.fillStyle = '#010402'
  ctx.fillRect(0, 0, width, height)
}

function drawRain() {
  if (!ctx) return

  frame++

  // Fade previous frames to create character trails.
  ctx.fillStyle = 'rgba(1, 4, 2, 0.16)'
  ctx.fillRect(0, 0, width, height)

  drops.forEach((drop, column) => {
    if (!drop.active) return

    const x = column * cellWidth

    // Occasionally change characters for a digital flicker.
    if (frame % 3 === 0 && Math.random() > 0.75) {
      const index = Math.floor(Math.random() * drop.length)
      drop.chars[index] = randomCharacter()
    }

    // Draw the falling character trail.
    for (let i = 0; i < drop.length; i++) {
      const y = Math.floor(drop.y - i * cellHeight)

      if (y < 0 || y > height) continue

      if (i === 0) {
        // Bright leading character.
        ctx.fillStyle = '#baffd0'
      } else {
        const opacity =
          Math.pow(1 - i / drop.length, 1.5) *
          drop.brightness

        ctx.fillStyle = `rgba(0, 220, 90, ${opacity})`
      }

      ctx.fillText(drop.chars[i], x, y)
    }

    drop.y += drop.speed

    // Reset the stream after it leaves the screen.
    if (drop.y - drop.length * cellHeight > height) {
      drops[column] = createDrop(-Math.random() * height * 0.5)
    }
  })

  animationFrame = requestAnimationFrame(drawRain)
}

onMounted(() => {
  if (!canvas.value) return

  resizeCanvas()

  window.addEventListener('resize', resizeCanvas)

  animationFrame = requestAnimationFrame(drawRain)
})

onBeforeUnmount(() => {
  cancelAnimationFrame(animationFrame)
  window.removeEventListener('resize', resizeCanvas)

  drops = []
  ctx = null
})
</script>

<template>
  <div class="matrix-background" aria-hidden="true">
    <canvas ref="canvas" class="matrix-canvas" />

    <div class="crt-overlay" />
    <div class="vignette-overlay" />
  </div>
</template>

<style scoped>
.matrix-background {
  position: fixed;
  inset: 0;
  z-index: -10;
  overflow: hidden;
  pointer-events: none;
  background: #010402;
}

.matrix-canvas {
  display: block;
  width: 100%;
  height: 100%;
  image-rendering: pixelated;
  opacity: 0.78;
}

.crt-overlay {
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    to bottom,
    transparent 0px,
    transparent 3px,
    rgba(0, 0, 0, 0.18) 4px
  );
  opacity: 0.55;
}

.vignette-overlay {
  position: absolute;
  inset: 0;
  background: radial-gradient(
    ellipse at center,
    transparent 35%,
    rgba(0, 0, 0, 0.45) 100%
  );
}
</style>
