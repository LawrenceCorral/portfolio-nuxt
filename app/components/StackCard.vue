<script setup>
defineProps({
  name: String,
  image: String
})
</script>

<template>
  <article
    class="flex flex-col items-center gap-4 border border-green-800/60 bg-black/70 p-6 transition hover:-translate-y-1 hover:border-green-400"
  >
    <img
      :src="image"
      :alt="name"
      class="h-20 w-20 object-contain"
      loading="lazy"
    />

    <h3 class="text-center font-jetbrains text-sm text-white">
      {{ name }}
    </h3>
  </article>
</template>