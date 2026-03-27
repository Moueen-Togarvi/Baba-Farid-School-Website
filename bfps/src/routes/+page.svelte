<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
  <title>Home - Baba Farid Public School</title>
</svelte:head>

<!-- Hero Section -->
<section class="relative overflow-hidden bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex flex-col items-center justify-between gap-12 lg:flex-row">
      <!-- Text Content -->
      <div class="z-10 text-center lg:text-left lg:w-1/2">
        <span class="mb-4 inline-block rounded-full bg-school-gold/20 px-4 py-1.5 text-sm font-semibold tracking-wider text-school-navy uppercase ring-1 ring-school-gold/50">
          Admissions Open For 2026
        </span>
        <h1 class="mb-6 text-4xl font-extrabold tracking-tight text-school-navy sm:text-5xl lg:text-6xl">
          <div class="school-name-animate text-school-gold mb-2">Baba Farid Public School</div>
          Shaping the Leaders of Tomorrow
        </h1>
        <p class="mb-10 max-w-2xl text-lg text-slate-600 sm:text-xl lg:mx-0">
          Providing exceptional, <strong class="text-school-navy">100% free</strong> education from Class 1 to 8. Proudly registered with the Punjab Education Foundation (PEF).
        </p>
        
        <div class="flex flex-col items-center justify-center gap-4 sm:flex-row lg:justify-start">
          <Button href="/about" size="lg" variant="outline">Discover More</Button>
        </div>
      </div>

      <!-- Image Content -->
      <div class="relative lg:w-1/2">
        <div class="absolute -left-4 -top-4 h-full w-full rounded-2xl bg-school-gold/10"></div>
        <div class="absolute -bottom-4 -right-4 h-full w-full rounded-2xl bg-school-navy/5"></div>
        <img 
          src="/hero-children.png" 
          alt="Happy school children" 
          class="relative z-10 w-full rounded-2xl shadow-2xl transition-transform hover:scale-[1.02] duration-500"
        />
      </div>
    </div>
  </div>
</section>

<style>
  .school-name-animate {
    animation: float 4s ease-in-out infinite;
    display: inline-block;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }
</style>

<!-- Stats Strip -->
<section class="relative z-20 -mt-10 mb-16">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-2 gap-4 rounded-2xl bg-white p-6 shadow-xl ring-1 ring-slate-200 lg:grid-cols-4 lg:p-8">
      <div class="text-center">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl">350<span class="text-school-gold">+</span></p>
        <p class="mt-2 text-sm font-medium text-slate-500 uppercase tracking-wider">Students</p>
      </div>
      <div class="text-center border-l border-slate-100">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl">15</p>
        <p class="mt-2 text-sm font-medium text-slate-500 uppercase tracking-wider">Teachers</p>
      </div>
      <div class="text-center border-t border-slate-100 pt-6 lg:border-l lg:border-t-0 lg:pt-0">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl">2015</p>
        <p class="mt-2 text-sm font-medium text-slate-500 uppercase tracking-wider">Established</p>
      </div>
      <div class="text-center border-l border-t border-slate-100 pt-6 lg:border-t-0 lg:pt-0">
        <p class="text-3xl font-bold text-school-navy lg:text-4xl">1-8</p>
        <p class="mt-2 text-sm font-medium text-slate-500 uppercase tracking-wider">Classes</p>
      </div>
    </div>
  </div>
</section>

<!-- Free Education Highlight -->
<section class="bg-slate-50 py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="overflow-hidden rounded-3xl bg-school-green text-center shadow-2xl relative">
      <div class="absolute inset-0 bg-gradient-to-br from-school-green via-green-800 to-green-950"></div>
      
      <div class="relative z-10 px-6 py-16 sm:px-12 sm:py-20 lg:px-16">
        <h2 class="mb-4 text-3xl font-bold tracking-tight text-white sm:text-4xl">100% Free Education for All</h2>
        <p class="mx-auto max-w-2xl text-lg text-green-100">
          At Baba Farid Public School, we believe that every child deserves a quality education regardless of their financial background.
        </p>
        
        <div class="mx-auto mt-12 grid max-w-lg grid-cols-1 gap-6 sm:max-w-4xl sm:grid-cols-3">
          <div class="rounded-2xl bg-white/10 p-6 backdrop-blur-sm border border-white/20">
            <div class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-school-gold text-school-navy">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v12m-3-2.818l.879.659c1.171.879 3.07.879 4.242 0 1.172-.879 1.172-2.303 0-3.182C13.536 12.219 12.768 12 12 12c-.725 0-1.45-.22-2.003-.659-1.106-.879-1.106-2.303 0-3.182s2.9-.879 4.006 0l.415.33M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-lg font-bold text-white">No Monthly Fees</h3>
          </div>
          <div class="rounded-2xl bg-white/10 p-6 backdrop-blur-sm border border-white/20">
            <div class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-school-gold text-school-navy">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
              </svg>
            </div>
            <h3 class="text-lg font-bold text-white">Free Books</h3>
          </div>
          <div class="rounded-2xl bg-white/10 p-6 backdrop-blur-sm border border-white/20">
            <div class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-school-gold text-school-navy">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-lg font-bold text-white">Free Admission</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PEF and Principal Section -->
<section class="py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-12 lg:grid-cols-2 lg:gap-16 items-center">
      
      <div>
        <h2 class="text-3xl font-bold text-school-navy">Message from the Principal</h2>
        <div class="mt-4 h-1 w-20 bg-school-gold rounded-full"></div>
        <p class="mt-6 text-lg text-slate-600 leading-relaxed">
          "Welcome to Baba Farid Public School. We are committed to providing a nurturing environment where our students can excel academically, morally, and socially. Through our partnership with the Punjab Education Foundation, we are making quality education accessible to every single child in Fatehwara Sharif without any financial burden on families."
        </p>
        <p class="mt-6 font-bold text-school-navy text-xl">— Ahmad Saeed</p>
        <p class="text-slate-500">Principal & Founder</p>
        
        <div class="mt-8 flex gap-4">
           <Button href="/about" variant="outline">Read Full Story</Button>
        </div>
      </div>
      
      <div class="relative">
        <div class="absolute -left-6 -top-6 h-full w-full rounded-3xl bg-slate-100"></div>
        <div class="absolute -bottom-6 -right-6 h-full w-full rounded-3xl bg-school-gold/20"></div>
        <Card class="relative z-10 flex flex-col items-center justify-center p-12 text-center h-full min-h-[400px]">
           <div class="mb-6 rounded-full bg-school-green/10 p-6">
             <!-- Placeholder PEF Logo icon -->
             <svg class="h-24 w-24 text-school-green" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
               <path stroke-linecap="round" stroke-linejoin="round" d="M12 21v-8.25M15.75 21v-8.25M8.25 21v-8.25M3 9l9-6 9 6m-1.5 12V10.332A48.36 48.36 0 0012 9.75c-2.551 0-5.056.2-7.5.582V21M3 21h18M12 6.75h.008v.008H12V6.75z" />
             </svg>
           </div>
           <h3 class="mb-2 text-2xl font-bold text-school-navy">PEF Registered Partner</h3>
           <p class="text-slate-600 mb-8 max-w-sm">
             We operate in partnership with the Punjab Education Foundation, guaranteeing compliance with provincial educational standards.
           </p>
           <Button href="/pef" variant="primary">Learn about PEF</Button>
        </Card>
      </div>

    </div>
  </div>
</section>

<!-- Quick Links / Explore -->
<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mb-12 text-center">
      <h2 class="text-3xl font-bold text-school-navy">Explore Our School</h2>
      <p class="mt-4 text-slate-600">Find everything you need to know about academic life and activities.</p>
    </div>
    
    <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-4">
      <!-- Card 1 -->
      <a href="/academics" class="group block h-full">
        <Card hover class="h-full flex flex-col text-center border-t-4 border-t-school-navy hover:border-t-school-gold">
          <div class="mx-auto mb-4 mt-2 flex h-14 w-14 items-center justify-center rounded-full bg-slate-100 text-school-navy group-hover:bg-school-gold group-hover:text-white transition-colors">
            <svg class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
            </svg>
          </div>
          <h3 class="mb-2 text-lg font-bold text-slate-900 group-hover:text-school-navy">Academics</h3>
          <p class="text-sm text-slate-500">Curriculum for Class 1 to 8</p>
        </Card>
      </a>
      
      <!-- Card 2 -->
      <a href="/qat-results" class="group block h-full">
        <Card hover class="h-full flex flex-col text-center border-t-4 border-t-school-navy hover:border-t-school-gold">
          <div class="mx-auto mb-4 mt-2 flex h-14 w-14 items-center justify-center rounded-full bg-slate-100 text-school-navy group-hover:bg-school-gold group-hover:text-white transition-colors">
            <svg class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
            </svg>
          </div>
          <h3 class="mb-2 text-lg font-bold text-slate-900 group-hover:text-school-navy">QAT Results</h3>
          <p class="text-sm text-slate-500">Annual academic performance</p>
        </Card>
      </a>
      
      <!-- Card 3 -->
      <a href="/gallery" class="group block h-full">
        <Card hover class="h-full flex flex-col text-center border-t-4 border-t-school-navy hover:border-t-school-gold">
          <div class="mx-auto mb-4 mt-2 flex h-14 w-14 items-center justify-center rounded-full bg-slate-100 text-school-navy group-hover:bg-school-gold group-hover:text-white transition-colors">
            <svg class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
            </svg>
          </div>
          <h3 class="mb-2 text-lg font-bold text-slate-900 group-hover:text-school-navy">Photo Gallery</h3>
          <p class="text-sm text-slate-500">Campus life & memories</p>
        </Card>
      </a>
      
      <!-- Card 4 -->
      <a href="/activities" class="group block h-full">
        <Card hover class="h-full flex flex-col text-center border-t-4 border-t-school-navy hover:border-t-school-gold">
          <div class="mx-auto mb-4 mt-2 flex h-14 w-14 items-center justify-center rounded-full bg-slate-100 text-school-navy group-hover:bg-school-gold group-hover:text-white transition-colors">
            <svg class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <h3 class="mb-2 text-lg font-bold text-slate-900 group-hover:text-school-navy">Activities</h3>
          <p class="text-sm text-slate-500">Events, sports & programs</p>
        </Card>
      </a>
    </div>
  </div>
</section>
