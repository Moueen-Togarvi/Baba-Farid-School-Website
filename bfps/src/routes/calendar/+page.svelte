<script lang="ts">
  import Card from '$lib/components/Card.svelte';
  
  const calendarEvents = [
    { date: 'March 1, 2026', type: 'academic', title: 'New Academic Session Begins', desc: 'Welcome back to school! First day of classes for all grades.' },
    { date: 'March 23, 2026', type: 'holiday', title: 'Pakistan Day', desc: 'School closed in observance of Pakistan Resolution Day.' },
    { date: 'April 15, 2026', type: 'exam', title: 'First Term Exams Begin', desc: 'Term 1 examinations for all primary and middle classes.' },
    { date: 'May 5, 2026', type: 'result', title: 'First Term Result Day', desc: 'Parent-Teacher meeting and result distribution.' },
    { date: 'June 1 - Aug 15', type: 'holiday', title: 'Summer Vacations', desc: 'School closed for summer break.' },
    { date: 'September 10, 2026', type: 'exam', title: 'PEF QAT Exams', desc: 'Annual Quality Assurance Test conducted by PEF.' },
    { date: 'November 20, 2026', type: 'event', title: 'Annual Sports Gala', desc: 'Three days of sports and athletics competitions.' },
    { date: 'December 10, 2026', type: 'exam', title: 'Final Term Exams Begin', desc: 'End of year examinations.' },
    { date: 'December 30, 2026', type: 'result', title: 'Annual Result Day', desc: 'Final results and awards ceremony.' }
  ];

  function getTypeStyles(type: string) {
    switch (type) {
      case 'academic': return 'bg-blue-100 text-blue-700 ring-blue-500/20';
      case 'exam': return 'bg-red-100 text-red-700 ring-red-500/20';
      case 'result': return 'bg-school-gold/20 text-school-navy ring-school-gold/30';
      case 'holiday': return 'bg-amber-100 text-amber-700 ring-amber-500/20';
      case 'event': return 'bg-purple-100 text-purple-700 ring-purple-500/20';
      default: return 'bg-slate-100 text-slate-700 ring-slate-500/20';
    }
  }

  function getTypeLabel(type: string) {
    return type.charAt(0).toUpperCase() + type.slice(1);
  }
</script>

<svelte:head>
  <title>Academic Calendar - Baba Farid Public School</title>
</svelte:head>

<!-- Header Banner -->
<div class="bg-white py-16 text-center text-school-navy border-b border-slate-100">
  <div class="container mx-auto px-4">
    <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl text-school-gold">Academic Calendar</h1>
    <p class="mt-4 text-lg text-slate-500">Important dates for exams, results, holidays, and events.</p>
  </div>
</div>

<section class="bg-white py-16 lg:py-24">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mx-auto max-w-4xl">
      
      <div class="mb-10 text-center">
        <h2 class="text-3xl font-bold text-school-navy">Session 2026 - 2027</h2>
        <div class="mx-auto mt-4 h-1 w-20 rounded-full bg-school-gold"></div>
        <p class="mt-4 text-slate-600 mb-8">Please note that dates are subject to change based on government notifications or PEF directives.</p>
        
        <!-- Legend -->
        <div class="flex flex-wrap justify-center gap-3">
          {#each ['academic', 'exam', 'result', 'holiday', 'event'] as type}
            <span class="inline-flex items-center rounded-md px-2.5 py-1 text-xs font-medium ring-1 ring-inset {getTypeStyles(type)}">
              {getTypeLabel(type)}
            </span>
          {/each}
        </div>
      </div>

      <div class="overflow-hidden rounded-2xl bg-white shadow-sm ring-1 ring-slate-200">
        <ul class="divide-y divide-slate-100">
          {#each calendarEvents as event}
            <li class="p-6 transition-colors hover:bg-slate-50 sm:p-8">
              <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-4">
                <div class="flex items-start gap-4 sm:gap-6">
                  <!-- Date Badge -->
                  <div class="flex min-w-32 flex-col rounded-xl bg-slate-100 p-3 text-center ring-1 ring-slate-200">
                     <span class="text-sm font-bold text-slate-900">{event.date}</span>
                  </div>
                  
                  <!-- Info -->
                  <div>
                    <h3 class="text-lg font-bold text-school-navy">{event.title}</h3>
                    <p class="mt-1 text-sm text-slate-600 line-clamp-2 md:line-clamp-none">{event.desc}</p>
                  </div>
                </div>
                
                <!-- Type Label -->
                <div class="hidden shrink-0 sm:block">
                  <span class="inline-flex items-center rounded-md px-2.5 py-1 text-xs font-medium ring-1 ring-inset {getTypeStyles(event.type)}">
                    {getTypeLabel(event.type)}
                  </span>
                </div>
              </div>
            </li>
          {/each}
        </ul>
      </div>

    </div>
  </div>
</section>
