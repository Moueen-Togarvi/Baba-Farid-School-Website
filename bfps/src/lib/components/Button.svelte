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

  const baseStyles = 'inline-flex items-center justify-center rounded-full font-bold transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 disabled:opacity-50 disabled:cursor-not-allowed';
  
  const variantStyles = {
    primary: 'bg-school-gold text-school-navy shadow-md hover:bg-yellow-400 hover:-translate-y-0.5 focus:ring-school-gold',
    secondary: 'bg-school-navy text-white shadow-md hover:bg-blue-800 hover:-translate-y-0.5 focus:ring-school-navy',
    outline: 'border-2 border-school-navy text-school-navy hover:bg-school-navy hover:text-white focus:ring-school-navy',
    ghost: 'text-school-navy hover:bg-slate-100 focus:ring-school-navy'
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
