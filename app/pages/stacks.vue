<script setup>
useHead({
  title: 'Stacks | Lawrence Dave Corral'
})

useSeoMeta({
  description: 'Explore the programming languages and development tools used by Lawrence Dave Corral, featuring Vue, Nuxt, and JavaScript.'
})

const languages = [
  { name: 'Java', image: '/images/stacks/stacks-java.png' },
  { name: 'JavaScript', image: '/images/stacks/stacks-javascript.png' },
  { name: 'HTML', image: '/images/stacks/stacks-css.png' }
]

const tools = [
  { name: 'Visual Studio Code', image: '/images/stacks/stacks-vscode.png' },
  { name: 'SQL', image: '/images/stacks/stacks-ssms.png' },
  { name: 'GitHub', image: '/images/stacks/stacks-githublight.png' },
  { name: 'Android Studio', image: '/images/stacks/stacks-android.png' },
  { name: 'PostgreSQL', image: '/images/stacks/stacks-postgre.png' },
  { name: 'Git', image: '/images/stacks/stacks-gitt.png' },
  { name: 'MongoDB', image: '/images/stacks/stacks-mongo.png' }
]
</script>

<template>
  <section class="relative isolate min-h-screen overflow-hidden px-4 pt-4 pb-12">
    <MatrixBackground />

    <!-- Background Image -->
    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/stacks/stacks-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

    <div class="relative z-10 mx-auto flex max-w-5xl flex-col gap-12">
      <!-- Heading -->
      <header class="text-center">
        <h1 class="font-matrix matrix-glow text-5xl text-white md:text-6xl">
          TECH STACK
        </h1>
        <p class="mt-3 font-jetbrains text-sm text-green-400">
          Languages and tools I used
        </p>
      </header>

  <!-- Languages -->
  <section>
    <h2 class="mb-6 border-b border-green-800/60 pb-3 font-matrix text-3xl text-green-400">
      LANGUAGES
    </h2>

    <div class="grid grid-cols-1 gap-5 sm:grid-cols-2 md:grid-cols-3">
      <StackCard
        v-for="item in languages"
        :key="item.name"
        :name="item.name"
        :image="item.image"
      />
    </div>
  </section>

  <!-- Tools -->
  <section>
    <h2 class="mb-6 border-b border-green-800/60 pb-3 font-matrix text-3xl text-green-400">
      TOOLS
    </h2>
    <div class="grid grid-cols-1 gap-5 sm:grid-cols-2 md:grid-cols-3">
      <StackCard
        v-for="item in tools"
        :key="item.name"
        :name="item.name"
        :image="item.image"
      />
    </div>
  </section>
    </div>
  </section>
</template>