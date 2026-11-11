<script setup>
useHead({
  title: 'About | Lawrence Dave Corral'
})

useSeoMeta({
  description: 'Explore the portfolio of Lawrence Dave Corral. Learn about his background, interests, and journey in Information Technology.'
})

</script>

<template>
  <section class="relative isolate min-h-screen overflow-hidden px-4 pt-4 pb-12">
    <MatrixBackground />

    <!-- Background Image -->
    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/about/about-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

    <!-- Content of the page--> 
    <div class="relative z-10 mx-auto flex max-w-4xl flex-col gap-8">
      

  <header class="mx-auto w-full max-w-3xl">
    <div class="group flex flex-col items-center gap-5 border border-green-700/50 bg-black/80 p-6 text-center shadow-[0_0_25px_rgba(0,255,100,0.08)] transition-all duration-500 hover:-translate-y-1 hover:border-green-400/70 hover:shadow-[0_0_35px_rgba(0,255,100,0.18)] motion-reduce:transition-none sm:flex-row sm:text-left md:p-8">

    <!-- Portrait -->
    <div class="relative shrink-0">
      <div
        class="absolute -inset-2 rounded-full border border-green-500/40"
        aria-hidden="true"
      ></div>

      <img
        src="/images/home/home-lawrence.jpg"
        alt="Portrait of Lawrence Dave Corral"
        class="relative h-28 w-28 rounded-full border-2 border-green-500 object-cover shadow-[0_0_18px_rgba(0,255,100,0.25)] transition-transform duration-500 group-hover:scale-105 motion-reduce:transition-none md:h-32 md:w-32"
      />
    </div>

    <!--Information -->
    <div class="min-w-0">
      <p class="mb-2 font-jetbrains text-xs tracking-[0.2em] text-green-500">
        ABOUT / PROFILE
      </p>

    <h1 class="matrix-glow font-matrix text-3xl text-white md:text-4xl">
      ABOUT ME
    </h1>

      <h2 class="mt-2 font-cyber text-sm tracking-wide text-green-400 md:text-base">
        LAWRENCE DAVE CORRAL
      </h2>

      <p class="mt-2 font-jetbrains text-xs leading-6 text-gray-400">
        IT STUDENT // ASPIRING FRONTEND WEB DEVELOPER
      </p>
    </div>

  </div>
</header>
    </div>
  </section>
</template>