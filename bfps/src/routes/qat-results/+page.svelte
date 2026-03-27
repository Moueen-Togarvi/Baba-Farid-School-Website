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
    <div class="mx-auto max-w-4xl">
      
      <div class="mb-12 text-center">
        <h2 class="text-3xl font-bold text-school-navy">Academic Excellence Guaranteed</h2>
        <div class="mx-auto mt-4 h-1 w-20 rounded-full bg-school-gold"></div>
        <p class="mt-6 text-slate-600">
          As a registered PEF partner school, our students undergo rigorous Quality Assurance Tests (QAT) annually. Our results speak for themselves, demonstrating our unwavering commitment to educational excellence.
        </p>
      </div>

      <div class="overflow-hidden rounded-2xl bg-white shadow-sm ring-1 ring-slate-200">
        <ul class="divide-y divide-slate-100">
          {#each qatResults as result}
            <li class="flex flex-col sm:flex-row items-start sm:items-center justify-between p-6 transition-colors">
              <div class="flex items-center gap-6">
                <div class="flex h-16 w-16 shrink-0 flex-col items-center justify-center rounded-xl bg-school-navy text-school-gold">
                   <span class="text-xl font-bold">{result.year}</span>
                </div>
                <div>
                   <h3 class="text-xl font-bold text-school-navy">{result.passRate}% Pass Rate</h3>
                   <p class="text-sm text-slate-500 mt-1">{result.text}</p>
                </div>
              </div>
              
              <div class="mt-4 sm:mt-0 flex items-center gap-2 rounded-full bg-school-green/10 px-4 py-1.5 text-sm font-medium text-school-green">
                <svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z" />
                </svg>
                PEF Verified
              </div>
            </li>
          {/each}
        </ul>
      </div>

    </div>
  </div>
</section>
