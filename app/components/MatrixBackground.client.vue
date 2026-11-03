
<script setup>
import { onMounted, onBeforeUnmount, nextTick, ref } from 'vue'
import * as THREE from 'three'

const background = ref(null)
let vantaEffect = null

onMounted(async () => {
  await nextTick()
  if (!background.value) return

  try {
    const vantaModule = await import('vanta/dist/vanta.net.min')

const NET =
  typeof vantaModule.default === 'function'
    ? vantaModule.default
    : vantaModule.default?.default

if (typeof NET !== 'function') {
  throw new TypeError('Vanta.NET export is not a function')
}
    vantaEffect = NET({
      el: background.value,
      THREE,
      mouseControls: true,
      touchControls: true,
      gyroControls: false,
      minHeight: 200,
      minWidth: 200,
      scale: 1,
      scaleMobile: 1,
      color: 0x00ff41,
      backgroundColor: 0x000000,
      points: 8,
      maxDistance: 12,
      spacing: 24,
    })
  } catch (error) {
    console.error('Vanta.NET initialization failed:', error)
  }
})

onBeforeUnmount(() => {
  if (vantaEffect) {
    vantaEffect.destroy()
    vantaEffect = null
  }
})
</script>

<template>
  <div
    ref="background"
    class="pointer-events-none fixed inset-0 -z-10"
    aria-hidden="true"
  ></div>
</template>
