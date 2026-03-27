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
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl">Our Academics</h1>
    <p class="mt-4 text-lg text-slate-500">A comprehensive curriculum from Class 1 to 8 designed for holistic growth.</p>
  </div>
</div>

<section class="py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    
    <!-- Primary & Middle Sections -->
    <div class="grid gap-12 lg:grid-cols-2">
      <!-- Primary -->
      <Card class="border-t-4 border-t-school-gold">
        <h2 class="text-2xl font-bold text-school-navy">Primary Classes</h2>
        <span class="mt-1 inline-block text-sm font-semibold uppercase tracking-wider text-school-gold">Class 1 to 5</span>
        <div class="mt-6 space-y-4 text-slate-600">
           <p>Our primary section focuses on building a strong foundational base in literacy and numeracy. We encourage curiosity and active learning.</p>
           <ul class="list-inside list-disc space-y-2 marker:text-school-gold">
             <li>Basic language skills in English and Urdu</li>
             <li>Foundational Mathematics concepts</li>
             <li>Introduction to General Science and Islamiat</li>
             <li>Interactive learning and regular assessments</li>
           </ul>
        </div>
      </Card>
      
      <!-- Middle -->
      <Card class="border-t-4 border-t-school-navy">
        <h2 class="text-2xl font-bold text-school-navy">Middle Classes</h2>
        <span class="mt-1 inline-block text-sm font-semibold uppercase tracking-wider text-school-navy">Class 6 to 8</span>
        <div class="mt-6 space-y-4 text-slate-600">
           <p>The middle school curriculum expands upon the foundational knowledge, introducing more complex concepts and critical thinking exercises.</p>
           <ul class="list-inside list-disc space-y-2 marker:text-school-gold">
             <li>Advanced scientific principles and experiments</li>
             <li>In-depth Mathematical problem solving</li>
             <li>Comprehensive Language Arts and Literature</li>
             <li>Preparation for Matriculation requirements</li>
           </ul>
        </div>
      </Card>
    </div>

    <!-- Core Subjects -->
    <div class="mt-20">
      <div class="mb-10 text-center">
        <h2 class="text-3xl font-bold text-school-navy">Core Subjects</h2>
        <p class="mt-3 text-slate-600">The subjects forming the foundation of our Punjab Education Foundation approved curriculum.</p>
      </div>
      
      <div class="grid grid-cols-2 gap-4 sm:grid-cols-3 lg:gap-8">
        {#each subjects as subject}
          <div class="group flex flex-col items-center rounded-2xl bg-white p-6 text-center transition-all hover:-translate-y-1 hover:bg-white hover:shadow-lg hover:ring-1 hover:ring-slate-200">
            <div class="mb-4 flex h-16 w-16 items-center justify-center rounded-full bg-school-navy/5 text-school-navy transition-colors group-hover:bg-school-navy group-hover:text-school-gold">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d={subject.icon} />
              </svg>
            </div>
            <h3 class="font-bold text-slate-900 group-hover:text-school-navy">{subject.name}</h3>
          </div>
        {/each}
      </div>
    </div>
    
  </div>
</section>
