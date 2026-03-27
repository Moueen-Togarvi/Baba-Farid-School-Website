<script lang="ts">
  import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
  <title>About Us - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="relative overflow-hidden bg-white py-24 text-center border-b border-slate-100">
  <div class="absolute inset-0 bg-grid-slate-900/[0.02] [mask-image:linear-gradient(0deg,white,rgba(255,255,255,0.6))]"></div>
  <div class="container relative mx-auto px-4">
    <span class="mb-4 inline-block rounded-full bg-school-gold/10 px-4 py-1.5 text-xs font-bold tracking-widest text-school-gold uppercase ring-1 ring-school-gold/20">
      Our Legacy
    </span>
    <h1 class="text-5xl font-black tracking-tight sm:text-7xl text-school-navy mb-6">About <span class="text-school-gold">Us</span></h1>
    <p class="mx-auto max-w-2xl text-xl text-slate-500 font-light leading-relaxed">Discover the high-impact history and elite mission of Baba Farid Public School.</p>
  </div>
</div>

<section class="relative py-24 lg:py-32 overflow-hidden bg-white">
  <div class="absolute top-0 right-0 -translate-y-1/2 translate-x-1/2 w-[500px] h-[500px] bg-school-navy/5 rounded-full blur-3xl opacity-50"></div>
  <div class="container relative mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mx-auto max-w-4xl text-center">
      <h2 class="text-4xl font-black text-school-navy tracking-tight mb-8">Our History & <span class="text-school-gold">Foundation</span></h2>
      <div class="mx-auto mb-12 h-1.5 w-24 rounded-full bg-gradient-to-r from-school-gold to-school-navy"></div>
      <p class="text-xl leading-relaxed text-slate-600 font-light">
        Established in <strong class="text-school-navy font-bold">2013</strong>, Baba Farid Public School was founded with a singular vision: to make high-quality education accessible to every child in Fatehwara Sharif, Bahawalnagar. Understanding the financial constraints of many families, we set out to build an institution where learning comes first, and money is never a barrier.
      </p>
      <p class="mt-8 text-xl leading-relaxed text-slate-600 font-light">
        Through our steadfast dedication and partnership with the <strong class="text-school-navy font-bold">Punjab Education Foundation (PEF)</strong>, we guarantee 100% free education, free books, and absolutely no hidden fees for all students from Class 1 to Class 8.
      </p>
    </div>
  </div>
</section>

<!-- Mission & Vision -->
<section class="bg-slate-50 py-24 lg:py-32 border-y border-slate-100">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-12 md:grid-cols-2">
      <!-- Mission -->
      <div class="group relative p-1 bg-white rounded-[2.5rem] shadow-xl hover:shadow-2xl transition-all duration-500 overflow-hidden ring-1 ring-slate-200">
        <div class="absolute top-0 right-0 p-8">
           <div class="h-16 w-16 bg-school-navy/5 rounded-full flex items-center justify-center text-school-navy/30 group-hover:scale-110 group-hover:bg-school-navy group-hover:text-school-gold transition-all duration-500">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
              </svg>
           </div>
        </div>
        <div class="p-10 pr-24">
           <h3 class="text-3xl font-black text-school-navy mb-6">Our Mission</h3>
           <p class="text-lg text-slate-500 font-light leading-relaxed">
             To cultivate a supportive, inclusive, and academically rigorous environment where students can thrive unconditionally. We focus on moral development, critical thinking, and equipping students with the essential skills they need for future success.
           </p>
        </div>
      </div>
      
      <!-- Vision -->
      <div class="group relative p-1 bg-white rounded-[2.5rem] shadow-xl hover:shadow-2xl transition-all duration-500 overflow-hidden ring-1 ring-slate-200">
        <div class="absolute top-0 right-0 p-8">
           <div class="h-16 w-16 bg-school-gold/10 rounded-full flex items-center justify-center text-school-gold/50 group-hover:scale-110 group-hover:bg-school-gold group-hover:text-school-navy transition-all duration-500">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
              </svg>
           </div>
        </div>
        <div class="p-10 pr-24">
           <h3 class="text-3xl font-black text-school-navy mb-6">Our Vision</h3>
           <p class="text-lg text-slate-500 font-light leading-relaxed">
             To serve as a beacon of educational excellence in Bahawalnagar, shaping well-rounded leaders of tomorrow who are compassionate, driven, and fully prepared to contribute meaningfully to society.
           </p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Principal's Message -->
<section class="bg-white py-24 lg:py-32">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto overflow-hidden rounded-[3rem] bg-school-navy text-white shadow-[0_50px_100px_-20px_rgba(15,23,42,0.4)] ring-1 ring-white/5">
      <div class="grid items-center lg:grid-cols-5">
        <!-- Image Placeholder -->
        <div class="lg:col-span-2 relative aspect-[3/4] lg:aspect-auto h-full min-h-[400px] overflow-hidden group">
            <div class="absolute inset-0 bg-slate-800 flex items-center justify-center">
                <svg class="h-48 w-48 text-white/5" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd" />
                </svg>
            </div>
            <div class="absolute inset-0 bg-gradient-to-t from-school-navy via-transparent to-transparent opacity-60"></div>
            <div class="absolute bottom-8 left-8">
               <div class="h-1 w-12 bg-school-gold rounded-full mb-2"></div>
               <p class="text-xs font-bold uppercase tracking-[0.3em] text-school-gold/80">Institutional Head</p>
            </div>
        </div>
        
        <div class="p-10 sm:p-16 lg:col-span-3">
          <h2 class="mb-10 text-4xl font-black text-school-gold tracking-tight leading-tight">Elite Leadership<br/><span class="text-white opacity-80">& Ethical Excellence</span></h2>
          <div class="relative">
             <div class="absolute -left-6 top-0 text-7xl font-serif text-school-gold/20 leading-none">“</div>
             <p class="relative z-10 mb-12 text-2xl font-light leading-relaxed text-slate-200">
               "Education is not merely about academics; it is about character building. When we established Baba Farid Public School, we made a promise to the community: no child will be left behind due to a lack of resources. Today, I am incredibly proud of our students' achievements and our dedicated faculty."
             </p>
          </div>
          <div class="flex items-center gap-6 pt-10 border-t border-white/10">
             <div class="h-16 w-16 rounded-2xl bg-white/5 flex items-center justify-center border border-white/10 shadow-inner">
                <svg class="h-8 w-8 text-school-gold" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M13.586 3.586a2 2 0 112.828 2.828l-.793.793-2.828-2.828.793-.793zM11.379 5.793L3 14.172V17h2.828l8.38-8.379-2.83-2.828z" />
                </svg>
             </div>
             <div>
               <h4 class="text-2xl font-black tracking-tight">Ahmad Saeed</h4>
               <p class="text-sm font-bold text-school-gold uppercase tracking-widest">Founder & Principal</p>
             </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
