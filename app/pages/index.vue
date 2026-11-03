<script setup>
useSeoMeta({
  title: 'Home | Lawrence Dave Corral',
  description: 'This is my personal portfolio of Lawrence Dave Corral, an aspiring frontend web developer and game developer'
})
</script>

<template>
  <section
    class="relative isolate flex min-h-[calc(100vh-5rem)] items-start justify-center overflow-hidden px-4 pt-8 pb-12"
  >
    <!-- Matrix Background -->
    <MatrixBackground />

    <!-- Background Image -->
    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/home/home-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

    <!-- Centered Hero Content -->
    <div
      class="relative z-10 flex w-full -translate-y-8 flex-col items-center gap-6 text-center"
    >
      <!-- My Portrait -->
      <div
        class="relative h-56 w-56 overflow-hidden rounded-full border-2 border-green-500 p-1 shadow-[0_0_25px_rgba(0,255,65,0.2)] md:h-64 md:w-64"
      >
        <img
          src="/images/home/home-lawrence.jpg"
          alt="Lawrence Dave S. Corral"
          class="h-full w-full rounded-full object-cover"
        />

        <!-- Scanlines -->
        <div
          class="bg-scanlines pointer-events-none absolute inset-0 rounded-full"
          aria-hidden="true"
        ></div>

        <!-- Moving Scanline -->
        <div
          class="animate-scan pointer-events-none absolute left-0 h-1 w-full bg-green-400/40 shadow-[0_0_12px_rgba(0,255,65,0.8)]"
          aria-hidden="true"
        ></div>
      </div>

      <!-- Introduction of my Port-->
      <div class="flex flex-col items-center gap-4">

        <!-- Welcome Text -->
        <p
          class="font-jetbrains text-sm uppercase tracking-[0.3em] text-green-500"
        >
          Welcome to my portfolio!!!
        </p>

        <!-- Name -->
        <h1
          class="font-matrix matrix-glow text-5xl leading-none text-white md:text-6xl"
        >
          LAWRENCE DAVE CORRAL
        </h1>

        <!-- Description -->
        <p
          class="font-jetbrains text-sm leading-7 text-green-400 md:text-base"
        >
          Aspiring Frontend Web Developer and Game Developer
        </p>

        <!-- GitHub Profile -->
        <a
          href="https://github.com/LawrenceCorral"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="Visit my GitHub profile"
          class="mt-2 inline-flex items-center gap-3 border border-green-700/60 px-4 py-2 font-jetbrains text-sm text-white transition-all duration-200 hover:border-green-400 hover:bg-green-500/10 hover:text-green-400"
        >
          <img
            src="/images/home/home-github-invertocat-white.svg"
            alt=""
            class="h-5 w-5"
          />
          GITHUB PROFILE
        </a>

      </div>
    </div>
  </section>
</template>