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
<div class="bg-school-navy py-16 text-center text-white">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">News & Updates</h1>
    <p class="mt-4 text-lg text-slate-300">Stay informed with the latest happenings at Baba Farid Public School.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
      {#each posts as post}
        <Card hover class="flex flex-col h-full">
          <div class="mb-4">
            <span class="inline-block rounded-full bg-slate-100 px-3 py-1 text-xs font-semibold uppercase tracking-wide text-school-navy">
              {post.category}
            </span>
          </div>
          <h2 class="mb-2 text-xl font-bold text-slate-900 line-clamp-2">{post.title}</h2>
          <p class="mb-4 text-sm text-slate-500">
            <time>{post.date}</time>
          </p>
          <p class="mb-6 flex-grow text-slate-600 line-clamp-3">
            {post.excerpt}
          </p>
          <button class="mt-auto self-start border-b-2 border-school-gold pb-0.5 text-sm font-bold text-school-navy transition-colors hover:text-school-gold">
            Read Full Story &rarr;
          </button>
        </Card>
      {/each}
    </div>
  </div>
</section>
