<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  import Card from '$lib/components/Card.svelte';
  
  let formState = $state<'idle' | 'submitting' | 'success'>('idle');
  
  function handleSubmit(e: Event) {
    e.preventDefault();
    formState = 'submitting';
    
    // Simulate network request
    setTimeout(() => {
      formState = 'success';
    }, 1500);
  }
</script>

<svelte:head>
  <title>Free Admissions - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">100% Free Admissions</h1>
    <p class="mt-4 text-lg text-slate-500">No monthly fees, no book charges, no hidden costs.</p>
  </div>
</div>

<section class="py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    
    <div class="grid gap-12 lg:grid-cols-5 lg:gap-16">
      
      <!-- Eligibility / Info (Left Col) -->
      <div class="space-y-8 lg:col-span-2">
        <div>
          <h2 class="text-3xl font-bold text-school-navy">Join Our School</h2>
          <div class="mt-4 h-1 w-20 rounded-full bg-school-gold"></div>
          <p class="mt-6 text-slate-600">
            Enrolling your child at Baba Farid Public School is completely free. Thanks to the PEF program, we ensure your child receives the best education without the financial burden.
          </p>
        </div>
        
        <div class="rounded-2xl bg-white p-6 ring-1 ring-slate-200">
          <h3 class="mb-4 font-bold text-school-navy flex items-center gap-2">
             <svg class="h-6 w-6 text-school-green" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
               <path stroke-linecap="round" stroke-linejoin="round" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
             </svg>
             Admission Requirements
          </h3>
          <ul class="space-y-3 text-sm text-slate-700">
            <li class="flex items-start gap-2">
              <svg class="h-5 w-5 text-school-gold shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Copy of student's B-Form
            </li>
            <li class="flex items-start gap-2">
              <svg class="h-5 w-5 text-school-gold shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Parents' CNIC copies
            </li>
            <li class="flex items-start gap-2">
              <svg class="h-5 w-5 text-school-gold shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Previous school leaving certificate (if applicable)
            </li>
            <li class="flex items-start gap-2">
              <svg class="h-5 w-5 text-school-gold shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              2 Passport size photographs
            </li>
          </ul>
        </div>
        
        <div class="rounded-2xl bg-white p-6 text-sm text-slate-700 border border-slate-200 shadow-sm ring-1 ring-slate-100">
          <strong>Questions about admission?</strong> Feel free to WhatsApp Principal Ahmad Saeed directly at <a href="https://wa.me/923059743641" class="font-bold underline text-school-navy hover:text-school-green transition-colors">0305-9743641</a>.
        </div>
      </div>
      
      <!-- Admission Form (Right Col) -->
      <div class="lg:col-span-3">
        <Card class="relative overflow-hidden">
          {#if formState === 'success'}
            <div class="flex flex-col items-center justify-center py-16 text-center animate-in fade-in duration-500">
              <div class="mb-6 flex h-20 w-20 items-center justify-center rounded-full bg-green-100 text-green-600">
                <svg class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
                </svg>
              </div>
              <h3 class="mb-2 text-2xl font-bold text-slate-900">Application Submitted!</h3>
              <p class="mb-8 max-w-sm text-slate-500">Thank you for applying to Baba Farid Public School. We will contact you at the provided phone number shortly.</p>
              <Button onclick={() => formState = 'idle'} variant="outline">Submit Another Application</Button>
            </div>
          {:else}
            <div class="border-b border-slate-100 px-8 py-6">
              <h2 class="text-xl font-bold text-school-navy">Online Admission Form</h2>
              <p class="text-sm text-slate-500 mt-1">Fill out the details completely to start the enrollment process.</p>
            </div>
            
            <form onsubmit={handleSubmit} class="space-y-6 px-8 py-6">
              <div class="grid gap-6 sm:grid-cols-2">
                <div>
                  <label for="studentName" class="mb-1.5 block text-sm font-medium text-slate-700">Student's Full Name *</label>
                  <input type="text" id="studentName" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="e.g. Ali Raza" />
                </div>
                <div>
                  <label for="fatherName" class="mb-1.5 block text-sm font-medium text-slate-700">Father's Name *</label>
                  <input type="text" id="fatherName" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="Father's Name" />
                </div>
                
                <div>
                  <label for="dob" class="mb-1.5 block text-sm font-medium text-slate-700">Date of Birth *</label>
                  <input type="date" id="dob" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" />
                </div>
                <div>
                  <label for="classApplying" class="mb-1.5 block text-sm font-medium text-slate-700">Class Applying For *</label>
                  <select id="classApplying" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm">
                    <option value="">Select a class</option>
                    <option value="1">Class 1</option>
                    <option value="2">Class 2</option>
                    <option value="3">Class 3</option>
                    <option value="4">Class 4</option>
                    <option value="5">Class 5</option>
                    <option value="6">Class 6</option>
                    <option value="7">Class 7</option>
                    <option value="8">Class 8</option>
                  </select>
                </div>
                
                <div>
                  <label for="phone" class="mb-1.5 block text-sm font-medium text-slate-700">Contact Number (WhatsApp) *</label>
                  <input type="tel" id="phone" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="03xx-xxxxxxx" />
                </div>
                <div>
                  <label for="prevSchool" class="mb-1.5 block text-sm font-medium text-slate-700">Previous School (if any)</label>
                  <input type="text" id="prevSchool" class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="Optional" />
                </div>
                
                <div class="sm:col-span-2">
                  <label for="address" class="mb-1.5 block text-sm font-medium text-slate-700">Home Address *</label>
                  <input type="text" id="address" required class="w-full rounded-lg border-slate-300 px-4 py-2.5 text-slate-900 focus:border-school-navy focus:ring-school-navy sm:text-sm" placeholder="Street, Sector/Area, Bahawalnagar" />
                </div>
              </div>
              
              <div class="pt-4">
                <Button type="submit" variant="primary" class="w-full sm:w-auto" disabled={formState === 'submitting'}>
                  {#if formState === 'submitting'}
                    <span class="mr-2 inline-block h-4 w-4 animate-spin rounded-full border-2 border-school-navy border-t-transparent"></span>
                    Submitting...
                  {:else}
                    Submit Admission Form
                  {/if}
                </Button>
                <p class="mt-4 text-xs text-slate-400">By submitting this form, you acknowledge that admissions at Baba Farid Public School are completely free of charge under the PEF program.</p>
              </div>
            </form>
          {/if}
        </Card>
      </div>

    </div>
    
  </div>
</section>
