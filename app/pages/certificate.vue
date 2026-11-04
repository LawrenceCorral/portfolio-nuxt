
<script setup>
import { ref } from 'vue'

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

const verificationUrl =
  'https://www.certiport.com/portal/pages/credentialverification.aspx'

const selectedCertificate = ref(null)

function openCertificate(certificate) {
  selectedCertificate.value = certificate
}

function closeCertificate() {
  selectedCertificate.value = null
}
</script>

<template>
  <section class="relative isolate min-h-screen overflow-hidden px-4 py-10">
    <MatrixBackground />

    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/certificates/home-matrix.jpg')] bg-cover bg-center opacity-20"
      aria-hidden="true"
    ></div>

    <div class="relative z-10 mx-auto w-full max-w-5xl">
      <h1 class="mb-10 text-center font-matrix text-5xl text-green-400 matrix-glow md:text-6xl">
        MY CERTIFICATES
      </h1>

      <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3">
        <article
          v-for="certificate in certificates"
          :key="certificate.name"
          class="flex flex-col items-center gap-5 border border-green-800/60 bg-black/70 p-5 transition hover:-translate-y-1 hover:border-green-400"
        >
          <button
            type="button"
            class="w-full cursor-pointer"
            :aria-label="`View ${certificate.name}`"
            @click="openCertificate(certificate)"
          >
            <img
              :src="certificate.badge"
              :alt="certificate.name"
              class="mx-auto w-full max-w-56 object-contain"
            />
          </button>

          <h2 class="text-center font-jetbrains text-sm text-white">
            {{ certificate.name }}
          </h2>

          <a
            :href="verificationUrl"
            target="_blank"
            rel="noopener noreferrer"
            class="border border-green-700/60 px-4 py-2 font-jetbrains text-xs text-green-400 hover:border-green-400 hover:bg-green-500/10"
          >
            VERIFY CERTIFICATE
          </a>
        </article>
      </div>
    </div>

    <!-- Certificate Lightbox -->
    <div
      v-if="selectedCertificate"
      class="fixed inset-0 z-[9999] flex items-center justify-center bg-black/95 p-4"
      @click.self="closeCertificate"
    >
      <div class="flex max-h-[90vh] w-full max-w-4xl flex-col items-center gap-4 border border-green-500 bg-black p-5">

        <button
          type="button"
          class="self-end border border-green-700 px-4 py-2 font-jetbrains text-sm text-green-400 hover:border-green-400"
          @click="closeCertificate"
        >
          CLOSE ✕
        </button>

        <img
          :src="selectedCertificate.image"
          :alt="selectedCertificate.name"
          class="max-h-[70vh] max-w-full object-contain"
        />

        <p class="font-jetbrains text-sm text-green-400">
          {{ selectedCertificate.name }}
        </p>

      </div>
    </div>
  </section>
</template>
