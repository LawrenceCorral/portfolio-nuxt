<script setup>
useHead({
  title: 'Certificates | Lawrence Dave Corral'
})

useSeoMeta({
  description: 'View the certificates and credentials earned by Lawrence Dave Corral.'
})

const certificates = [
  {
    name: 'PowerPoint Badge',
    badge: '/images/certificates/cert-ppt-badge.png',
    image: '/images/certificates/cert-ppt.jpg'
  },
  {
    name: 'Word Badge',
    badge: '/images/certificates/cert-word-badge.png',
    image: '/images/certificates/cert-word.jpg'
  },
  {
    name: 'Java Badge',
    badge: '/images/certificates/cert-java-badge.png',
    image: '/images/certificates/cert-java.jpg'
  }
]

const verificationUrl ='https://www.certiport.com/portal/pages/credentialverification.aspx'
</script>

<template>
  <section class="relative isolate min-h-screen overflow-hidden px-4 py-12">
    <MatrixBackground />

    <!-- Background Image -->
    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/certificates/cert-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

    <div class="relative z-10 mx-auto flex max-w-5xl flex-col gap-10">
      <!-- Page Heading -->
      <header class="text-center">
        <h1 class="font-matrix matrix-glow text-5xl text-white md:text-6xl">
          CERTIFICATES
        </h1>
        <p class="mt-3 font-jetbrains text-sm text-green-400">
          My achievements and credentials
        </p>
      </header>

      <!-- Certificate Gallery -->
      <div class="grid grid-cols-1 gap-8 sm:grid-cols-2 md:grid-cols-3">
        <article
          v-for="certificate in certificates"
          :key="certificate.name"
          class="flex flex-col items-center gap-5 border border-green-800/60 bg-black/70 p-5"
        >
          <a
            :href="certificate.image"
            target="_blank"
            rel="noopener noreferrer"
            :aria-label="`View ${certificate.name}`"
          >
            <img
              :src="certificate.badge"
              :alt="certificate.name"
              class="w-full max-w-56 object-contain transition-transform duration-200 hover:scale-105"
            />
          </a>

          <h2 class="text-center font-jetbrains text-sm text-white">
            {{ certificate.name }}
          </h2>

          <a
            :href="verificationUrl"
            target="_blank"
            rel="noopener noreferrer"
            class="border border-green-700/60 px-4 py-2 font-jetbrains text-xs text-green-400 transition-colors hover:border-green-400 hover:bg-green-500/10"
          >
            VERIFY CERTIFICATE
          </a>
        </article>
      </div>
    </div>
  </section>
</template>