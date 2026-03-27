<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  import Card from '$lib/components/Card.svelte';
  
  let rollNumber = $state('');
  let searchStatus = $state<'idle' | 'searching' | 'notFound' | 'found'>('idle');
  
  function handleSearch(e: Event) {
    e.preventDefault();
    if (!rollNumber) return;
    
    searchStatus = 'searching';
    
    // Simulate lookup delay
    setTimeout(() => {
      // For demo purposes, any roll number ending in '1' is "found"
      if (rollNumber.endsWith('1')) {
        searchStatus = 'found';
      } else {
        searchStatus = 'notFound';
      }
    }, 1200);
  }
</script>

<svelte:head>
  <title>Student Result Lookup - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold uppercase">Check Result</h1>
    <p class="mt-4 text-lg text-slate-500 font-light">Enter your roll number below to access your academic performance report.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24 relative overflow-hidden">
  <!-- Decorative Elements -->
  <div class="absolute -right-40 -top-40 h-96 w-96 bg-school-gold/5 rounded-full blur-3xl"></div>
  <div class="absolute -left-40 -bottom-40 h-96 w-96 bg-school-navy/5 rounded-full blur-3xl"></div>

  <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
    <div class="max-w-2xl mx-auto">
      
      <!-- Lookup Form Card -->
      <div class="bg-white rounded-[2.5rem] p-8 md:p-12 shadow-2xl ring-1 ring-slate-100 hover:ring-school-gold/20 transition-all duration-500">
        <div class="py-12 text-center">
           <div class="inline-flex h-24 w-24 items-center justify-center rounded-full bg-slate-50 text-school-gold shadow-sm ring-1 ring-slate-100 mb-8 relative">
              <svg class="h-10 w-10 animate-pulse" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v6h4.5m4.5 0a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <div class="absolute -right-2 -top-2 h-6 w-6 bg-school-navy rounded-full border-2 border-white flex items-center justify-center">
                 <div class="h-2 w-2 bg-school-gold rounded-full animate-ping"></div>
              </div>
           </div>
           
           <h2 class="text-4xl font-black text-school-navy mb-4 tracking-tight uppercase">Coming <span class="text-school-gold">Soon</span></h2>
           <p class="text-slate-500 font-light text-lg mb-10 max-w-sm mx-auto leading-relaxed">
             Our online student result management system is currently under development. Stay tuned for a world-class digital experience.
           </p>
           
           <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 inline-block">
             <span class="text-xs font-bold text-slate-400 uppercase tracking-widest block mb-2">Notice</span>
             <p class="text-sm font-bold text-school-navy">Wait for the Next Academic Session Updates</p>
           </div>
        </div>
      </div>

      <!-- FAQ Section -->
      <div class="mt-16 text-center">
        <p class="text-slate-400 text-sm">Facing issues? Contact the Administration Office: <span class="text-school-navy font-bold">0300-6937159</span></p>
      </div>

    </div>
  </div>
</section>
