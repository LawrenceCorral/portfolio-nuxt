
<script setup>

useHead({
  title: 'Page Not Found | Lawrence Dave Corral'
})
</script>

<template>
  <section
    class="relative isolate flex min-h-screen items-center justify-center overflow-hidden px-4 py-12 text-center"
  >
    <MatrixBackground />

    <!-- Background Image -->
    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/home/home-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

    <!-- Error Content -->
    <div class="relative z-10 flex flex-col items-center gap-6">

      <p class="font-jetbrains text-sm uppercase tracking-widest text-green-400">
        SYSTEM ERROR
      </p>

      <h1 class="font-matrix matrix-glow text-8xl text-white md:text-9xl">
        404
      </h1>

      <h2 class="font-matrix text-3xl text-green-400 md:text-4xl">
        PAGE NOT FOUND
      </h2>

      <p class="font-jetbrains text-sm leading-7 text-gray-400">
        The page you are looking for cannot be found.
      </p>

      <!-- Return Home Button -->
      <NuxtLink
        to="/"
        class="mt-3 border border-green-700/60 px-6 py-3 font-jetbrains text-sm text-green-400 transition-all duration-200 hover:border-green-400 hover:bg-green-500/10"
      >
        RETURN TO HOME
      </NuxtLink>

    </div>
  </section>
</template>
