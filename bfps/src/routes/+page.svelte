<script lang="ts">
  import { onMount } from 'svelte';
  import Button from '$lib/components/Button.svelte';
  import Card from '$lib/components/Card.svelte';

  let typewriterText = $state('');
  let currentPhraseIndex = 0;
  const phrases = [
    'Empowering Minds, Transforming Futures.',
    'Quality Education for Every Child.',
    'A Tradition of Excellence Since 2015.'
  ];

  function typeWriter() {
    let charIndex = 0;
    const interval = setInterval(() => {
      typewriterText = phrases[currentPhraseIndex].slice(0, charIndex + 1);
      charIndex++;
      if (charIndex === phrases[currentPhraseIndex].length) {
        clearInterval(interval);
        setTimeout(() => {
          deleteWriter();
        }, 2000);
      }
    }, 100);
  }

  function deleteWriter() {
    let charIndex = phrases[currentPhraseIndex].length;
    const interval = setInterval(() => {
      typewriterText = phrases[currentPhraseIndex].slice(0, charIndex - 1);
      charIndex--;
      if (charIndex === 0) {
        clearInterval(interval);
        currentPhraseIndex = (currentPhraseIndex + 1) % phrases.length;
        setTimeout(typeWriter, 500);
      }
    }, 50);
  }

  onMount(() => {
    typeWriter();
  });
</script>

<svelte:head>
  <title>Home - Baba Farid Public School</title>
</svelte:head>

<!-- Hero Section -->
<section class="relative overflow-hidden bg-white pt-2 pb-16 lg:pt-4 lg:pb-20">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex flex-col items-center justify-between gap-12 lg:flex-row lg:items-start lg:gap-16">
      <!-- Text Content -->
      <div class="z-10 text-center lg:text-left lg:w-1/2 lg:pt-12">
        <span class="mb-4 inline-block rounded-full bg-slate-50 px-4 py-1.5 text-xs font-bold tracking-widest text-school-gold uppercase ring-1 ring-slate-200">
          Admissions Open For 2026
        </span>
        <h1 class="mb-6 font-extrabold tracking-tight text-school-navy">
          <div class="text-lg font-bold uppercase tracking-[0.2em] text-school-gold/80 mb-4 h-8">
            {typewriterText}<span class="animate-pulse">|</span>
          </div>
          <span class="text-4xl sm:text-5xl lg:text-6xl block mb-2 font-medium text-school-navy/70 tracking-tight">Welcome to</span>
          <span class="text-4xl sm:text-6xl lg:text-7xl block text-school-navy tracking-tighter drop-shadow-sm font-black whitespace-nowrap leading-none">
            Baba Farid <br class="sm:hidden" /> Public School
          </span>
        </h1>
        <p class="mb-10 max-w-2xl text-lg text-slate-500 sm:text-xl lg:mx-0 leading-relaxed font-light">
          Experience a world-class, <strong class="text-school-navy font-bold">100% Free Education</strong> where every student is mentored to achieve their highest potential within an elite academic environment.
        </p>
        
        <div class="flex flex-col items-center justify-center gap-4 sm:flex-row lg:justify-start">
          <Button href="/admissions" size="lg" variant="primary" class="shadow-xl shadow-school-navy/10 min-w-[160px]">Enroll Now</Button>
          <Button href="#about" size="lg" variant="outline" class="min-w-[160px]">Our Legacy</Button>
        </div>
      </div>

      <!-- Hero Image Container -->
      <div class="relative w-full lg:w-1/2 max-w-2xl lg:mt-4">
        <div class="absolute -bottom-6 -right-6 h-full w-full rounded-2xl bg-school-navy/5"></div>
        <div class="relative z-10 overflow-hidden rounded-2xl shadow-2x-strong ring-1 ring-slate-200">
          <img 
            src="/image.png" 
            alt="Baba Farid Public School Campus" 
            class="h-64 sm:h-96 lg:h-[520px] w-full object-cover transition-transform hover:scale-[1.01] duration-500"
          />
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  :global(.shadow-2x-strong) {
    box-shadow: 0 25px 50px -12px rgba(15, 23, 42, 0.25);
  }
</style>

<!-- Stats Strip -->
<section class="relative z-20 -mt-10 mb-16">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-2 gap-4 rounded-2xl bg-white p-6 shadow-xl ring-1 ring-slate-100 lg:grid-cols-4 lg:p-8">
      <div class="text-center group cursor-default">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl group-hover:text-school-gold transition-colors duration-300">350<span class="text-school-gold">+</span></p>
        <p class="mt-2 text-xs font-bold text-slate-400 uppercase tracking-[0.2em]">Enrolled Students</p>
      </div>
      <div class="text-center border-l border-slate-100 group cursor-default">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl group-hover:text-school-gold transition-colors duration-300">15</p>
        <p class="mt-2 text-xs font-bold text-slate-400 uppercase tracking-[0.2em]">Expert Educators</p>
      </div>
      <div class="text-center border-t border-slate-100 pt-6 lg:border-l lg:border-t-0 lg:pt-0 group cursor-default">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl group-hover:text-school-gold transition-colors duration-300">2015</p>
        <p class="mt-2 text-xs font-bold text-slate-400 uppercase tracking-[0.2em]">Year Founded</p>
      </div>
      <div class="text-center border-l border-t border-slate-100 pt-6 lg:border-t-0 lg:pt-0 group cursor-default">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl group-hover:text-school-gold transition-colors duration-300">1-8</p>
        <p class="mt-2 text-xs font-bold text-slate-400 uppercase tracking-[0.2em]">Educational Levels</p>
      </div>
    </div>
  </div>
</section>

<!-- About & Legacy Section -->
<section id="about" class="bg-white py-24 lg:py-32 overflow-hidden">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-16 lg:grid-cols-2 items-center">
      <div class="relative order-2 lg:order-1">
        <div class="absolute -inset-10 bg-school-gold/5 rounded-full blur-3xl opacity-50"></div>
        <div class="relative overflow-hidden rounded-3xl bg-school-navy shadow-2xl p-8 sm:p-12">
            <h4 class="text-xl font-bold text-school-gold uppercase tracking-widest mb-6">Principal's Perspective</h4>
            <p class="text-white/90 text-xl font-light italic leading-relaxed mb-10 border-l-4 border-school-gold pl-6">
              "We established this institution on one simple truth: Education is a right, not a privilege. Our mission is to ensure every child in Bahawalnagar receives an elite education, completely free of charge, with a focus on character and leadership."
            </p>
            <div class="flex items-center gap-4 pt-6 border-t border-white/10">
              <div class="h-14 w-14 rounded-full bg-slate-800 flex items-center justify-center border-2 border-school-gold/30">
                <svg class="h-7 w-7 text-school-gold" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd" />
                </svg>
              </div>
              <div>
                <p class="text-lg font-bold text-white">Ahmad Saeed</p>
                <p class="text-sm font-medium text-school-gold/80">Founder & Principal</p>
              </div>
            </div>
        </div>
      </div>

      <div class="order-1 lg:order-2">
        <div class="flex items-center gap-3 mb-6">
           <div class="h-[1px] w-8 bg-school-gold"></div>
           <span class="text-sm font-bold uppercase tracking-widest text-school-gold">Est. 2015</span>
        </div>
        <h2 class="text-4xl sm:text-5xl lg:text-6xl font-black text-school-navy tracking-tight leading-[1.1] mb-8">
          A Decade of <span class="text-transparent bg-clip-text bg-gradient-to-r from-school-navy to-slate-600">Free Excellence</span>
        </h2>
        <p class="text-lg text-slate-500 leading-relaxed mb-8 font-light">
          Baba Farid Public School is more than just an educational center; it is a community beacon. Registered with the <strong>Punjab Education Foundation (PEF)</strong>, we have spent years refining a curriculum that balances traditional values with modern academic rigor.
        </p>
        
        <div class="grid sm:grid-cols-2 gap-6">
           <div class="p-6 rounded-2xl bg-slate-50 ring-1 ring-slate-100 hover:shadow-lg transition-all border-b-4 border-school-navy">
              <h5 class="font-bold text-school-navy mb-2">Our Mission</h5>
              <p class="text-sm text-slate-500 leading-relaxed">Cultivating a supportive environment where intellectual growth and ethical behavior go hand-in-hand.</p>
           </div>
           <div class="p-6 rounded-2xl bg-slate-50 ring-1 ring-slate-100 hover:shadow-lg transition-all border-b-4 border-school-gold">
              <h5 class="font-bold text-school-navy mb-2">Our Vision</h5>
              <p class="text-sm text-slate-500 leading-relaxed">To transform the educational landscape of Bahawalnagar by proving that free education can be premium quality.</p>
           </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Academic Excellence -->
<section id="academics" class="bg-slate-50 py-24 lg:py-32">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-20">
      <h2 class="text-sm font-bold uppercase tracking-[0.2em] text-school-gold mb-4">Academic Excellence</h2>
      <h3 class="text-4xl sm:text-5xl font-black text-school-navy tracking-tight mb-6">Tailored for Every <span class="text-school-gold">Stage</span></h3>
      <p class="text-lg text-slate-500 font-light">From the first steps in primary education to the advanced concepts of middle school, we provide a structured and supportive path for all students.</p>
    </div>

    <div class="grid md:grid-cols-2 gap-12">
      <!-- Primary Education -->
      <div class="group relative">
        <div class="absolute -inset-4 bg-white rounded-3xl opacity-0 group-hover:opacity-100 transition-all duration-500 shadow-xl ring-1 ring-slate-100"></div>
        <div class="relative z-10 flex flex-col sm:flex-row gap-8 items-center sm:items-start text-center sm:text-left p-6">
          <div class="h-24 w-24 shrink-0 rounded-2xl bg-white shadow-lg flex items-center justify-center text-school-navy border-t-4 border-school-navy group-hover:scale-105 transition-transform duration-500">
             <svg class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
               <path stroke-linecap="round" stroke-linejoin="round" d="M12 21v-8.25M15.75 21v-8.25M8.25 21v-8.25M3 9l9-6 9 6m-1.5 12V10.332A48.36 48.36 0 0012 9.75c-2.551 0-5.056.2-7.5.582V21M3 21h18M12 6.75h.008v.008H12V6.75z" />
             </svg>
          </div>
          <div>
            <h4 class="text-2xl font-bold text-school-navy mb-4">Primary Education (Class 1-5)</h4>
            <p class="text-slate-500 leading-relaxed mb-6 font-light">Building strong foundations in English, Mathematics, Science, and Urdu. We focus on curiosity, literacy, and core values.</p>
            <ul class="space-y-3">
              {#each ['Foundational Literacy & Numeracy', 'Islamic Studies & Character Building', 'Creative Arts & Physical Education'] as item}
                <li class="flex items-center gap-2 text-sm text-slate-600">
                  <svg class="h-4 w-4 text-school-gold" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                  {item}
                </li>
              {/each}
            </ul>
          </div>
        </div>
      </div>

      <!-- Middle School -->
      <div class="group relative">
        <div class="absolute -inset-4 bg-white rounded-3xl opacity-0 group-hover:opacity-100 transition-all duration-500 shadow-xl ring-1 ring-slate-100"></div>
        <div class="relative z-10 flex flex-col sm:flex-row gap-8 items-center sm:items-start text-center sm:text-left p-6">
          <div class="h-24 w-24 shrink-0 rounded-2xl bg-white shadow-lg flex items-center justify-center text-school-navy border-t-4 border-school-gold group-hover:scale-105 transition-transform duration-500">
             <svg class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
               <path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147L12 15l7.74-4.853A4.301 4.301 0 0012 5.25a4.301 4.301 0 00-7.74 4.897zM12 15v5.25m0-5.25L4.26 10.147M12 15l7.74-4.853m-15.48 4.853A4.301 4.301 0 0012 20.25a4.301 4.301 0 007.74-5.25l-7.74 4.853" />
             </svg>
          </div>
          <div>
            <h4 class="text-2xl font-bold text-school-navy mb-4">Middle School (Class 6-8)</h4>
            <p class="text-slate-500 leading-relaxed mb-6 font-light">Transitioning to advanced scientific concepts, computer literacy, and critical thinking to prepare for higher secondary education.</p>
            <ul class="space-y-3">
              {#each ['Advanced Science & Math Curriculum', 'Digital Literacy & Computer Science', 'Leadership & Community Service'] as item}
                <li class="flex items-center gap-2 text-sm text-slate-600">
                  <svg class="h-4 w-4 text-school-navy" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                  </svg>
                  {item}
                </li>
              {/each}
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Free Education Highlight -->
<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="overflow-hidden rounded-3xl bg-white text-center shadow-xl ring-1 ring-slate-200 relative">
      <div class="absolute inset-0 bg-gradient-to-br from-slate-50 to-white"></div>
      
      <div class="relative z-10 px-6 py-16 sm:px-12 sm:py-20 lg:px-16">
        <h2 class="mb-4 text-3xl font-black tracking-tight text-school-navy sm:text-4xl lg:text-5xl">100% Free Education for All</h2>
        <div class="mx-auto mb-6 h-1 w-24 rounded-full bg-school-gold"></div>
        <p class="mx-auto max-w-2xl text-lg text-slate-600">
          At Baba Farid Public School, we believe that every child deserves a quality education regardless of their financial background.
        </p>
        
        <div class="mx-auto mt-12 grid max-w-lg grid-cols-1 gap-6 sm:max-w-4xl sm:grid-cols-3">
          <!-- Feature Card 1 -->
          <div class="rounded-2xl bg-white p-6 shadow-md ring-1 ring-school-green/20 border-t-4 border-t-school-green">
            <div class="mx-auto mb-4 flex h-14 w-14 items-center justify-center rounded-2xl bg-school-green/10 text-school-green">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v12m-3-2.818l.879.659c1.171.879 3.07.879 4.242 0 1.172-.879 1.172-2.303 0-3.182C13.536 12.219 12.768 12 12 12c-.725 0-1.45-.22-2.003-.659-1.106-.879-1.106-2.303 0-3.182s2.9-.879 4.006 0l.415.33M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-school-navy">No Monthly Fees</h3>
          </div>

          <!-- Feature Card 2 -->
          <div class="rounded-2xl bg-white p-6 shadow-md ring-1 ring-school-gold/20 border-t-4 border-t-school-gold">
            <div class="mx-auto mb-4 flex h-14 w-14 items-center justify-center rounded-2xl bg-school-gold/10 text-school-gold">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-school-navy">Free Textbooks</h3>
          </div>

          <!-- Feature Card 3 -->
          <div class="rounded-2xl bg-white p-6 shadow-md ring-1 ring-school-navy/20 border-t-4 border-t-school-navy">
            <div class="mx-auto mb-4 flex h-14 w-14 items-center justify-center rounded-2xl bg-school-navy/10 text-school-navy">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-school-navy">Free Admissions</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- QAT Performance -->
<section id="results" class="bg-white py-24 lg:py-32 border-t border-slate-100">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex flex-col lg:flex-row gap-16 items-center">
      <div class="lg:w-1/3">
        <h2 class="text-sm font-bold uppercase tracking-[0.2em] text-school-gold mb-4">Excellence Verified</h2>
        <h3 class="text-4xl font-black text-school-navy tracking-tight mb-8">Unmatched QAT <span class="text-school-gold">Performance</span></h3>
        <p class="text-slate-500 leading-relaxed font-light mb-8">
          Our annual Quality Assurance Tests (QAT) conducted by PEF consistently place us among the top-performing schools in the region.
        </p>
        <div class="inline-flex items-center gap-3 px-4 py-2 bg-school-gold/5 text-school-gold rounded-full text-sm font-bold border border-school-gold/20">
           <svg class="h-5 w-5 font-bold" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
             <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
           </svg>
           PEF Certified Top Tier
        </div>
      </div>

      <div class="lg:w-2/3 grid grid-cols-2 sm:grid-cols-3 gap-6">
        {#each [
          { year: '2024', rate: '87%', label: 'Current Pass Rate' },
          { year: '2023', rate: '85%', label: 'Performance Peak' },
          { year: '2022', rate: '83%', label: 'Consistent Growth' },
          { year: '2021', rate: '80%', label: 'Resilient Standards' }
        ] as stat}
          <div class="p-8 rounded-3xl bg-white ring-1 ring-slate-100 shadow-sm hover:shadow-xl transition-all duration-500 group border-b-4 border-transparent hover:border-school-gold">
             <p class="text-xs font-bold text-slate-400 uppercase tracking-widest mb-2">{stat.year}</p>
             <p class="text-4xl font-black text-school-navy group-hover:text-school-gold transition-colors">{stat.rate}</p>
             <p class="text-xs font-medium text-slate-500 mt-2">{stat.label}</p>
          </div>
        {/each}
        <div class="col-span-2 sm:col-span-1 p-8 rounded-3xl bg-school-navy text-white shadow-xl flex flex-col justify-center">
           <p class="text-sm font-bold text-school-gold uppercase tracking-widest mb-2">Total Score</p>
           <p class="text-3xl font-black">A+ Grade</p>
           <p class="text-xs text-white/50 mt-2">PEF Rating Matrix</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Our PEF Partnership Spotlight -->
<section class="py-16 bg-slate-50 border-y border-slate-100">
  <div class="container mx-auto px-4 text-center">
    <div class="flex flex-col items-center justify-center gap-8 md:flex-row md:gap-16">
       <div class="flex items-center gap-4">
          <div class="h-16 w-16 rounded-full bg-white shadow-md flex items-center justify-center text-school-navy p-3 border border-slate-100">
             <svg class="h-full w-full" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1">
               <path stroke-linecap="round" stroke-linejoin="round" d="M12 21v-8.25M15.75 21v-8.25M8.25 21v-8.25M3 9l9-6 9 6m-1.5 12V10.332A48.36 48.36 0 0012 9.75c-2.551 0-5.056.2-7.5.582V21M3 21h18M12 6.75h.008v.008H12V6.75z" />
             </svg>
          </div>
          <p class="text-xl font-bold text-school-navy">Proud PEF Partner</p>
       </div>
       <div class="h-px w-24 bg-slate-200 hidden md:block"></div>
       <p class="text-slate-500 max-w-lg">Officially registered institution with the Punjab Education Foundation, ensuring transparent and high-quality free education delivery.</p>
    </div>
  </div>
</section>

<!-- Activities Spotlight -->
<section id="activities" class="bg-white py-24 lg:py-32">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-20">
      <h2 class="text-sm font-bold uppercase tracking-[0.2em] text-school-gold mb-4">Life at School</h2>
      <h3 class="text-4xl sm:text-5xl font-black text-school-navy tracking-tight mb-6">Beyond the <span class="text-school-gold">Classroom</span></h3>
      <p class="text-lg text-slate-500 font-light">We believe in holistic development. Our students participate in various extra-curricular activities to build character and leadership skills.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each [
        { title: 'Annual Sports Gala', desc: 'A tradition of physical fitness and competitive spirit.', icon: 'M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z' },
        { title: 'Quran Competitions', desc: 'Fostering spiritual growth through Hifz and Naat.', icon: 'M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253' },
        { title: 'Science & Art Fairs', desc: 'Encouraging innovation and creative expression.', icon: 'M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z' }
      ] as activity}
        <div class="p-10 rounded-3xl bg-slate-50 ring-1 ring-slate-100 hover:bg-white hover:shadow-2xl transition-all duration-500 group border-t-2 border-transparent hover:border-school-navy">
          <div class="h-16 w-16 rounded-2xl bg-school-navy text-school-gold flex items-center justify-center mb-8 shadow-lg group-hover:scale-110 transition-transform">
             <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
               <path stroke-linecap="round" stroke-linejoin="round" d={activity.icon} />
             </svg>
          </div>
          <h4 class="text-2xl font-bold text-school-navy mb-4">{activity.title}</h4>
          <p class="text-slate-500 leading-relaxed font-light">{activity.desc}</p>
        </div>
      {/each}
    </div>
  </div>
</section>
<!-- Latest News & Blog -->
<section id="blog" class="bg-slate-50 py-24 lg:py-32 border-y border-slate-100">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6">
      <div class="max-w-2xl text-center md:text-left">
        <h2 class="text-sm font-bold uppercase tracking-[0.2em] text-school-gold mb-4">News & Updates</h2>
        <h3 class="text-4xl font-black text-school-navy tracking-tight">Stay Informed with <span class="text-school-gold">Our Journey</span></h3>
      </div>
      <Button href="/blog" variant="outline" class="hidden md:flex">View All News</Button>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each [
        { title: 'Annual Sports Gala 2026', date: 'March 20, 2026', cat: 'Events' },
        { title: 'PEF Inspection Success', date: 'March 10, 2026', cat: 'News' },
        { title: 'New Computer Lab Open', date: 'Feb 28, 2026', cat: 'Announcements' }
      ] as post}
        <div class="group h-full flex flex-col bg-white rounded-3xl overflow-hidden shadow-sm hover:shadow-2xl transition-all duration-500 ring-1 ring-slate-100">
          <div class="bg-slate-200 h-48 w-full relative group-hover:scale-105 transition-transform duration-700">
             <div class="absolute inset-0 bg-school-navy/10"></div>
          </div>
          <div class="p-8 flex flex-col flex-grow">
            <span class="text-[10px] font-bold uppercase tracking-widest text-school-gold mb-3">{post.cat}</span>
            <h4 class="text-xl font-bold text-school-navy mb-4 group-hover:text-school-gold transition-colors">{post.title}</h4>
            <div class="mt-auto flex items-center justify-between pt-6 border-t border-slate-50">
               <span class="text-xs text-slate-400 font-medium">{post.date}</span>
               <span class="text-school-navy text-sm font-bold opacity-0 group-hover:opacity-100 transition-opacity">Read Story →</span>
            </div>
          </div>
        </div>
      {/each}
    </div>
    <div class="mt-12 text-center md:hidden">
      <Button href="/blog" variant="outline" class="w-full">View All News</Button>
    </div>
  </div>
</section>

<!-- Gallery Spotlight -->
<section id="gallery" class="bg-white py-24 lg:py-32">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-20">
      <h2 class="text-sm font-bold uppercase tracking-[0.2em] text-school-gold mb-4">Visual Glimpses</h2>
      <h3 class="text-4xl sm:text-5xl font-black text-school-navy tracking-tight mb-6">Our <span class="text-school-gold">Vibrant</span> Campus</h3>
      <p class="text-lg text-slate-500 font-light">Experience the energy and joy of learning at Baba Farid Public School through our latest photography.</p>
    </div>

    <div class="grid grid-cols-2 lg:grid-cols-4 gap-4 sm:gap-6">
       {#each [1, 2, 3, 4] as i}
         <div class="aspect-[4/5] rounded-3xl bg-slate-100 overflow-hidden ring-1 ring-slate-200 group relative">
            <div class="absolute inset-0 bg-school-navy/20 opacity-0 group-hover:opacity-100 transition-opacity duration-500 z-10"></div>
            <div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all duration-500 z-20 scale-90 group-hover:scale-100">
               <svg class="h-10 w-10 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7" />
               </svg>
            </div>
         </div>
       {/each}
    </div>
    <div class="mt-12 text-center">
       <Button href="/gallery" variant="outline">Explore Gallery</Button>
    </div>
  </div>
</section>

<!-- Contact & Enrollment Hub -->
<section id="contact" class="bg-slate-50 py-24 lg:py-32">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto rounded-[3rem] bg-white shadow-2xl overflow-hidden ring-1 ring-slate-100">
      <div class="grid lg:grid-cols-5">
        <div class="lg:col-span-2 bg-school-navy p-10 sm:p-16 text-white text-center sm:text-left">
           <h4 class="text-3xl font-black text-school-gold mb-6">Start Your Future</h4>
           <p class="text-white/70 font-light mb-12">Submit an inquiry today and our team will get back to you within 24 hours regarding admissions and enrollment.</p>
           
           <div class="space-y-8">
              <div class="flex items-center gap-6 group">
                <div class="h-12 w-12 rounded-2xl bg-white/10 flex items-center justify-center text-school-gold group-hover:bg-school-gold group-hover:text-school-navy transition-all">
                  <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                </div>
                <div>
                   <p class="text-xs font-bold text-white/50 uppercase tracking-widest">WhatsApp Principal</p>
                   <p class="text-lg font-bold">0305-9743641</p>
                </div>
              </div>
              <div class="flex items-center gap-6 group">
                <div class="h-12 w-12 rounded-2xl bg-white/10 flex items-center justify-center text-school-gold group-hover:bg-school-gold group-hover:text-school-navy transition-all">
                  <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                </div>
                <div>
                   <p class="text-xs font-bold text-white/50 uppercase tracking-widest">Visit Campus</p>
                   <p class="text-lg font-bold leading-tight">Fatehwara Sharif, Bahawalnagar</p>
                </div>
              </div>
           </div>
        </div>
        
        <div class="lg:col-span-3 p-10 sm:p-16">
          <form class="grid sm:grid-cols-2 gap-8">
            <div class="space-y-2">
              <label for="name" class="text-xs font-bold uppercase tracking-widest text-slate-400">Full Name</label>
              <input type="text" id="name" placeholder="Child's or Parent's Name" class="w-full bg-slate-50 border-0 rounded-xl px-4 py-4 text-school-navy focus:ring-2 focus:ring-school-navy" />
            </div>
            <div class="space-y-2">
              <label for="phone" class="text-xs font-bold uppercase tracking-widest text-slate-400">Phone / WhatsApp</label>
              <input type="tel" id="phone" placeholder="Contact Number" class="w-full bg-slate-50 border-0 rounded-xl px-4 py-4 text-school-navy focus:ring-2 focus:ring-school-navy" />
            </div>
            <div class="sm:col-span-2 space-y-2">
              <label for="message" class="text-xs font-bold uppercase tracking-widest text-slate-400">Your Inquiry</label>
              <textarea id="message" rows="4" placeholder="How can we help your child excel?" class="w-full bg-slate-50 border-0 rounded-xl px-4 py-4 text-school-navy focus:ring-2 focus:ring-school-navy resize-none"></textarea>
            </div>
            <div class="sm:col-span-2 pt-4">
              <Button size="lg" variant="primary" class="w-full shadow-2xl shadow-school-navy/10">Submit Inquiry</Button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</section>
