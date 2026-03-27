<script lang="ts">
  import { page } from '$app/stores';
  
  let isMobileMenuOpen = $state(false);

  const links = [
    { href: '/', label: 'Home' },
    { href: '/about', label: 'About Us' },
    { href: '/academics', label: 'Academics' },
    { href: '/admissions', label: 'Admissions' },
    { href: '/gallery', label: 'Gallery' },
    { href: '/pef', label: 'PEF' },
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
        <a href="/" class="flex items-center">
          <img src="/WhatsApp_Image_2026-03-27_at_4.39.16_PM-removebg-preview.png" alt="Baba Farid Public School Logo" class="h-16 w-auto sm:h-20" />
        </a>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden lg:block">
        <ul class="flex items-center space-x-6 xl:space-x-8">
          {#each links as link}
            <li>
              <a 
                href={link.href} 
                class="text-sm font-medium transition-colors hover:text-school-gold {$page.url.pathname === link.href ? 'text-school-gold font-bold' : 'text-slate-100'}"
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
          class="inline-flex items-center justify-center rounded-md p-2 text-slate-200 hover:bg-school-navy hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-school-gold"
          onclick={toggleMobileMenu}
        >
          <span class="sr-only">Open main menu</span>
          {#if !isMobileMenuOpen}
            <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          {:else}
            <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          {/if}
        </button>
      </div>
    </div>
  </div>

  <!-- Mobile Menu -->
  {#if isMobileMenuOpen}
    <div class="lg:hidden bg-school-navy border-t border-blue-800">
      <div class="space-y-1 px-4 pb-4 pt-2 shadow-inner">
        {#each links as link}
          <a 
            href={link.href} 
            class="block rounded-md px-3 py-2 text-base font-medium transition-colors {$page.url.pathname === link.href ? 'bg-blue-800 text-school-gold' : 'text-slate-200 hover:bg-blue-800 hover:text-white'}"
            onclick={() => isMobileMenuOpen = false}
          >
            {link.label}
          </a>
        {/each}
      </div>
    </div>
  {/if}
</header>
