<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <component
    :is="href ? 'a' : 'button'"
    :href="href"
    :type="!href ? type : null"
    :target="href && external ? '_blank' : null"
    :disabled="disabled"
    :class="[
      'inline-flex items-center justify-center gap-2 font-mono text-xs font-bold uppercase tracking-wider px-5 py-3 rounded-lg border transition-all duration-300 select-none active:scale-95 disabled:opacity-50 disabled:pointer-events-none cursor-pointer',
      variants[variant]
    ]"
  >
    <slot name="icon-left" />

    <slot />

    <slot name="icon-right" />
  </component>
</template>

<script setup>
defineProps({
  href: {
    type: String,
    default: ''
  },
  type: {
    type: String,
    default: 'button'
  },
  external: {
    type: Boolean,
    default: false
  },
  disabled: {
    type: Boolean,
    default: false
  },
  variant: {
    type: String,
    default: 'primary',
    validator: (value) => ['primary', 'secondary', 'terminal'].includes(value)
  }
})

// Dicionário de variantes CSS do Tailwind
const variants = {
  primary: 'bg-violet-600 hover:bg-violet-700 text-white border-transparent shadow-lg shadow-violet-500/10 dark:shadow-purple-500/5 hover:shadow-violet-500/25',
  secondary: 'bg-transparent border-slate-200 dark:border-slate-800 text-slate-700 dark:text-slate-300 hover:border-violet-500/50 dark:hover:border-purple-500/50 hover:text-violet-600 dark:hover:text-purple-400',
  terminal: 'bg-slate-100 hover:bg-violet-600/10 dark:bg-slate-950 dark:hover:bg-purple-500/10 border border-slate-200/80 dark:border-slate-800/80 hover:border-violet-500/50 dark:hover:border-purple-500/50 text-slate-600 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400'
}
</script>
