<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <footer
    class="relative bg-slate-50 dark:bg-slate-950 border-t border-slate-200 dark:border-slate-900 py-10 text-slate-500 dark:text-slate-400 transition-colors duration-300 overflow-hidden"
  >
    <div
      class="absolute top-0 left-0 w-full h-px bg-linear-to-r from-transparent via-violet-500/30 dark:via-purple-500/30 to-transparent"
    ></div>

    <div
      class="w-full px-6 md:px-12 flex flex-col md:flex-row items-center justify-between gap-6 relative z-10"
    >
      <div
        class="flex items-start gap-3 group/copy text-center md:text-left justify-center md:justify-start"
      >
        <span
          class="font-mono text-xs text-slate-300 dark:text-slate-700 select-none group-hover/copy:text-violet-500 dark:group-hover/copy:text-purple-500 transition-colors duration-300 mt-1 hidden sm:inline"
          >[!]</span
        >

        <div class="flex flex-col">
          <span
            class="text-base font-mono text-slate-900 dark:text-white tracking-wide uppercase transition-colors duration-300 group-hover/copy:text-violet-600 dark:group-hover/copy:text-purple-400"
          >
            Bruno Amorim
          </span>

          <p class="font-mono text-xs tracking-wide text-slate-400 dark:text-slate-500 mt-1">
            &copy; {{ currentYear }} <span class="text-slate-300 dark:text-slate-800">—</span>
            Construído com
            <span
              class="text-emerald-500 dark:text-emerald-400 font-semibold transition-colors duration-300"
              >Vue.js 3</span
            >
            &amp;
            <span
              class="text-cyan-600 dark:text-cyan-400 font-semibold transition-colors duration-300"
              >Tailwind CSS</span
            >
          </p>
        </div>
      </div>

      <div
        class="hidden md:flex items-center gap-4 font-mono text-[10px] text-slate-400 dark:text-slate-600 select-none bg-slate-100/50 dark:bg-slate-900/40 px-3 py-1.5 rounded-md border border-slate-200/60 dark:border-slate-800/40"
      >
        <div class="flex items-center gap-1">
          <span
            class="w-1.5 h-1.5 rounded-full bg-emerald-500 dark:bg-emerald-400 animate-pulse"
          ></span>
          <span>ENV: PRODUCTION</span>
        </div>
        <span class="text-slate-300 dark:text-slate-800">|</span>
        <div>BUILD: STABLE</div>
      </div>

      <div class="flex items-center space-x-6 font-mono text-xs">
        <a
          href="https://github.com"
          target="_blank"
          class="group flex items-center gap-1 hover:text-violet-600 dark:hover:text-purple-400 transition-colors duration-300"
        >
          <span
            class="text-slate-300 dark:text-slate-700 font-normal group-hover:text-violet-500 dark:group-hover:text-purple-500 transition-colors duration-300"
            >~/</span
          >
          <span>GitHub</span>
        </a>

        <a
          href="https://linkedin.com"
          target="_blank"
          class="group flex items-center gap-1 hover:text-violet-600 dark:hover:text-purple-400 transition-colors duration-300"
        >
          <span
            class="text-slate-300 dark:text-slate-700 font-normal group-hover:text-violet-500 dark:group-hover:text-purple-500 transition-colors duration-300"
            >~/</span
          >
          <span>LinkedIn</span>
        </a>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>
