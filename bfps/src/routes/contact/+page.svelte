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
<div class="bg-school-navy py-16 text-center text-white">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">Contact Us</h1>
    <p class="mt-4 text-lg text-slate-300">Get in touch for admissions, inquiries, or feedback.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid gap-12 lg:grid-cols-2 lg:gap-16">
      
      <!-- Contact Info -->
      <div>
        <h2 class="text-3xl font-bold text-school-navy">Get In Touch</h2>
        <div class="mt-4 h-1 w-20 rounded-full bg-school-gold mb-8"></div>
        <p class="text-lg text-slate-600 mb-10">We would love to hear from you. For urgent inquiries, please contact Principal Ahmad Saeed directly via WhatsApp or phone call.</p>
        
        <div class="space-y-6">
          <Card class="flex items-start gap-4 p-6">
            <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-full bg-school-gold/20 text-school-gold">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
              </svg>
            </div>
            <div>
              <h3 class="text-lg font-bold text-school-navy">Address</h3>
              <p class="mt-1 text-slate-600">Fatehwara Sharif, Bahawalnagar, Punjab, Pakistan</p>
            </div>
          </Card>
          
          <Card class="flex items-start gap-4 p-6">
            <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-full bg-green-100 text-green-600">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
              </svg>
            </div>
            <div>
              <h3 class="text-lg font-bold text-school-navy">Phone / WhatsApp</h3>
              <p class="mt-1 text-slate-600 font-medium">0300-6937159</p>
              <div class="mt-2 text-school-navy font-bold hover:text-green-600 transition-colors">
                <a href="https://wa.me/923059743641" target="_blank" class="flex items-center gap-2">
                   <img src="/whatsapp.svg" alt="WhatsApp" class="h-5 w-5" />
                   0305-9743641
                </a>
              </div>
            </div>
          </Card>
          
          <Card class="flex items-start gap-4 p-6">
            <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-full bg-blue-100 text-blue-600">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <div>
              <h3 class="text-lg font-bold text-school-navy">Email Address</h3>
              <a href="mailto:babafaridast@gmail.com" class="mt-1 text-slate-600 hover:text-school-navy hover:underline">babafaridast@gmail.com</a>
            </div>
          </Card>
        </div>
      </div>
      
      <!-- Contact Form -->
      <div>
         <Card class="h-full">
           {#if formState === 'success'}
             <div class="flex h-full flex-col justify-center items-center py-16 text-center animate-in fade-in duration-500">
               <div class="mb-4 flex h-16 w-16 items-center justify-center rounded-full bg-green-100 text-green-600">
                 <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                   <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                 </svg>
               </div>
               <h3 class="mb-2 text-xl font-bold text-school-navy">Message Sent Successfully!</h3>
               <p class="mb-8 text-slate-500">We will get back to you as soon as possible.</p>
               <Button onclick={() => formState = 'idle'} variant="outline">Send Another Message</Button>
             </div>
           {:else}
             <div class="border-b border-slate-100 px-8 py-6">
               <h3 class="text-xl font-bold text-school-navy">Send us a Message</h3>
             </div>
             
             <form onsubmit={handleSubmit} class="space-y-6 px-8 py-6">
               <div class="space-y-4">
                 <div>
                   <label for="name" class="mb-1.5 block text-sm font-medium text-slate-700">Full Name *</label>
                   <input type="text" id="name" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="Your name" />
                 </div>
                 
                 <div>
                   <label for="phone" class="mb-1.5 block text-sm font-medium text-slate-700">Phone Number *</label>
                   <input type="tel" id="phone" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="Your contact number" />
                 </div>
                 
                 <div>
                   <label for="message" class="mb-1.5 block text-sm font-medium text-slate-700">Message *</label>
                   <textarea id="message" required rows="4" class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="How can we help you?"></textarea>
                 </div>
               </div>
               
               <Button type="submit" variant="primary" class="w-full" disabled={formState === 'submitting'}>
                 {#if formState === 'submitting'}
                   <span class="mr-2 inline-block h-4 w-4 animate-spin rounded-full border-2 border-school-navy border-t-transparent"></span>
                   Sending...
                 {:else}
                   Send Message
                 {/if}
               </Button>
             </form>
           {/if}
         </Card>
      </div>

    </div>
  </div>
</section>
