<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  import Card from '$lib/components/Card.svelte';
  
  let formState = $state<'idle' | 'submitting' | 'success'>('idle');
  
  function handleSubmit(e: Event) {
    e.preventDefault();
    formState = 'submitting';
    
    // Simulate network delay
    setTimeout(() => {
      formState = 'success';
    }, 1500);
  }
</script>

<svelte:head>
  <title>Contact Us - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">Contact Us</h1>
    <p class="mt-4 text-lg text-slate-500">Get in touch for admissions, inquiries, or feedback.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-12 lg:grid-cols-2 lg:gap-20">
      
      <!-- Contact Info -->
      <div class="space-y-12">
        <div>
          <h2 class="text-3xl md:text-5xl font-black text-school-navy tracking-tight mb-6">Let's <span class="text-school-gold">Connect</span></h2>
          <p class="text-lg text-slate-500 font-light leading-relaxed max-w-xl">
            We are here to support your child's educational journey. For immediate assistance, contact our Principal or visit us during school hours.
          </p>
        </div>
        
        <div class="space-y-4">
          <!-- Address -->
          <div class="group flex items-center gap-6 p-8 rounded-[2rem] bg-slate-50 border border-slate-100 hover:bg-white hover:shadow-2xl hover:ring-1 hover:ring-school-gold/20 transition-all duration-500">
            <div class="flex h-16 w-16 shrink-0 items-center justify-center rounded-2xl bg-school-navy text-school-gold shadow-lg group-hover:scale-110 transition-transform">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
              </svg>
            </div>
            <div>
              <h3 class="text-xs font-bold text-school-gold uppercase tracking-[0.2em] mb-1">Our Location</h3>
              <p class="text-lg font-bold text-school-navy">Fatehwara Sharif, Bahawalnagar</p>
              <p class="text-sm text-slate-400">Punjab, Pakistan</p>
            </div>
          </div>
          
          <!-- Phone -->
          <div class="group flex items-center gap-6 p-8 rounded-[2rem] bg-slate-50 border border-slate-100 hover:bg-white hover:shadow-2xl hover:ring-1 hover:ring-school-gold/20 transition-all duration-500">
            <div class="flex h-16 w-16 shrink-0 items-center justify-center rounded-2xl bg-school-gold text-school-navy shadow-lg group-hover:scale-110 transition-transform">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
              </svg>
            </div>
            <div>
              <h3 class="text-xs font-bold text-school-navy uppercase tracking-[0.2em] mb-1">Direct Contact</h3>
              <p class="text-lg font-bold text-school-navy">0300-6937159</p>
              <p class="text-sm text-slate-400">Ahmad Saeed (Principal)</p>
            </div>
          </div>
          
          <!-- Email -->
          <div class="group flex items-center gap-6 p-8 rounded-[2rem] bg-slate-50 border border-slate-100 hover:bg-white hover:shadow-2xl hover:ring-1 hover:ring-school-gold/20 transition-all duration-500">
            <div class="flex h-16 w-16 shrink-0 items-center justify-center rounded-2xl bg-school-navy text-white shadow-lg group-hover:scale-110 transition-transform">
              <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <div>
              <h3 class="text-xs font-bold text-school-gold uppercase tracking-[0.2em] mb-1">Email Inquiry</h3>
              <p class="text-lg font-bold text-school-navy">babafaridast@gmail.com</p>
              <p class="text-sm text-slate-400">Official Correspondence</p>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Contact Form -->
      <div>
         <div class="rounded-[2.5rem] bg-white p-10 shadow-2xl ring-1 ring-slate-100 relative overflow-hidden">
           <div class="absolute -right-20 -top-20 h-64 w-64 bg-school-gold/5 rounded-full blur-3xl"></div>
           <div class="absolute -left-20 -bottom-20 h-64 w-64 bg-school-navy/5 rounded-full blur-3xl"></div>
           
           {#if formState === 'success'}
             <div class="flex h-full flex-col justify-center items-center py-20 text-center animate-in zoom-in duration-500 relative z-10">
               <div class="mb-8 flex h-24 w-24 items-center justify-center rounded-full bg-school-gold text-school-navy shadow-inner">
                 <svg class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="3">
                   <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                 </svg>
               </div>
               <h3 class="mb-4 text-3xl font-black text-school-navy">Message Received!</h3>
               <p class="mb-10 text-slate-500 font-light leading-relaxed">Thank you for reaching out. Our team will contact you shortly.</p>
               <Button onclick={() => formState = 'idle'} variant="primary">Send Another</Button>
             </div>
           {:else}
             <div class="mb-10 relative z-10">
               <h3 class="text-2xl font-black text-school-navy">Send a Message</h3>
               <p class="text-sm text-slate-400 mt-2">Required fields are marked with *</p>
             </div>
             
             <form onsubmit={handleSubmit} class="space-y-6 relative z-10">
               <div class="space-y-4">
                 <div>
                   <label for="name" class="mb-2 block text-xs font-bold uppercase tracking-widest text-slate-500">Full Name *</label>
                   <input type="text" id="name" required class="w-full rounded-2xl border-slate-200 bg-slate-50 px-6 py-4 text-slate-900 focus:border-school-gold focus:ring-school-gold transition-all" placeholder="Enter your name" />
                 </div>
                 
                 <div>
                   <label for="phone" class="mb-2 block text-xs font-bold uppercase tracking-widest text-slate-500">Phone Number *</label>
                   <input type="tel" id="phone" required class="w-full rounded-2xl border-slate-200 bg-slate-50 px-6 py-4 text-slate-900 focus:border-school-gold focus:ring-school-gold transition-all" placeholder="Your contact number" />
                 </div>
                 
                 <div>
                   <label for="message" class="mb-2 block text-xs font-bold uppercase tracking-widest text-slate-500">Message *</label>
                   <textarea id="message" required rows="4" class="w-full rounded-2xl border-slate-200 bg-slate-50 px-6 py-4 text-slate-900 focus:border-school-gold focus:ring-school-gold transition-all" placeholder="How can we help you?"></textarea>
                 </div>
               </div>
               
               <Button type="submit" variant="primary" class="w-full py-5 rounded-2xl shadow-xl hover:shadow-school-navy/20" disabled={formState === 'submitting'}>
                 {#if formState === 'submitting'}
                   <span class="mr-2 inline-block h-5 w-5 animate-spin rounded-full border-2 border-white border-t-transparent"></span>
                   Processing...
                 {:else}
                   Send Message
                 {/if}
               </Button>
             </form>
           {/if}
         </div>
      </div>

    </div>
  </div>
</section>
