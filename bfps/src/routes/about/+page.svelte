<script lang="ts">
  import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
  <title>About Us - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl">About Us</h1>
    <p class="mt-4 text-lg text-slate-500">Discover the history and mission of Baba Farid Public School.</p>
  </div>
</div>

<section class="py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mx-auto max-w-4xl text-center">
      <h2 class="text-3xl font-bold text-school-navy">Our History & Foundation</h2>
      <div class="mx-auto mt-4 h-1 w-20 rounded-full bg-school-gold"></div>
      <p class="mt-8 text-lg leading-relaxed text-slate-600">
        Established in <strong>2015</strong>, Baba Farid Public School was founded with a singular vision: to make high-quality education accessible to every child in Fatehwara Sharif, Bahawalnagar. Understanding the financial constraints of many families, we set out to build an institution where learning comes first, and money is never a barrier.
      </p>
      <p class="mt-6 text-lg leading-relaxed text-slate-600">
        Through our steadfast dedication and partnership with the <strong>Punjab Education Foundation (PEF)</strong>, we guarantee 100% free education, free books, and absolutely no hidden fees for all students from Class 1 to Class 8.
      </p>
    </div>
  </div>
</section>

<!-- Mission & Vision -->
<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-8 md:grid-cols-2">
      <!-- Mission -->
      <Card class="flex h-full flex-col border-t-4 border-t-school-green">
        <div class="mb-4 flex h-16 w-16 items-center justify-center rounded-2xl bg-school-green/10 text-school-green">
          <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
          </svg>
        </div>
        <h3 class="mb-4 text-2xl font-bold text-school-navy">Our Mission</h3>
        <p class="text-slate-600 leading-relaxed">
          To cultivate a supportive, inclusive, and academically rigorous environment where students can thrive unconditionally. We focus on moral development, critical thinking, and equipping students with the essential skills they need for future success.
        </p>
      </Card>
      
      <!-- Vision -->
      <Card class="flex h-full flex-col border-t-4 border-t-school-gold">
        <div class="mb-4 flex h-16 w-16 items-center justify-center rounded-2xl bg-school-gold/10 text-school-gold">
          <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
            <path stroke-linecap="round" stroke-linejoin="round" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
          </svg>
        </div>
        <h3 class="mb-4 text-2xl font-bold text-school-navy">Our Vision</h3>
        <p class="text-slate-600 leading-relaxed">
          To serve as a beacon of educational excellence in Bahawalnagar, shaping well-rounded leaders of tomorrow who are compassionate, driven, and fully prepared to contribute meaningfully to society.
        </p>
      </Card>
    </div>
  </div>
</section>

<!-- Principal's Message -->
<section class="py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="overflow-hidden rounded-3xl bg-school-navy text-white shadow-2xl">
      <div class="grid lg:grid-cols-5">
        <!-- Image Placeholder -->
        <div class="bg-gray-800 lg:col-span-2 relative min-h-[300px] flex items-center justify-center">
            <svg class="h-32 w-32 text-gray-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
            </svg>
            <div class="absolute inset-0 bg-school-navy/20"></div>
        </div>
        
        <div class="p-8 sm:p-12 lg:col-span-3 lg:p-16">
          <h2 class="mb-4 text-3xl font-bold text-school-gold">Message from the Principal</h2>
          <p class="mb-8 text-lg leading-relaxed text-slate-300">
            "Education is not merely about academics; it is about character building. When we established Baba Farid Public School, we made a promise to the community: no child will be left behind due to a lack of resources. Today, I am incredibly proud of our students' achievements and our dedicated faculty."
          </p>
          <div class="flex items-center gap-4">
             <div class="h-12 w-1.5 bg-school-gold rounded-full"></div>
             <div>
               <h4 class="text-xl font-bold">Ahmad Saeed</h4>
               <p class="text-sm font-medium text-slate-400">Founder & Principal</p>
             </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
