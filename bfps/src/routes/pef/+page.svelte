<script lang="ts">
  import Card from '$lib/components/Card.svelte';
</script>

<svelte:head>
  <title>PEF Partnership - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-school-navy py-16 text-center text-white">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl">Our PEF Partnership</h1>
    <p class="mt-4 text-lg text-slate-300">Proudly registered with the Punjab Education Foundation.</p>
  </div>
</div>

<section class="py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-12 lg:grid-cols-2 items-center">
      
      <div>
        <h2 class="text-3xl font-bold text-school-navy">What is PEF?</h2>
        <div class="mt-4 h-1 w-20 rounded-full bg-school-gold"></div>
        <p class="mt-6 text-lg leading-relaxed text-slate-600">
          The <strong>Punjab Education Foundation (PEF)</strong> is an autonomous statutory body established by the Government of Punjab. Its primary objective is to encourage and promote quality education on a non-commercial basis, particularly in less affluent areas.
        </p>
        <p class="mt-6 text-lg leading-relaxed text-slate-600">
          Through public-private partnerships, PEF provides financial assistance to schools like ours, enabling us to offer 100% free education to our students. This program ensures that every child has access to quality education regardless of their socio-economic background.
        </p>
      </div>
      
      <div class="relative">
        <div class="absolute inset-0 -mx-4 -my-4 rounded-3xl bg-school-green/5 lg:-my-8"></div>
        <Card class="relative z-10 p-8 sm:p-12 border-t-4 border-t-school-green">
           <div class="mb-8 flex justify-center">
             <div class="flex h-32 w-32 items-center justify-center rounded-full bg-school-green/10 text-school-green">
               <!-- Placeholder PEF Logo icon -->
               <svg class="h-16 w-16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M12 21v-8.25M15.75 21v-8.25M8.25 21v-8.25M3 9l9-6 9 6m-1.5 12V10.332A48.36 48.36 0 0012 9.75c-2.551 0-5.056.2-7.5.582V21M3 21h18M12 6.75h.008v.008H12V6.75z" />
               </svg>
             </div>
           </div>
           
           <h3 class="mb-4 text-center text-2xl font-bold text-school-navy">Baba Farid Public School is a Proud PEF Partner</h3>
           <ul class="space-y-4">
             <li class="flex items-start gap-3 text-slate-700">
               <svg class="mt-0.5 h-5 w-5 shrink-0 text-school-green" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
               </svg>
               <span>Fully sponsored tuition for all students from Class 1 to 8.</span>
             </li>
             <li class="flex items-start gap-3 text-slate-700">
               <svg class="mt-0.5 h-5 w-5 shrink-0 text-school-green" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
               </svg>
               <span>Free distribution of curriculum textbooks every academic year.</span>
             </li>
             <li class="flex items-start gap-3 text-slate-700">
               <svg class="mt-0.5 h-5 w-5 shrink-0 text-school-green" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                 <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
               </svg>
               <span>Regular Quality Assurance Tests (QAT) to maintain educational standards.</span>
             </li>
           </ul>
        </Card>
      </div>

    </div>
  </div>
</section>
