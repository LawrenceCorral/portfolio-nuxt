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
      <header class="text-center">
        <h1 class="font-matrix matrix-glow text-5xl text-white md:text-6xl">
          ABOUT ME
        </h1>
        <p class="mt-3 font-jetbrains text-sm text-green-400">
          Get to know me
        </p>
      </header>

<!-- About Content -->
<ContentCard title="About Me">
  <div class="space-y-5 font-jetbrains text-sm leading-8 text-gray-300">
    <p>
      Hello! I am Lawrence Dave S. Corral, currently studying at St. Dominic
      College of Asia. My interest in technology started with my passion
      for playing video games, which made me curious about how these
      digital worlds and interfaces are created.
    </p>

    <p>
      This hobby led me to pursue a degree in Information Technology to
      understand the logic behind the screens. I am a quiet person, but I
      am dedicated to improving my communication and teamwork—essential
      skills in the IT field.
    </p>

    <p>
      My professional aspiration is to become a Frontend Web Developer.
      I want to master modern web technologies to create seamless digital
      experiences that are as interactive and smooth as the games I enjoy.
    </p>
  </div>
</ContentCard>
    </div>
  </section>
</template>