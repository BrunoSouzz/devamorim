<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <footer class="relative bg-slate-100/80 dark:bg-slate-950 border-t border-slate-200 dark:border-slate-900 py-4 text-slate-500 dark:text-slate-400 transition-colors duration-300 select-none font-mono text-xs">

    <!-- Linha laser estética superior -->
    <div class="absolute top-0 left-0 w-full h-px bg-linear-to-r from-transparent via-violet-500/30 dark:via-purple-500/30 to-transparent"></div>

    <div class="max-w-7xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4 relative z-10">

      <!-- Lado Esquerdo: Copyright, Status do Linter & Engine -->
      <div class="flex flex-wrap items-center justify-center sm:justify-start gap-x-4 gap-y-2 text-center sm:text-left">
        <div class="flex items-center gap-1.5 text-slate-900 dark:text-slate-300 font-bold">
          <span>&copy; {{ currentYear }}</span>
          <span class="text-slate-300 dark:text-slate-800">|</span>
          <span class="text-violet-600 dark:text-purple-400 uppercase tracking-tight">Bruno Amorim</span>
        </div>

        <span class="text-slate-300 dark:text-slate-800 hidden md:inline">|</span>

        <!-- Diagnósticos de Código (0 Erros / 0 Avisos) -->
        <div class="hidden md:flex items-center gap-3 text-[11px] text-slate-400 dark:text-slate-500">
          <div class="flex items-center gap-1 hover:text-emerald-500 transition-colors">
            <span class="text-emerald-500 font-bold">⊗</span> 0
          </div>
          <div class="flex items-center gap-1 hover:text-amber-500 transition-colors">
            <span class="text-amber-500 font-bold">⚠</span> 0
          </div>
        </div>

        <span class="text-slate-300 dark:text-slate-800 hidden sm:inline">|</span>

        <!-- Especificações da Stack -->
        <p class="text-[11px] text-slate-400 dark:text-slate-500">
          compilado com
          <span class="text-emerald-500 dark:text-emerald-400/90 font-bold">Vue 3</span>
          &amp;
          <span class="text-cyan-500 dark:text-cyan-400/90 font-bold">Tailwind</span>
        </p>
      </div>

      <!-- Lado Direito: Parâmetros da IDE & Links de Conexão -->
      <div class="flex items-center gap-6 text-[11px]">

        <!-- Métricas de Ambiente (Ocultas em telas muito pequenas) -->
        <div class="hidden lg:flex items-center space-x-4 text-slate-400 dark:text-slate-600 border-r border-slate-200 dark:border-slate-900 pr-6">
          <span>Ln 104, Col 32</span>
          <span>Spaces: 2</span>
          <span>UTF-8</span>
          <span class="text-violet-500 dark:text-purple-500 font-bold">Vue v3.x</span>
        </div>

        <!-- Links Sociais como Subdomínios Operacionais -->
        <div class="flex items-center space-x-4">
          <a
            href="https://github.com/BrunoSouzz"
            target="_blank"
            class="group flex items-center gap-1 text-slate-400 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 transition-colors duration-200"
          >
            <span class="text-slate-300 dark:text-slate-800 group-hover:text-violet-500 transition-colors font-normal">[</span>
            <span>io.github</span>
            <span class="text-slate-300 dark:text-slate-800 group-hover:text-violet-500 transition-colors font-normal">]</span>
          </a>

          <a
            href="https://www.linkedin.com/in/dev-brunoamorim"
            target="_blank"
            class="group flex items-center gap-1 text-slate-400 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 transition-colors duration-200"
          >
            <span class="text-slate-300 dark:text-slate-800 group-hover:text-purple-500 transition-colors font-normal">[</span>
            <span>net.linkedin</span>
            <span class="text-slate-300 dark:text-slate-800 group-hover:text-purple-500 transition-colors font-normal">]</span>
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
