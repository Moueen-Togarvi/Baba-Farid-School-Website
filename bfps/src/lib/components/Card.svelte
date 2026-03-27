<script lang="ts">
  import type { Snippet } from 'svelte';

  let {
    title,
    subtitle,
    hover = false,
    class: className = '',
    children
  }: {
    title?: string;
    subtitle?: string;
    hover?: boolean;
    class?: string;
    children: Snippet;
  } = $props();
</script>

<div class={`overflow-hidden rounded-2xl bg-white shadow-sm ring-1 ring-slate-200 transition-all ${hover ? 'hover:-translate-y-1 hover:shadow-md' : ''} ${className}`}>
  {#if title || subtitle}
    <div class="border-b border-slate-100 bg-slate-50/50 px-6 py-4">
      {#if title}
        <h3 class="text-xl font-bold text-school-navy">{title}</h3>
      {/if}
      {#if subtitle}
        <p class="mt-1 text-sm text-slate-500">{subtitle}</p>
      {/if}
    </div>
  {/if}
  
  <div class="px-6 py-5">
    {@render children()}
  </div>
</div>
