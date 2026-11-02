
<script setup>
import { onMounted, onBeforeUnmount, ref } from 'vue'
import * as THREE from 'three'
import NET from 'vanta/dist/vanta.net.min'

const background = ref(null)
let vantaEffect = null

onMounted(() => {
  if (!background.value) return

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
    points: 10,
    maxDistance: 20,
    spacing: 18,
  })
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
  />
</template>
