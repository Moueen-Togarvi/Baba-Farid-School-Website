<script lang="ts">
  import Card from '$lib/components/Card.svelte';
  
  // Sample Data. In a real app, this could come from a database or CMS.
  const qatResults = [
    { year: 2024, passRate: 87, text: 'Consistently maintaining excellence' },
    { year: 2023, passRate: 85, text: 'Awarded highest category by PEF' },
    { year: 2022, passRate: 83, text: 'Exceeded regional pass averages' },
    { year: 2021, passRate: 80, text: 'Strong performance despite pandemic challenges' },
    { year: 2020, passRate: 82, text: 'Recognized for outstanding primary results' }
  ];
</script>

<svelte:head>
  <title>QAT Results - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">QAT Results</h1>
    <p class="mt-4 text-lg text-slate-500">Our annual Quality Assurance Test (QAT) performance.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto mb-20 text-center">
      <div class="inline-flex items-center justify-center gap-2 px-4 py-2 bg-school-gold/10 text-school-gold rounded-full text-xs font-bold border border-school-gold/20 mb-6 uppercase tracking-widest">
         <svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
           <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
         </svg>
         Excellence Verified
      </div>
      <h2 class="text-3xl md:text-5xl font-black text-school-navy tracking-tight mb-6">Quality Assurance <span class="text-school-gold">Performance</span></h2>
      <p class="text-lg text-slate-500 font-light leading-relaxed">
        As a registered PEF partner, our standards are rigorously verified. These annual Quality Assurance Tests (QAT) demonstrate our consistent ranking among the top-tier institutions.
      </p>
    </div>

    <!-- Results Grid -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each qatResults as result}
        <div class="flex flex-col items-center text-center p-10 rounded-3xl bg-slate-50 shadow-sm ring-1 ring-slate-100 hover:bg-white hover:shadow-2xl transition-all duration-500 group border-b-4 border-transparent hover:border-school-gold">
           <span class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-4 inline-block bg-white px-3 py-1 rounded-full ring-1 ring-slate-100">{result.year}</span>
           <p class="text-6xl font-black text-school-navy group-hover:text-school-gold transition-colors duration-300 mb-2">{result.passRate}%</p>
           <p class="text-sm font-medium text-slate-500 mt-2 max-w-[200px] leading-relaxed">{result.text}</p>
        </div>
      {/each}
      
      <!-- PEF Badge Card -->
      <div class="flex flex-col justify-center items-center text-center p-10 rounded-3xl bg-school-navy text-white shadow-xl hover:-translate-y-2 transition-transform duration-500 relative overflow-hidden border-b-4 border-school-gold lg:col-span-1">
         <div class="absolute -right-10 -top-10 h-32 w-32 bg-white/5 rounded-full blur-2xl"></div>
         <div class="absolute -left-10 -bottom-10 h-32 w-32 bg-school-gold/20 rounded-full blur-2xl"></div>
         
         <svg class="h-12 w-12 text-school-gold mb-6 relative z-10" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
           <path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75L11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 01-1.043 3.296 3.745 3.745 0 01-3.296 1.043A3.745 3.745 0 0112 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 01-3.296-1.043 3.745 3.745 0 01-1.043-3.296A3.745 3.745 0 013 12c0-1.268.63-2.39 1.593-3.068a3.745 3.745 0 011.043-3.296 3.746 3.746 0 013.296-1.043A3.746 3.746 0 0112 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 013.296 1.043 3.746 3.746 0 011.043 3.296A3.745 3.745 0 0121 12z" />
         </svg>
         
         <span class="relative z-10 text-xs font-bold text-school-gold uppercase tracking-widest mb-2">Authenticated</span>
         <p class="relative z-10 text-3xl font-black mb-2 leading-tight">PEF Certified Excellence</p>
         <p class="relative z-10 text-xs text-white/50">Quality Matrix Verified</p>
      </div>
    </div>
  </div>
</section>
