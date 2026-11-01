<template>

<header 
 class = "w-full max-w-4x1 mx-auto flex flex -col md:flex-row
          justify-between items-center 
          border-b border-green-900/50 pb-2 mb-12"
>

--Portolio Name/Branding--

<NuxtLink 
  to="/" 
  class="text-3xl font-matrix tracking-widest text-white matrix-glow"
>
    CORRAL
</NuxtLink>
  
--Desktop Navigation Links--

<nav 
 aria-label="Main Navigation"
 class="hidden md:flex gap-6 text-sm uppercase font-jetbrains"
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
  to="/" 
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
  to="/certificates" 
  class="hover:text-green-400 transition-colors"
  active-class="text-green-400"
  exact-active-class="text-green-400"
>
    CERTIFICATES
</NuxtLink>
</nav>

--For Mobile Navigation Links--

    <div class="dropdown dropdown-end md:hidden mt-4">
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
        rounded-box z-50 mt-3 w-52 p-2 shadow-x1 font-jetbrains uppercase"
        >
         <li><NuxtLink to="/">HOME</NuxtLink></li>
         <li><NuxtLink to="/about">ABOUT</NuxtLink></li>
         <li><NuxtLink to="/stacks">STACKS</NuxtLink></li>
         <li><NuxtLink to="/certificates">CERTIFICATES</NuxtLink></li>
        
    </ul>
    </div>

</header>
</template>