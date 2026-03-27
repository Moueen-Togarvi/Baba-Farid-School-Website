<script lang="ts">
  import Card from '$lib/components/Card.svelte';
  
  // Placeholder images - using simple colored blocks in SVG format to simulate photos
  const images = [
    { id: 1, title: 'Annual Day Celebrations', category: 'Events', color: 'bg-school-navy' },
    { id: 2, title: 'Computer Lab Session', category: 'Academics', color: 'bg-slate-800' },
    { id: 3, title: 'Campus View', category: 'Infrastructure', color: 'bg-school-navy' },
    { id: 4, title: 'Science Exhibition', category: 'Events', color: 'bg-slate-800' },
    { id: 5, title: 'Sports Gala Final', category: 'Sports', color: 'bg-school-navy' },
    { id: 6, title: 'Morning Assembly', category: 'Daily Life', color: 'bg-slate-800' },
    { id: 7, title: 'Library Reading Time', category: 'Academics', color: 'bg-school-navy' },
    { id: 8, title: 'Tree Plantation', category: 'Events', color: 'bg-slate-800' },
  ];
  
  let selectedImage = $state<number | null>(null);

  function openLightbox(id: number) {
    selectedImage = id;
    document.body.style.overflow = 'hidden';
  }

  function closeLightbox() {
    selectedImage = null;
    document.body.style.overflow = 'auto';
  }
</script>

<svelte:head>
  <title>Photo Gallery - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="relative overflow-hidden bg-white py-24 text-center border-b border-slate-100">
  <div class="absolute inset-0 bg-grid-slate-900/[0.02] [mask-image:linear-gradient(0deg,white,rgba(255,255,255,0.6))]"></div>
  <div class="container relative mx-auto px-4">
    <span class="mb-4 inline-block rounded-full bg-school-gold/10 px-4 py-1.5 text-xs font-bold tracking-widest text-school-gold uppercase ring-1 ring-school-gold/20">
      Visual Journey
    </span>
    <h1 class="text-5xl font-black tracking-tight sm:text-7xl text-school-navy mb-6">Photo <span class="text-school-gold">Gallery</span></h1>
    <p class="mx-auto max-w-2xl text-xl text-slate-500 font-light leading-relaxed">Glimpses of life, excellence, and ethical growth at Baba Farid Public School.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-6 sm:grid-cols-2md:grid-cols-3 lg:grid-cols-4">
      <!-- To use real photos, replace the colored divs inside this loop with \`<img src="/path/to/img" />\` -->
      {#each images as image}
        <button 
          class="group relative aspect-square w-full overflow-hidden rounded-2xl shadow-sm transition-all focus:outline-none focus:ring-4 focus:ring-school-gold hover:shadow-xl hover:-translate-y-1"
          onclick={() => openLightbox(image.id)}
          aria-label={"View " + image.title}
        >
          <!-- Placeholder Image -->
          <div class="h-full w-full {image.color} flex items-center justify-center transition-transform duration-500 group-hover:scale-105">
             <svg class="h-12 w-12 text-white/30" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
             </svg>
          </div>
          
          <!-- Overlay -->
          <div class="absolute inset-x-0 bottom-0 bg-gradient-to-t from-black/80 via-black/40 to-transparent p-4 pt-12 text-left opacity-0 transition-opacity duration-300 group-hover:opacity-100">
            <p class="text-xs font-semibold uppercase tracking-wider text-school-gold">{image.category}</p>
            <h3 class="mt-1 text-lg font-bold text-white leading-tight">{image.title}</h3>
          </div>
        </button>
      {/each}
    </div>
  </div>
</section>

<!-- Lightbox Modal -->
{#if selectedImage !== null}
  <!-- svelte-ignore a11y_click_events_have_key_events -->
  <!-- svelte-ignore a11y_no_noninteractive_element_interactions -->
  <div 
    class="fixed inset-0 z-[100] flex items-center justify-center bg-black/90 p-4 backdrop-blur-sm animate-in fade-in duration-200"
    role="dialog"
    aria-modal="true"
    tabindex="-1"
    onclick={closeLightbox}
  >
    <button class="absolute right-6 top-6 rounded-full bg-white/10 p-2 text-white hover:bg-white/20 focus:outline-none" aria-label="Close Gallery" onclick={closeLightbox}>
      <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
      </svg>
    </button>
    
    <div 
      class="relative aspect-video w-full max-w-5xl overflow-hidden rounded-2xl {images.find(i => i.id === selectedImage)?.color}"
      role="presentation"
      onclick={(e) => e.stopPropagation()}
    >
       <div class="absolute inset-0 flex items-center justify-center">
         <div class="text-center text-white">
           <svg class="mx-auto mb-4 h-24 w-24 opacity-30" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
           </svg>
           <h2 class="text-3xl font-bold">{images.find(i => i.id === selectedImage)?.title}</h2>
           <p class="mt-2 text-white/70">Placeholder image. Add real photos to src/lib/data and link them.</p>
         </div>
       </div>
    </div>
  </div>
{/if}
