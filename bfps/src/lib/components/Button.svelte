<script lang="ts">
  import type { Snippet } from 'svelte';

  let {
    href = '',
    type = 'button',
    variant = 'primary',
    size = 'md',
    disabled = false,
    class: className = '',
    onclick,
    children
  }: {
    href?: string;
    type?: 'button' | 'submit' | 'reset';
    variant?: 'primary' | 'secondary' | 'outline' | 'ghost';
    size?: 'sm' | 'md' | 'lg';
    disabled?: boolean;
    class?: string;
    onclick?: (e: MouseEvent) => void;
    children: Snippet;
  } = $props();

  const baseStyles = 'inline-flex items-center justify-center rounded-xl font-bold tracking-tight transition-all duration-300 focus:outline-none focus:ring-2 focus:ring-offset-2 disabled:opacity-50 disabled:cursor-not-allowed uppercase text-xs sm:text-sm';
  
  const variantStyles = {
    primary: 'bg-school-navy text-white shadow-lg shadow-blue-900/20 hover:bg-blue-950 hover:shadow-xl hover:-translate-y-0.5 focus:ring-school-navy ring-1 ring-white/10',
    secondary: 'bg-school-gold text-school-navy shadow-lg shadow-yellow-500/20 hover:bg-yellow-400 hover:shadow-xl hover:-translate-y-0.5 focus:ring-school-gold',
    outline: 'border border-slate-200 bg-white text-school-navy shadow-sm hover:border-school-navy hover:bg-slate-50 hover:shadow-md hover:-translate-y-0.5 focus:ring-school-navy',
    ghost: 'text-school-navy hover:bg-slate-50 focus:ring-school-navy'
  };

  const sizeStyles = {
    sm: 'px-4 py-1.5 text-sm',
    md: 'px-6 py-2.5 text-base',
    lg: 'px-8 py-3.5 text-lg'
  };

  let combinedClasses = $derived(`${baseStyles} ${variantStyles[variant]} ${sizeStyles[size]} ${className}`);
</script>

{#if href}
  <a {href} class={combinedClasses}>
    {@render children()}
  </a>
{:else}
  <button {type} {disabled} class={combinedClasses} {onclick}>
    {@render children()}
  </button>
{/if}
