<script setup>
</script>

<template>
  <section
    class="relative isolate flex min-h-[calc(100vh-5rem)] flex-col items-center justify-center gap-6 overflow-hidden px-4 py-8 text-center"
  >

    <MatrixBackground/>

    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/home/home-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

<div class="relative z-10 flex -translate-y-23 flex-col items-center gap-4">
  
  <div class="h-40 w-40 rounded-full border-2 border-green-500 p-1">
    <img
      src="/images/home/home-lawrence.jpg"
      alt="Lawrence Dave S. Corral"
      class="h-full w-full rounded-full object-cover"
    />
  </div>

  <div class="space-y-3">
    <h1 class="font-matrix matrix-glow text-4xl text-white">
      LAWRENCE DAVE CORRAL
    </h1>

    <p class="font-jetbrains text-sm text-green-400">
      Aspiring Frontend Web Developer and Game Developer
    </p>

    <a
      href="https://github.com/LawrenceCorral"
      target="_blank"
      rel="noopener noreferrer"
      class="flex justify-center transition-transform duration-200 hover:scale-110"
    >
      <img
        src="/images/home/home-github-invertocat-white.svg"
        alt=""
        class="h-8 w-8"
      />
    </a>
  </div>
</div>
  </section>
</template>
