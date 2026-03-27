<script lang="ts">
  const currentYear = new Date().getFullYear();
</script>

<footer class="bg-slate-900 text-slate-300">
  <div class="container mx-auto px-4 py-12 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 gap-12 md:grid-cols-2 lg:grid-cols-4 text-center sm:text-left">
      
      <!-- School Info -->
      <div class="space-y-4 flex flex-col items-center sm:items-start">
        <div class="flex items-center gap-4 mb-4">
          <img src="/image-removebg-preview.png" alt="Logo" class="h-16 w-auto brightness-110" />
          <h3 class="text-xl font-black tracking-tight text-white leading-tight">Baba Farid<br/><span class="text-school-gold">Public School</span></h3>
        </div>
        <p class="text-sm leading-relaxed text-slate-400 pt-2 max-w-xs mx-auto sm:mx-0">
          Providing high-quality, 100% free education from Class 1 to 8 in Fatehwara Sharif.
        </p>
        <div class="mt-6 flex items-center gap-3 rounded-xl border border-school-gold/30 bg-school-gold/5 p-4 ring-1 ring-white/5 w-full max-w-[240px] justify-center sm:justify-start">
          <div class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-school-gold/20 text-school-gold shadow-sm">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" class="h-6 w-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75L11.25 15 15 9.75M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <div class="text-left">
            <p class="text-[10px] font-bold uppercase tracking-widest text-school-gold">Excellence Verified</p>
            <p class="text-sm font-bold text-white">PEF REGISTERED</p>
          </div>
        </div>
      </div>

      <!-- Quick Links -->
      <div class="flex flex-col items-center sm:items-start">
        <h3 class="mb-4 text-sm font-bold uppercase tracking-wider text-white border-b border-school-gold/30 pb-1 inline-block">Quick Links</h3>
        <ul class="space-y-3 text-sm">
          <li><a href="/about" class="transition-colors hover:text-school-gold">About Us</a></li>
          <li><a href="/academics" class="transition-colors hover:text-school-gold">Academics</a></li>
          <li><a href="/admissions" class="transition-colors hover:text-school-gold">Free Admissions</a></li>
          <li><a href="/pef" class="transition-colors hover:text-school-gold">PEF Partnership</a></li>
          <li><a href="/gallery" class="transition-colors hover:text-school-gold">Photo Gallery</a></li>
        </ul>
      </div>

      <!-- Resources -->
      <div class="flex flex-col items-center sm:items-start">
        <h3 class="mb-4 text-sm font-bold uppercase tracking-wider text-white border-b border-school-gold/30 pb-1 inline-block">Resources</h3>
        <ul class="space-y-3 text-sm">
          <li><a href="/check-result" class="transition-colors hover:text-school-gold">Check Result</a></li>
          <li><a href="/qat-results" class="transition-colors hover:text-school-gold">QAT Performance</a></li>
          <li><a href="/calendar" class="transition-colors hover:text-school-gold">Academic Calendar</a></li>
          <li><a href="/blog" class="transition-colors hover:text-school-gold">News & Blog</a></li>
        </ul>
      </div>

      <!-- Contact Info -->
      <div class="flex flex-col items-center sm:items-start">
        <h3 class="mb-4 text-sm font-bold uppercase tracking-wider text-white border-b border-school-gold/30 pb-1 inline-block">Contact Us</h3>
        <ul class="space-y-4 text-sm flex flex-col items-center sm:items-start">
          <li class="flex items-start gap-3 justify-center sm:justify-start">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" class="mt-0.5 h-5 w-5 text-school-gold shrink-0">
              <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
            </svg>
            <span class="max-w-[200px]">Fatehwara Sharif, Bahawalnagar, Punjab, Pakistan</span>
          </li>
          <li class="flex items-center gap-3">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" class="h-5 w-5 text-school-gold shrink-0">
              <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.864-1.04l-3.202-.462a1.125 1.125 0 00-1.121.365l-1.55 1.55a13.5 13.5 0 01-6.73-6.73l1.55-1.55a1.125 1.125 0 00.365-1.121l-.462-3.202a1.125 1.125 0 00-1.04-.864H4.5a2.25 2.25 0 00-2.25 2.25z" />
            </svg>
            <span>0300-6937159</span>
          </li>
          <li class="flex items-center gap-3 hover:text-white transition-colors">
            <img src="/whatsapp.svg" alt="WhatsApp" class="h-5 w-5 sepia mix-blend-screen" />
            <a href="https://wa.me/923059743641" target="_blank">0305-9743641 (WhatsApp)</a>
          </li>
          <li class="flex items-center gap-3 hover:text-white transition-colors">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5" class="h-5 w-5 text-school-gold shrink-0">
              <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
            </svg>
            <a href="mailto:babafaridast@gmail.com">babafaridast@gmail.com</a>
          </li>
        </ul>
        
        <div class="mt-6 flex space-x-4 justify-center sm:justify-start">
          <a href="https://web.facebook.com/ahmadsaeedtogarvi" target="_blank" class="text-slate-400 hover:text-[#1877F2] transition-colors">
            <span class="sr-only">Facebook</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
              <path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" />
            </svg>
          </a>
        </div>
      </div>

    </div>
    
    <div class="mt-12 border-t border-slate-800 pt-8 flex flex-col items-center justify-between gap-4 md:flex-row text-center md:text-left">
      <p class="text-xs sm:text-sm text-slate-500">
        &copy; {currentYear} Baba Farid Public School. All rights reserved.
      </p>
      <p class="text-xs sm:text-sm text-slate-500 italic opacity-60">
        Created for Principal Ahmad Saeed
      </p>
    </div>
  </div>
</footer>
