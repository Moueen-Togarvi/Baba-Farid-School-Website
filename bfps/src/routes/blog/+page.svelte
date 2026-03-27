<script lang="ts">
  import Card from '$lib/components/Card.svelte';
  
  const posts = [
    {
      id: 1,
      title: 'Annual Sports Gala 2026 Concludes',
      date: 'March 20, 2026',
      excerpt: 'The three-day annual sports gala ended with a spectacular closing ceremony. Students from all classes participated with unmatched enthusiasm.',
      category: 'Events'
    },
    {
      id: 2,
      title: 'PEF Inspection Team Visits School',
      date: 'March 10, 2026',
      excerpt: 'A delegation from the Punjab Education Foundation visited to review our facilities and academic progress, expressing satisfaction with our standards.',
      category: 'News'
    },
    {
      id: 3,
      title: 'New Computer Lab Inaugurated',
      date: 'February 28, 2026',
      excerpt: 'To ensure our students are ready for the digital age, we have officially inaugurated a newly equipped computer lab for middle school students.',
      category: 'Announcements'
    },
    {
      id: 4,
      title: 'Parent-Teacher Meeting Schedule',
      date: 'February 15, 2026',
      excerpt: 'The first Parent-Teacher Meeting of the academic year is scheduled for next week. Parents are requested to ensure attendance.',
      category: 'Notices'
    }
  ];
</script>

<svelte:head>
  <title>News & Blog - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="relative overflow-hidden bg-white py-24 text-center border-b border-slate-100">
  <div class="absolute inset-0 bg-grid-slate-900/[0.02] [mask-image:linear-gradient(0deg,white,rgba(255,255,255,0.6))]"></div>
  <div class="container relative mx-auto px-4">
    <span class="mb-4 inline-block rounded-full bg-school-gold/10 px-4 py-1.5 text-xs font-bold tracking-widest text-school-gold uppercase ring-1 ring-school-gold/20">
      Academic Blog
    </span>
    <h1 class="text-5xl font-black tracking-tight sm:text-7xl text-school-navy mb-6">News & <span class="text-school-gold">Updates</span></h1>
    <p class="mx-auto max-w-2xl text-xl text-slate-500 font-light leading-relaxed">Stay informed with the latest happenings, milestones, and daily life at Baba Farid Public School.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-10 md:grid-cols-2 lg:grid-cols-3">
      {#each posts as post}
        <div class="group h-full flex flex-col bg-white rounded-[2rem] overflow-hidden shadow-sm hover:shadow-2xl transition-all duration-500 ring-1 ring-slate-100 hover:ring-school-gold/20">
          <div class="bg-slate-100 h-56 w-full relative overflow-hidden group-hover:scale-105 transition-transform duration-700">
             <div class="absolute inset-0 bg-school-navy/10"></div>
             <div class="absolute inset-0 flex items-center justify-center opacity-30">
                <svg class="h-16 w-16 text-school-navy" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10l4 4v10a2 2 0 01-2 2z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M14 2v4a2 2 0 002 2h4" />
                </svg>
             </div>
          </div>
          
          <div class="p-8 flex flex-col flex-grow">
            <div class="flex items-center justify-between mb-4">
               <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-school-gold bg-school-gold/5 px-3 py-1 rounded-full border border-school-gold/10">{post.category}</span>
               <span class="text-[10px] font-medium text-slate-400 uppercase tracking-widest">{post.date}</span>
            </div>
            
            <h2 class="text-2xl font-black text-school-navy mb-4 group-hover:text-school-gold transition-colors leading-tight">{post.title}</h2>
            
            <p class="text-slate-500 font-light leading-relaxed mb-8 line-clamp-3">
              {post.excerpt}
            </p>
            
            <button class="mt-auto flex items-center gap-2 group/btn text-sm font-bold text-school-navy">
               <span class="relative">
                 Read Full Story
                 <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-school-gold transition-all duration-300 group-hover/btn:w-full"></span>
               </span>
               <svg class="h-4 w-4 transform group-hover/btn:translate-x-1 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M17 8l4 4m0 0l-4 4m4-4H3" />
               </svg>
            </button>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
