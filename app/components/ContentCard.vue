<script setup>
defineProps({
  title: String
})
</script>

<template>
  <article class="border border-green-800/60 bg-black/70 shadow-lg">
    <!-- Card Header -->
    <div class="flex items-center gap-2 border-b border-green-900/60 px-5 py-4">
      <span class="h-3 w-3 rounded-full bg-red-500"></span>
      <span class="h-3 w-3 rounded-full bg-yellow-500"></span>
      <span class="h-3 w-3 rounded-full bg-green-500"></span>

      <p class="ml-3 font-jetbrains text-sm text-green-400">
        {{ title }}
      </p>
    </div>

    <!-- Card Content -->
    <div class="p-6 md:p-8">
      <slot />
    </div>
  </article>
</template>