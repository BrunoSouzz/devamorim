<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="skills"
    class="py-20 bg-slate-50 dark:bg-slate-950 text-slate-900 dark:text-white scroll-mt-20 transition-colors duration-300 relative overflow-hidden"
  >
    <!-- Background Grid Alinhado com a Identidade de Workspace -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#80808007_1px,transparent_1px),linear-gradient(to_bottom,#80808007_1px,transparent_1px)] bg-size-[24px_24px] pointer-events-none"></div>

    <!-- Linhas de Telemetria Laterais -->
    <div class="absolute top-12 left-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      + MATRIX.DIAG_0x99FF
    </div>
    <div class="absolute bottom-12 right-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      // CORE_STACK_LOADED [OK]
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">

      <!-- Cabeçalho (Comando do Analisador de Sistema) -->
      <div class="flex flex-col items-center text-center mb-16">

        <div class="font-mono text-sm sm:text-base mb-4 flex items-center gap-2 select-none">
          <span class="text-slate-500 dark:text-slate-500">bruno@portfolio:~$</span>
          <span class="text-violet-600 dark:text-purple-400 font-semibold">ls --skills</span>
          <span class="w-2.5 h-5 bg-violet-600 dark:bg-purple-400 animate-pulse"></span>
        </div>

        <h2 class="text-3xl sm:text-4xl md:text-5xl font-mono font-bold text-slate-900 dark:text-white tracking-wide mb-5">
          Competências Técnicas
        </h2>

        <p class="text-slate-600 dark:text-slate-400 text-sm sm:text-base max-w-2xl mx-auto leading-relaxed">
          Uma visão detalhada das linguagens, frameworks e ferramentas que utilizo focando em arquitetura limpa, performance e escalabilidade.
        </p>

      </div>

      <!-- Grid de Módulos de Performance -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

        <!-- Módulo 01: Front-End Engine -->
        <div class="group relative p-6 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-900 rounded-xl space-y-6 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-300 hover:-translate-y-0.5">
          <div class="absolute top-0 left-0 w-full h-px bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>

          <div class="flex items-center justify-between border-b border-slate-100 dark:border-slate-900 pb-3 select-none">
            <h3 class="font-mono text-xs text-violet-600 dark:text-purple-400 font-bold uppercase tracking-wider flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-violet-500 dark:bg-purple-500"></span>
              THREAD_01 // FRONT_ENGINE
            </h3>
            <span class="font-mono text-[10px] text-emerald-500 dark:text-emerald-400 font-bold bg-emerald-50 dark:bg-emerald-950/20 px-1.5 py-0.5 rounded border border-emerald-100 dark:border-emerald-900/30">ACTIVE</span>
          </div>

          <div class="space-y-5">
            <!-- Skill: Vue.js (Emerald/Teal) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Vue.js <span class="text-[10px] text-slate-400 font-normal">v3.x</span></span>
                <span class="text-emerald-600 dark:text-emerald-400 font-medium">55%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-emerald-500 rounded-xs transition-all duration-500 w-[55%] group-hover:bg-linear-to-r group-hover:from-emerald-500 group-hover:to-teal-400"></div>
              </div>
            </div>

            <!-- Skill: Tailwind CSS (Cyan/Sky) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Tailwind CSS <span class="text-[10px] text-slate-400 font-normal">v4.x</span></span>
                <span class="text-cyan-600 dark:text-cyan-400 font-medium">90%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-cyan-500 rounded-xs transition-all duration-500 w-[90%] group-hover:bg-linear-to-r group-hover:from-cyan-500 group-hover:to-sky-400"></div>
              </div>
            </div>

            <!-- Skill: JavaScript (Yellow/Amber) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">JavaScript <span class="text-[10px] text-slate-400 font-normal">(ES6+)</span></span>
                <span class="text-amber-500 dark:text-amber-400 font-medium">90%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-yellow-500 rounded-xs transition-all duration-500 w-[90%] group-hover:bg-linear-to-r group-hover:from-yellow-400 group-hover:to-amber-500"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Módulo 02: Back-End Core -->
        <div class="group relative p-6 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-900 rounded-xl space-y-6 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-300 hover:-translate-y-0.5">
          <div class="absolute top-0 left-0 w-full h-px bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>

          <div class="flex items-center justify-between border-b border-slate-100 dark:border-slate-900 pb-3 select-none">
            <h3 class="font-mono text-xs text-violet-600 dark:text-purple-400 font-bold uppercase tracking-wider flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-violet-500 dark:bg-purple-500"></span>
              THREAD_02 // BACK_CORE
            </h3>
            <span class="font-mono text-[10px] text-violet-500 dark:text-purple-400 font-bold bg-violet-50 dark:bg-purple-950/20 px-1.5 py-0.5 rounded border border-violet-100 dark:border-purple-900/30">RUNNING</span>
          </div>

          <div class="space-y-5">
            <!-- Skill: Node.js (Green/Lime) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Node.js <span class="text-[10px] text-slate-400 font-normal">Runtime</span></span>
                <span class="text-green-600 dark:text-green-400 font-medium">75%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-green-500 rounded-xs transition-all duration-500 w-[75%] group-hover:bg-linear-to-r group-hover:from-green-500 group-hover:to-emerald-500"></div>
              </div>
            </div>

            <!-- Skill: Python / Flask (Blue/Steel) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Python <span class="text-[10px] text-slate-400 font-normal">/ Flask</span></span>
                <span class="text-blue-500 dark:text-blue-400 font-medium">54%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-blue-600 rounded-xs transition-all duration-500 w-[54%] group-hover:bg-linear-to-r group-hover:from-blue-600 group-hover:to-sky-500"></div>
              </div>
            </div>

            <!-- Skill: REST APIs & SQL -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">REST APIs &amp; SQL</span>
                <span class="text-indigo-500 dark:text-indigo-400 font-medium">65%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-indigo-500 rounded-xs transition-all duration-500 w-[65%] group-hover:bg-linear-to-r group-hover:from-indigo-500 group-hover:to-violet-500"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Módulo 03: Mobile & CS Core -->
        <div class="group relative p-6 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-900 rounded-xl space-y-6 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-300 hover:-translate-y-0.5">
          <div class="absolute top-0 left-0 w-full h-px bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>

          <div class="flex items-center justify-between border-b border-slate-100 dark:border-slate-900 pb-3 select-none">
            <h3 class="font-mono text-xs text-violet-600 dark:text-purple-400 font-bold uppercase tracking-wider flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-violet-500 dark:bg-purple-500"></span>
              THREAD_03 // CS_CORE
            </h3>
            <span class="font-mono text-[10px] text-amber-600 dark:text-amber-400 font-bold bg-amber-50 dark:bg-amber-950/20 px-1.5 py-0.5 rounded border border-amber-100 dark:border-amber-900/30">COMPILED</span>
          </div>

          <div class="space-y-5">
            <!-- Skill: Flutter / Dart (Sky/Light Blue) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Flutter <span class="text-[10px] text-slate-400 font-normal">/ Dart</span></span>
                <span class="text-sky-500 dark:text-sky-400 font-medium">45%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-sky-400 rounded-xs transition-all duration-500 w-[45%] group-hover:bg-linear-to-r group-hover:from-sky-400 group-hover:to-blue-500"></div>
              </div>
            </div>

            <!-- Skill: Estruturas de Dados (Fuchsia/Pink para Core Acadêmico) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Estruturas de Dados</span>
                <span class="text-fuchsia-600 dark:text-fuchsia-400 font-medium">50%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-fuchsia-500 rounded-xs transition-all duration-500 w-[50%] group-hover:bg-linear-to-r group-hover:from-fuchsia-500 group-hover:to-pink-500"></div>
              </div>
            </div>

            <!-- Skill: Análise de Algoritmos (Violet/Purple) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Análise de Algoritmos</span>
                <span class="text-violet-600 dark:text-purple-400 font-medium">65%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-violet-500 rounded-xs transition-all duration-500 w-[65%] group-hover:bg-linear-to-r group-hover:from-violet-500 group-hover:to-purple-500"></div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
</script>
