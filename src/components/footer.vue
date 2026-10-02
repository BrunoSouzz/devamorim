<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <footer class="section-reveal border-t border-slate-200 bg-slate-50/80 py-5 font-mono text-xs text-slate-500 transition-colors duration-300 select-none dark:border-zinc-800 dark:bg-[#09090b] dark:text-zinc-500">

    <div class="relative z-10 mx-auto flex max-w-7xl flex-col items-center justify-between gap-4 px-6 sm:flex-row">

      <div class="flex flex-wrap items-center justify-center sm:justify-start gap-x-4 gap-y-2 text-center sm:text-left">
        <div class="flex items-center gap-1.5 text-slate-900 dark:text-slate-300 font-bold">
          <span>&copy; {{ currentYear }}</span>
          <span class="text-slate-300 dark:text-zinc-800">/</span>
          <span class="text-indigo-600 dark:text-indigo-400 uppercase tracking-tight">Bruno Amorim</span>
        </div>

        <span class="hidden text-slate-300 dark:text-zinc-800 md:inline">/</span>

        <div class="hidden md:flex items-center gap-3 text-[11px] text-slate-400 dark:text-slate-500">
          <div class="flex items-center gap-1 hover:text-indigo-500 transition-colors">
            <span class="text-indigo-500 font-bold">⊗</span> 0
          </div>
          <div class="flex items-center gap-1 hover:text-amber-500 transition-colors">
            <span class="text-amber-500 font-bold">⚠</span> 0
          </div>
        </div>

        <span class="hidden text-slate-300 dark:text-zinc-800 sm:inline">/</span>

        <p class="text-[11px] text-slate-400 dark:text-slate-500">
          compilado com
          <span class="text-emerald-500 dark:text-emerald-400/90 font-bold">Vue 3</span>
          &amp;
          <span class="text-cyan-500 dark:text-cyan-400/90 font-bold">Tailwind</span>
        </p>
      </div>

      <div class="flex items-center gap-6 text-[11px]">

        <div class="hidden lg:flex items-center space-x-4 text-slate-400 dark:text-slate-600 border-r border-slate-200 dark:border-slate-900 pr-6">
          <span>Ln 104, Col 32</span>
          <span>Spaces: 2</span>
          <span>UTF-8</span>
          <span class="text-indigo-500 dark:text-indigo-500 font-bold">Vue v3.x</span>
        </div>

        <div class="flex items-center gap-3">

          <a
            href="https://github.com/BrunoSouzz"
            target="_blank"
            class="group flex items-center gap-1.5 rounded-md border border-slate-200 bg-slate-50 px-2.5 py-1.5 text-slate-700 transition-colors hover:border-indigo-500/50 hover:bg-indigo-500/5 hover:text-indigo-600 dark:border-zinc-800 dark:bg-zinc-900/50 dark:text-zinc-300 dark:hover:border-indigo-500/50 dark:hover:bg-indigo-500/10 dark:hover:text-indigo-400"
            title="Acessar GitHub"
          >
            <svg class="w-3.5 h-3.5 fill-current transition-transform duration-300 group-hover:scale-110" viewBox="0 0 24 24" aria-hidden="true">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.603-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.462-1.11-1.462-.908-.62.069-.061.069-.061 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.831.092-.646.35-1.086.636-1.336-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.579.688.481C19.138 20.161 22 16.418 22 12c0-5.523-4.477-10-10-10z" />
            </svg>
            <span class="font-bold tracking-wide">io.github</span>
          </a>

          <a
            href="https://www.linkedin.com/in/dev-brunoamorim"
            target="_blank"
            class="group flex items-center gap-1.5 rounded-md border border-slate-200 bg-slate-50 px-2.5 py-1.5 text-slate-700 transition-colors hover:border-indigo-500/50 hover:bg-indigo-500/5 hover:text-indigo-600 dark:border-zinc-800 dark:bg-zinc-900/50 dark:text-zinc-300 dark:hover:border-indigo-500/50 dark:hover:bg-indigo-500/10 dark:hover:text-indigo-400"
            title="Acessar LinkedIn"
          >
            <svg class="w-3.5 h-3.5 fill-current transition-transform duration-300 group-hover:scale-110" viewBox="0 0 24 24" aria-hidden="true">
              <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
            </svg>
            <span class="font-bold tracking-wide">net.linkedin</span>
          </a>

        </div>

      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>
