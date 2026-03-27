<script lang="ts">
  import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
  <title>PEF Partnership - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="relative overflow-hidden bg-white py-24 text-center border-b border-slate-100">
  <div class="absolute inset-0 bg-grid-slate-900/[0.02] [mask-image:linear-gradient(0deg,white,rgba(255,255,255,0.6))]"></div>
  <div class="container relative mx-auto px-4">
    <span class="mb-4 inline-block rounded-full bg-school-gold/10 px-4 py-1.5 text-xs font-bold tracking-widest text-school-gold uppercase ring-1 ring-school-gold/20">
      Verified Partnership
    </span>
    <h1 class="text-5xl font-black tracking-tight sm:text-7xl text-school-navy mb-6">Our <span class="text-school-gold">PEF</span> Partnership</h1>
    <p class="mx-auto max-w-2xl text-xl text-slate-500 font-light leading-relaxed">Baba Farid Public School is a proudly registered institution with the Punjab Education Foundation.</p>
  </div>
</div>

<section class="relative py-24 lg:py-32 overflow-hidden bg-white">
  <div class="absolute top-0 right-0 -translate-y-1/2 translate-x-1/2 w-[500px] h-[500px] bg-school-gold/5 rounded-full blur-3xl opacity-50"></div>
  <div class="container relative mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-16 lg:grid-cols-2 items-center">
      
      <div>
        <h2 class="text-4xl font-black text-school-navy tracking-tight mb-8">What is <span class="text-school-gold">PEF?</span></h2>
        <div class="mb-10 h-1.5 w-24 rounded-full bg-gradient-to-r from-school-gold to-school-navy"></div>
        <p class="text-xl leading-relaxed text-slate-600 font-light">
          The <strong class="text-school-navy font-bold">Punjab Education Foundation (PEF)</strong> is an autonomous statutory body established by the Government of Punjab. Its primary objective is to encourage and promote quality education on a non-commercial basis, particularly in less affluent areas.
        </p>
        <p class="mt-8 text-xl leading-relaxed text-slate-600 font-light">
          Through public-private partnerships, PEF provides financial assistance to schools like ours, enabling us to offer 100% free education to our students. This program ensures that every child has access to quality education regardless of their socio-economic background.
        </p>
      </div>
      
      <div class="relative">
        <div class="absolute -inset-8 bg-slate-50 rounded-[3rem] ring-1 ring-slate-100"></div>
        <div class="relative z-10 p-10 bg-white rounded-[3rem] shadow-2xl ring-1 ring-slate-200 border-t-8 border-t-school-navy group overflow-hidden transition-all duration-500 hover:shadow-school-navy/10">
           <div class="absolute -right-20 -top-20 h-64 w-64 bg-school-gold/5 rounded-full blur-3xl group-hover:bg-school-gold/10 transition-all duration-700"></div>
           
           <div class="mb-12 flex justify-center relative">
             <div class="flex h-32 w-32 items-center justify-center rounded-[2.5rem] bg-school-navy text-school-gold shadow-2xl transform rotate-3 group-hover:rotate-0 transition-transform duration-500">
                <svg class="h-16 w-16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M12 21v-8.25M15.75 21v-8.25M8.25 21v-8.25M3 9l9-6 9 6m-1.5 12V10.332A48.36 48.36 0 0012 9.75c-2.551 0-5.056.2-7.5.582V21M3 21h18M12 6.75h.008v.008H12V6.75z" />
                </svg>
             </div>
           </div>
           
           <h3 class="mb-10 text-center text-3xl font-black text-school-navy leading-tight">Elite Partner <br/><span class="text-school-gold text-lg uppercase tracking-[0.3em]">of the State</span></h3>
           <ul class="space-y-6">
             {#each [
               'Fully sponsored tuition for all students (Class 1-8)',
               'Free distribution of premium curriculum textbooks',
               'Annual Quality Assurance Tests (QAT) verification'
             ] as benefit}
               <li class="flex items-start gap-4">
                  <div class="h-6 w-6 rounded-full bg-school-gold/20 flex items-center justify-center text-school-gold shadow-sm shrink-0 mt-1">
                    <svg class="h-3.5 w-3.5" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <span class="text-slate-600 font-medium text-lg leading-snug">{benefit}</span>
               </li>
             {/each}
           </ul>
        </div>
      </div>

    </div>
  </div>
</section>
