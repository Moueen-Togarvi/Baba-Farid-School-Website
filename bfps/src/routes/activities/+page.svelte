<script lang="ts">
  import Card from '$lib/components/Card.svelte';
  
  const activities = [
    {
      title: 'Annual Sports Day',
      category: 'Physical Education',
      description: 'A day dedicated to physical fitness, teamwork, and healthy competition leading to the distribution of medals.',
      icon: 'M3.75 13.5l10.5-11.25L12 10.5h8.25L9.75 21.75 12 13.5H3.75z'
    },
    {
      title: 'Quran Recitation Competitions',
      category: 'Religious Studies',
      description: 'Fostering a deep connection with Islamic teachings through Husn-e-Qirat and Naat competitions.',
      icon: 'M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253'
    },
    {
      title: 'Science Fairs',
      category: 'Academics',
      description: 'Encouraging practical application of theoretical knowledge where students present innovative science projects.',
      icon: 'M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z'
    },
    {
      title: 'Tree Plantation Drives',
      category: 'Environment',
      description: 'Teaching students about environmental responsibility through hands-on tree planting activities around Bahawalnagar.',
      icon: 'M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064'
    },
    {
      title: 'National Day Celebrations',
      category: 'Patriotism',
      description: 'Celebrating Pakistan Resolution Day, Independence Day, and Iqbal Day to instill a strong sense of patriotism.',
      icon: 'M3 21v-4m0 0V5a2 2 0 012-2h6.5l1 1H21l-3 6 3 6h-8.5l-1-1H5a2 2 0 00-2 2zm9-13.5V9'
    },
    {
      title: 'Art and Craft Exhibitions',
      category: 'Creative Arts',
      description: 'Providing a platform for students to express their creativity and artistic flair through drawing and crafting.',
      icon: 'M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01'
    }
  ];
</script>

<svelte:head>
  <title>Extracurricular Activities - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">Activities & Life</h1>
    <p class="mt-4 text-lg text-slate-500">Developing well-rounded individuals beyond the classroom.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    
    <div class="mb-12 text-center max-w-3xl mx-auto">
      <h2 class="text-3xl font-bold text-school-navy">Beyond Academics</h2>
      <div class="mx-auto mt-4 h-1 w-20 rounded-full bg-school-gold"></div>
      <p class="mt-6 text-slate-600 text-lg">
        We believe that education goes far beyond textbooks. Our extracurricular programs are designed to discover hidden talents, promote physical health, and build confidence among our students.
      </p>
    </div>

    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      {#each activities as activity}
        <Card hover class="flex h-full flex-col">
          <div class="mb-6 flex h-14 w-14 items-center justify-center rounded-2xl bg-school-gold text-school-navy shadow-sm">
            <svg class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d={activity.icon} />
            </svg>
          </div>
          <span class="mb-2 text-xs font-bold uppercase tracking-wider text-school-green">{activity.category}</span>
          <h3 class="mb-3 text-xl font-bold text-school-navy">{activity.title}</h3>
          <p class="text-slate-600 leading-relaxed max-w-sm">{activity.description}</p>
        </Card>
      {/each}
    </div>

  </div>
</section>
