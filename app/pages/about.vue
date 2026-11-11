
<script setup>
useHead({
  title: 'About | Lawrence Dave Corral'
})

useSeoMeta({
  description: 'Explore the portfolio of Lawrence Dave Corral, an aspiring Frontend Web Developer interested in creating functional and engaging digital experiences.'
})
</script>

<template>
  <section class="relative isolate min-h-screen overflow-hidden px-4 pt-4 pb-16">

    <!-- Matrix Background -->
    <MatrixBackground />

    <!-- Static Background Image -->
    <div
      class="pointer-events-none fixed inset-0 -z-10 bg-[url('/images/about/about-matrix.jpg')] bg-cover bg-center opacity-15"
      aria-hidden="true"
    ></div>

    <!-- Page Content -->
    <div class="relative z-10 mx-auto max-w-6xl">

      <!-- MY JOURNEY HEADING -->
      <header class="mb-10 md:mb-14">
        <p class="mb-4 font-jetbrains text-xs tracking-[0.25em] text-green-500">
          02 / PERSONAL BACKGROUND
        </p>

        <div class="flex flex-col justify-between gap-5 md:flex-row md:items-end">
          <h1 class="font-matrix text-5xl leading-none text-white md:text-7xl">
            MY <span class="matrix-glow text-green-400">JOURNEY</span>
          </h1>

          <p class="max-w-sm font-jetbrains text-xs leading-6 text-gray-500">
            A look into my interest in technology, my experiences, and the path I want to pursue.
          </p>
        </div>

        <div class="mt-6 h-px w-full bg-gradient-to-r from-green-500/70 via-green-800/40 to-transparent"></div>
      </header>

      <!-- PROFILE AND TIMELINE OF ABOUT PAGE -->
      <div class="grid items-start gap-10 lg:grid-cols-12 lg:gap-12">

        <!-- LEFT COLUMN: PROFILE -->
        <aside class="lg:col-span-4">

          <!-- PROFILE CARD -->
          <div class="group relative overflow-hidden border border-green-800/60 bg-black/80 p-6 shadow-[0_0_30px_rgba(0,255,100,0.05)] transition-all duration-500 hover:border-green-500/70 hover:shadow-[0_0_35px_rgba(0,255,100,0.12)] motion-reduce:transition-none md:p-7">

            <!-- Decorative Corner -->
            <div
              class="pointer-events-none absolute right-0 top-0 h-20 w-20 border-r border-t border-green-500/30"
              aria-hidden="true"
            ></div>

            <!-- Profile Label -->
            <div class="mb-7 flex items-center justify-between">
              <p class="font-jetbrains text-xs tracking-[0.2em] text-green-500">
                ABOUT / PROFILE
              </p>

              <span class="font-jetbrains text-[10px] text-gray-600">
                01
              </span>
            </div>

            <!-- Portrait -->
            <div class="relative mx-auto mb-7 w-fit">
              <div
                class="absolute -inset-3 rounded-full border border-green-500/30 transition-all duration-500 group-hover:border-green-400/70 group-hover:shadow-[0_0_25px_rgba(0,255,100,0.12)]"
                aria-hidden="true"
              ></div>

              <img
                src="/images/home/home-lawrence.jpg"
                alt="Portrait of Lawrence Dave Corral"
                class="relative h-32 w-32 rounded-full border-2 border-green-500 object-cover shadow-[0_0_20px_rgba(0,255,100,0.2)] transition-transform duration-500 group-hover:scale-105 motion-reduce:transition-none md:h-40 md:w-40"
              />
            </div>

            <!-- Name and Career Direction -->
            <div class="text-center">
              <h2 class="matrix-glow font-matrix text-4xl text-white md:text-5xl">
                ABOUT ME
              </h2>

              <h3 class="mt-3 font-cyber text-base leading-relaxed text-green-400 md:text-lg">
                LAWRENCE DAVE CORRAL
              </h3>

              <p class="mt-3 font-jetbrains text-[10px] leading-6 tracking-wide text-gray-400 md:text-xs">
                ASPIRING FRONTEND WEB AND GAME DEVELOPER
              </p>
            </div>
          </div>
         
          <!-- AREA OF INTEREST -->
          <div class="mt-5 border-l-2 border-green-800/60 py-2 pl-4 transition-all duration-300 hover:border-green-400">

            <p class="font-jetbrains text-[10px] leading-6 tracking-wider text-gray-500">
              AREA OF INTEREST_
            </p>

            <p class="font-jetbrains text-xs leading-6 text-green-400">
              WEB DEVELOPMENT & UI DESIGN
            </p>

          </div>

        </aside>


        <!-- RIGHT COLUMN: MY JOURNEY TIMELINE -->
        <main class="lg:col-span-8">

          <div class="relative space-y-7">

            <!-- Timeline Line -->
            <div
              class="absolute bottom-8 left-[19px] top-8 w-px bg-gradient-to-b from-green-400/80 via-green-700/50 to-transparent"
              aria-hidden="true"
            ></div>

            <!-- ENTRY 01 -->
            <article class="group relative pl-12">

              <!-- Timeline -->
              <div class="absolute left-0 top-6 z-10 flex h-10 w-10 items-center justify-center rounded-full border border-green-500/60 bg-[#07120a] font-jetbrains text-xs text-green-400 shadow-[0_0_15px_rgba(0,255,100,0.12)] transition-all duration-300 group-hover:border-green-300 group-hover:bg-green-950 group-hover:shadow-[0_0_20px_rgba(0,255,100,0.3)]">
                01
              </div>

              <!-- Content Card -->
              <div class="relative overflow-hidden border border-green-900/60 bg-black/80 p-5 transition-all duration-300 hover:-translate-y-1 hover:border-green-500/60 hover:shadow-[0_0_25px_rgba(0,255,100,0.08)] motion-reduce:transition-none md:p-7">

                <div
                  class="pointer-events-none absolute right-0 top-0 h-14 w-14 border-r border-t border-green-500/20"
                  aria-hidden="true"
                ></div>

                <p class="mb-3 font-jetbrains text-[10px] tracking-[0.2em] text-green-500">
                  THE BEGINNING
                </p>

                <h3 class="mb-4 font-cyber text-base text-white md:text-lg">
                  Where It All Started
                </h3>

                <p class="text-sm leading-7 text-gray-400 md:text-base">
                  Hello! I'm Lawrence Dave S. Corral, currently studying Information Technology at St. Dominic College of Asia. My interest in technology started with my passion for playing video games, which eventually made me curious about how digital worlds, interfaces, and the systems behind them are created.
                </p>

                <span class="mt-5 block text-right font-jetbrains text-[10px] text-green-700">
                  ENTRY_001
                </span>

              </div>
            </article>

            <!-- ENTRY 02 -->
            <article class="group relative pl-12 lg:ml-6">

              <!-- Timeline -->
              <div class="absolute left-0 top-6 z-10 flex h-10 w-10 items-center justify-center rounded-full border border-green-500/60 bg-[#07120a] font-jetbrains text-xs text-green-400 shadow-[0_0_15px_rgba(0,255,100,0.12)] transition-all duration-300 group-hover:border-green-300 group-hover:bg-green-950 group-hover:shadow-[0_0_20px_rgba(0,255,100,0.3)]">
                02
              </div>

              <!-- Content Card -->
              <div class="relative overflow-hidden border border-green-900/60 bg-gradient-to-br from-green-950/20 to-black/90 p-5 transition-all duration-300 hover:-translate-y-1 hover:border-green-500/60 hover:shadow-[0_0_25px_rgba(0,255,100,0.08)] motion-reduce:transition-none md:p-7">

                <div
                  class="pointer-events-none absolute right-0 top-0 h-14 w-14 border-r border-t border-green-500/20"
                  aria-hidden="true"
                ></div>

                <p class="mb-3 font-jetbrains text-[10px] tracking-[0.2em] text-green-500">
                  THE LEARNING PROCESS
                </p>

                <h3 class="mb-4 font-cyber text-base text-white md:text-lg">
                  Growing Through Learning
                </h3>

                <p class="text-sm leading-7 text-gray-400 md:text-base">
                  That curiosity led me to pursue a degree in Information Technology, where I began exploring programming, web development, and the logic behind the applications we use every day. I'm naturally a quiet person, but I continuously work on improving my communication and teamwork skills, recognizing how important they are in the IT field.
                </p>

                <span class="mt-5 block text-right font-jetbrains text-[10px] text-green-700">
                  ENTRY_002
                </span>

              </div>
            </article>


            <!-- ENTRY 03 -->
            <article class="group relative pl-12">

              <!-- Timeline -->
              <div class="absolute left-0 top-6 z-10 flex h-10 w-10 items-center justify-center rounded-full border border-green-500/60 bg-[#07120a] font-jetbrains text-xs text-green-400 shadow-[0_0_15px_rgba(0,255,100,0.12)] transition-all duration-300 group-hover:border-green-300 group-hover:bg-green-950 group-hover:shadow-[0_0_20px_rgba(0,255,100,0.3)]">
                03
              </div>

              <!-- Content Card -->
              <div class="relative overflow-hidden border border-green-900/60 bg-black/80 p-5 transition-all duration-300 hover:-translate-y-1 hover:border-green-500/60 hover:shadow-[0_0_25px_rgba(0,255,100,0.08)] motion-reduce:transition-none md:p-7">

                <div
                  class="pointer-events-none absolute right-0 top-0 h-14 w-14 border-r border-t border-green-500/20"
                  aria-hidden="true"
                ></div>

                <p class="mb-3 font-jetbrains text-[10px] tracking-[0.2em] text-green-500">
                  THE DIRECTION
                </p>

                <h3 class="mb-4 font-cyber text-base text-white md:text-lg">
                  Looking Ahead
                </h3>

                <p class="text-sm leading-7 text-gray-400 md:text-base">
                  My current goal is to become a Frontend Web Developer. I'm interested in creating websites that combine functionality, thoughtful design, and engaging user experiences. I want to continue exploring modern web technologies, developing my skills, and turning ideas into projects that people can actually use.
                </p>

                <span class="mt-5 block text-right font-jetbrains text-[10px] text-green-700">
                  ENTRY_003
                </span>

              </div>
            </article>

          </div>
        </main>

      </div>
    </div>
  </section>
</template>
