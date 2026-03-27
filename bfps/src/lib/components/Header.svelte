<script lang="ts">
  import { page } from '$app/stores';
  
  let isMobileMenuOpen = $state(false);

  const links = [
    { href: '/', label: 'Home' },
    { href: '/about', label: 'About Us' },
    { href: '/academics', label: 'Academics' },
    { href: '/admissions', label: 'Admissions' },
    { href: '/pef', label: 'PEF' },
    { href: '/qat-results', label: 'QAT Results' },
    { href: '/check-result', label: 'Check Result' },
    { href: '/blog', label: 'Blog & News' },
    { href: '/gallery', label: 'Gallery' },
    { href: '/contact', label: 'Contact' }
  ];

  function toggleMobileMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
  }
</script>

<header class="sticky top-0 z-50 w-full bg-school-navy text-white shadow-md">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex h-20 items-center justify-between">
      <!-- Logo -->
      <div class="flex flex-shrink-0 items-center">
        <a href="/" class="flex items-center transition-transform hover:scale-[1.02]">
          <img src="/image-removebg-preview.png" alt="Baba Farid Public School Logo" class="h-14 w-auto sm:h-20 lg:h-24" />
        </a>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden flex-1 justify-center lg:flex">
        <ul class="flex items-center space-x-6 xl:space-x-8">
          {#each links as link}
            <li>
              <a 
                href={link.href} 
                class="text-sm font-bold uppercase tracking-wider transition-all hover:text-school-gold {$page.url.pathname === link.href ? 'text-school-gold border-b-2 border-school-gold pb-1' : 'text-slate-100 hover:opacity-80'}"
              >
                {link.label}
              </a>
            </li>
          {/each}
        </ul>
      </nav>

      <!-- Mobile menu button -->
      <div class="flex items-center lg:hidden">
        <button 
          type="button" 
          class="group inline-flex items-center justify-center gap-2 rounded-xl bg-white/5 px-3 py-2 text-slate-200 transition-all hover:bg-white/10 hover:text-white focus:outline-none focus:ring-2 focus:ring-school-gold"
          onclick={toggleMobileMenu}
        >
          <span class="text-xs font-bold uppercase tracking-widest transition-colors group-hover:text-school-gold">Menu</span>
          {#if !isMobileMenuOpen}
            <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          {:else}
            <svg class="block h-6 w-6 text-school-gold" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          {/if}
        </button>
      </div>
    </div>
  </div>

  <!-- Mobile Menu -->
  {#if isMobileMenuOpen}
    <div class="lg:hidden bg-school-navy border-t border-white/5 shadow-2xl animate-in fade-in slide-in-from-top-4 duration-300">
      <div class="space-y-1 px-4 pb-8 pt-4">
        {#each links as link}
          <a 
            href={link.href} 
            class="flex items-center justify-between rounded-xl px-4 py-3.5 text-base font-bold tracking-tight transition-all {$page.url.pathname === link.href ? 'bg-school-gold text-school-navy shadow-lg' : 'text-slate-200 hover:bg-white/5 hover:text-white'}"
            onclick={() => isMobileMenuOpen = false}
          >
            <span>{link.label}</span>
            {#if $page.url.pathname === link.href}
              <svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="3">
                <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
              </svg>
            {:else}
              <svg class="h-4 w-4 opacity-30" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
              </svg>
            {/if}
          </a>
        {/each}
        
        <div class="mt-6 px-4 py-6 rounded-2xl bg-white/5 border border-white/5">
           <p class="text-[10px] uppercase tracking-[0.2em] text-school-gold font-black mb-1">Status</p>
           <p class="text-xs text-white/50 font-medium italic">Empowering Minds, Transforming Futures.</p>
        </div>
      </div>
    </div>
  {/if}
</header>
