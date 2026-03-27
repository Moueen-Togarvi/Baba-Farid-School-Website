<script lang="ts">
  import Card from '$lib/components/Card.svelte';
  
  const subjects = [
    { name: 'English', icon: 'M3 5h12M9 3v2m1.048 9.5A18.022 18.022 0 016.412 9m6.088 9h7M11 21l5-10 5 10M12.751 5C11.783 10.77 8.07 15.61 3 18.129' },
    { name: 'Urdu', icon: 'M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253' },
    { name: 'Mathematics', icon: 'M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 11h.01M12 11h.01M9 11h.01M7 21h10a2 2 0 002-2V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2z' },
    { name: 'Science', icon: 'M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z' },
    { name: 'Islamiat', icon: 'M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253m0 0A17.919 17.919 0 0112 16.5c-3.162 0-6.133-.815-8.716-2.247m0 0A9.015 9.015 0 013 12c0-1.605.42-3.113 1.157-4.418' },
    { name: 'Social Studies', icon: 'M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z' }
  ];
</script>

<svelte:head>
  <title>Academics - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="relative overflow-hidden bg-white py-24 text-center border-b border-slate-100">
  <div class="absolute inset-0 bg-grid-slate-900/[0.02] [mask-image:linear-gradient(0deg,white,rgba(255,255,255,0.6))]"></div>
  <div class="container relative mx-auto px-4">
    <span class="mb-4 inline-block rounded-full bg-school-gold/10 px-4 py-1.5 text-xs font-bold tracking-widest text-school-gold uppercase ring-1 ring-school-gold/20">
      Academic Programs
    </span>
    <h1 class="text-5xl font-black tracking-tight sm:text-7xl text-school-navy mb-6">Our <span class="text-school-gold">Academics</span></h1>
    <p class="mx-auto max-w-2xl text-xl text-slate-500 font-light leading-relaxed">A comprehensive curriculum from Class 1 to 8 designed for holistic growth and elite success.</p>
  </div>
</div>

<section class="relative py-24 lg:py-32 overflow-hidden bg-white">
  <div class="absolute top-0 left-0 -translate-y-1/2 -translate-x-1/2 w-[500px] h-[500px] bg-school-gold/5 rounded-full blur-3xl opacity-50"></div>
  <div class="container relative mx-auto px-4 sm:px-6 lg:px-8">
    
    <!-- Primary & Middle Sections -->
    <div class="grid gap-12 lg:grid-cols-2">
      <!-- Primary -->
      <div class="group relative p-1 bg-white rounded-[3rem] shadow-xl hover:shadow-2xl transition-all duration-500 ring-1 ring-slate-200 border-t-4 border-t-school-gold">
         <div class="p-10">
            <h2 class="text-3xl font-black text-school-navy mb-2">Primary Classes</h2>
            <span class="inline-block px-3 py-1 rounded-full bg-school-gold/10 text-xs font-bold uppercase tracking-widest text-school-gold mb-8">Class 1 to 5</span>
            <div class="space-y-6 text-lg text-slate-500 font-light leading-relaxed">
               <p>Our primary section focuses on building a strong foundational base in literacy and numeracy. We encourage curiosity and active learning.</p>
               <ul class="space-y-4">
                 {#each ['Foundational Language Skills (English/Urdu)', 'Core Mathematics & Science Concepts', 'Islamiat & Ethical Building', 'Regular Assessment Frameworks'] as item}
                   <li class="flex items-center gap-3">
                      <div class="h-6 w-6 rounded-full bg-school-gold/20 flex items-center justify-center text-school-gold">
                        <svg class="h-3.5 w-3.5" fill="currentColor" viewBox="0 0 20 20">
                          <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                        </svg>
                      </div>
                      <span class="text-slate-700 font-medium text-sm">{item}</span>
                   </li>
                 {/each}
               </ul>
            </div>
         </div>
      </div>
      
      <!-- Middle -->
      <div class="group relative p-1 bg-white rounded-[3rem] shadow-xl hover:shadow-2xl transition-all duration-500 ring-1 ring-slate-200 border-t-4 border-t-school-navy">
         <div class="p-10">
            <h2 class="text-3xl font-black text-school-navy mb-2">Middle Classes</h2>
            <span class="inline-block px-3 py-1 rounded-full bg-school-navy/10 text-xs font-bold uppercase tracking-widest text-school-navy mb-8">Class 6 to 8</span>
            <div class="space-y-6 text-lg text-slate-500 font-light leading-relaxed">
               <p>The middle school curriculum expands upon the foundational knowledge, introducing more complex concepts and critical thinking exercises.</p>
               <ul class="space-y-4">
                 {#each ['Advanced Scientific Inquiry', 'Problem Solving in Mathematics', 'Depth in Humanities & Literature', 'Matriculation Prerequisite Training'] as item}
                   <li class="flex items-center gap-3">
                      <div class="h-6 w-6 rounded-full bg-school-navy/20 flex items-center justify-center text-school-navy">
                        <svg class="h-3.5 w-3.5" fill="currentColor" viewBox="0 0 20 20">
                          <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                        </svg>
                      </div>
                      <span class="text-slate-700 font-medium text-sm">{item}</span>
                   </li>
                 {/each}
               </ul>
            </div>
         </div>
      </div>
    </div>

    <!-- Core Subjects -->
    <div class="mt-24 lg:mt-32">
      <div class="mb-16 text-center max-w-3xl mx-auto">
        <h2 class="text-sm font-bold uppercase tracking-[0.2em] text-school-gold mb-4">Core Subjects</h2>
        <h3 class="text-4xl font-black text-school-navy tracking-tight mb-6">Foundations of <span class="text-school-gold">Excellence</span></h3>
        <p class="text-lg text-slate-500 font-light">Subject matter curated and approved by the Punjab Education Foundation for maximized intellectual impact.</p>
      </div>
      
      <div class="grid grid-cols-2 gap-6 sm:grid-cols-3 lg:grid-cols-6 lg:gap-8">
        {#each subjects as subject}
          <div class="group flex flex-col items-center rounded-[2rem] bg-slate-50 p-8 text-center transition-all duration-500 hover:-translate-y-2 hover:bg-white hover:shadow-2xl hover:ring-1 hover:ring-slate-100 border-b-4 border-transparent hover:border-school-gold">
            <div class="mb-6 flex h-16 w-16 items-center justify-center rounded-2xl bg-white shadow-sm text-school-navy transition-all duration-500 group-hover:bg-school-navy group-hover:text-school-gold group-hover:scale-110">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d={subject.icon} />
              </svg>
            </div>
            <h3 class="text-sm font-black text-school-navy tracking-widest uppercase">{subject.name}</h3>
          </div>
        {/each}
      </div>
    </div>
    
  </div>
</section>
