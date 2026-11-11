<template>

<header
  class="relative z-10 mx-auto flex w-full flex-col items-center justify-between border-b border-green-900/50 pb-4 mb-6 md:flex-row"
>

<NuxtLink 
  to="/" 
  class="text-3xl font-matrix tracking-widest text-white matrix-glow"
>
    CORRAL
</NuxtLink>
  

<nav
  aria-label="Main Navigation"
  class="navbar-desktop-links flex gap-6 text-sm uppercase font-jetbrains text-white"
>

 <NuxtLink 
  to="/" 
  class="hover:text-green-400 transition-colors"
  active-class="text-green-400"
  exact-active-class="text-green-400"
>
    HOME
</NuxtLink>

 <NuxtLink 
  to="/about" 
  class="hover:text-green-400 transition-colors"
  active-class="text-green-400"
  exact-active-class="text-green-400"
>
    ABOUT
</NuxtLink>

 <NuxtLink 
  to="/stacks" 
  class="hover:text-green-400 transition-colors"
  active-class="text-green-400"
  exact-active-class="text-green-400"
>
    STACKS
</NuxtLink>
  
 <NuxtLink 
  to="/certificate" 
  class="hover:text-green-400 transition-colors"
  active-class="text-green-400"
  exact-active-class="text-green-400"
>
    CERTIFICATE
</NuxtLink>
</nav>


    <div class="navbar-mobile-menu dropdown dropdown-end mt-4">
      <button
        tabindex="0"
        type="button"
        aria-label="Open navigation menu"
        class="btn btn-ghost btn-square text-green-400"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-6 h-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>

      <ul
        tabindex="0"
        class="menu menu-sm dropdown-content bg-black/95 border border-green-900
        rounded-box z-50 mt-3 w-52 p-2 shadow-xl font-jetbrains uppercase"
        >
         <li><NuxtLink to="/">HOME</NuxtLink></li>
         <li><NuxtLink to="/about">ABOUT</NuxtLink></li>
         <li><NuxtLink to="/stacks">STACKS</NuxtLink></li>
         <li><NuxtLink to="/certificate">CERTIFICATES</NuxtLink></li>
        
    </ul>
    </div>

</header>
</template>

<style scoped>
.navbar-desktop-links {
  display: flex !important;
}

.navbar-mobile-menu {
  display: none !important;
}

@media (max-width: 47.999rem) {
  .navbar-desktop-links {
    display: none !important;
  }

  .navbar-mobile-menu {
    display: block !important;
  }
}
</style>