<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="skills"
    class="relative scroll-mt-20 overflow-hidden bg-slate-50 py-20 text-slate-900 transition-colors duration-300 dark:bg-[#09090b] dark:text-white"
  >
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="mb-12 flex flex-col items-center text-center">
        <div class="mb-3 flex items-center gap-2 font-mono text-xs text-slate-500 dark:text-zinc-500 sm:text-sm">
          <span class="text-slate-500 dark:text-slate-500">bruno@portfolio:~$</span>
          <span class="text-indigo-600 dark:text-indigo-400 font-semibold">ls --skills</span>
          <span class="terminal-blink h-3.5 w-1 bg-indigo-500"></span>
        </div>
        <h2 class="mb-4 text-3xl font-mono font-bold tracking-tight text-slate-900 dark:text-white sm:text-4xl md:text-5xl">
          Competências Técnicas
        </h2>
        <p class="mx-auto max-w-2xl text-sm leading-relaxed text-slate-600 dark:text-zinc-400 sm:text-base">
          Uma visão detalhada das linguagens, frameworks e ferramentas que utilizo focando em arquitetura limpa, performance e escalabilidade.
        </p>
      </div>

      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">

        <!-- Módulo 01: Front-End Engine -->
        <div class="group overflow-hidden rounded-lg border border-slate-200 bg-white/70 transition-colors duration-300 hover:border-indigo-500/50 dark:border-zinc-800 dark:bg-zinc-900/35 dark:hover:border-indigo-500/50">
          <div class="flex items-center justify-between border-b border-slate-200 px-5 py-4 select-none dark:border-zinc-800">
            <h3 class="font-mono text-xs text-indigo-600 dark:text-indigo-400 font-bold uppercase tracking-wider flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-indigo-500 dark:bg-indigo-500"></span>
              THREAD_01 // FRONT_ENGINE
            </h3>
            <span class="font-mono text-[10px] text-emerald-500 dark:text-emerald-400 font-bold bg-emerald-50 dark:bg-emerald-950/20 px-1.5 py-0.5 rounded border border-emerald-100 dark:border-emerald-900/30">ACTIVE</span>
          </div>
          <div class="space-y-5 p-5">
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
        <div class="group overflow-hidden rounded-lg border border-slate-200 bg-white/70 transition-colors duration-300 hover:border-indigo-500/50 dark:border-zinc-800 dark:bg-zinc-900/35 dark:hover:border-indigo-500/50">
          <div class="flex items-center justify-between border-b border-slate-200 px-5 py-4 select-none dark:border-zinc-800">
            <h3 class="font-mono text-xs text-indigo-600 dark:text-indigo-400 font-bold uppercase tracking-wider flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-indigo-500 dark:bg-indigo-500"></span>
              THREAD_02 // BACK_CORE
            </h3>
            <span class="font-mono text-[10px] text-indigo-500 dark:text-indigo-400 font-bold bg-indigo-50 dark:bg-indigo-950/20 px-1.5 py-0.5 rounded border border-indigo-100 dark:border-indigo-900/30">RUNNING</span>
          </div>

          <div class="space-y-5 p-5">
            <!-- Skill: Node.js (Green/Lime) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Node.js <span class="text-[10px] text-slate-400 font-normal">v26.x</span></span>
                <span class="text-green-600 dark:text-green-400 font-medium">75%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-green-500 rounded-xs transition-all duration-500 w-[75%] group-hover:bg-linear-to-r group-hover:from-green-500 group-hover:to-emerald-500"></div>
              </div>
            </div>

            <!-- Skill: Python / Flask (Blue/Steel) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Python <span class="text-[10px] text-slate-400 font-normal">v3.x</span></span>
                <span class="text-blue-500 dark:text-blue-400 font-medium">60%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-blue-600 rounded-xs transition-all duration-500 w-[60%] group-hover:bg-linear-to-r group-hover:from-blue-600 group-hover:to-sky-500"></div>
              </div>
            </div>

            <!-- Skill: REST APIs & SQL (Cyan/Blue) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">PostgreSQL <span class="text-[10px] text-slate-400 font-normal">v17.x</span></span>
                <span class="text-cyan-600 dark:text-cyan-400 font-medium">45%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-cyan-500 rounded-xs transition-all duration-500 w-[45%] group-hover:bg-linear-to-r group-hover:from-cyan-500 group-hover:to-blue-500"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Módulo 03: Mobile & CS Core -->
        <div class="group overflow-hidden rounded-lg border border-slate-200 bg-white/70 transition-colors duration-300 hover:border-indigo-500/50 dark:border-zinc-800 dark:bg-zinc-900/35 dark:hover:border-indigo-500/50">
          <div class="flex items-center justify-between border-b border-slate-200 px-5 py-4 select-none dark:border-zinc-800">
            <h3 class="font-mono text-xs text-indigo-600 dark:text-indigo-400 font-bold uppercase tracking-wider flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-indigo-500 dark:bg-indigo-500"></span>
              THREAD_03 // CS_CORE
            </h3>
            <span class="font-mono text-[10px] text-amber-600 dark:text-amber-400 font-bold bg-amber-50 dark:bg-amber-950/20 px-1.5 py-0.5 rounded border border-amber-100 dark:border-amber-900/30">COMPILED</span>
          </div>

          <div class="space-y-5 p-5">
            <!-- Skill: Flutter / Dart (Sky/Light Blue) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Dart <span class="text-[10px] text-slate-400 font-normal">/ Flutter</span></span>
                <span class="text-sky-500 dark:text-sky-400 font-medium">45%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-sky-400 rounded-xs transition-all duration-500 w-[45%] group-hover:bg-linear-to-r group-hover:from-sky-400 group-hover:to-blue-500"></div>
              </div>
            </div>

            <!-- Skill: Estruturas de Dados (Rose/Amber) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Estruturas de Dados</span>
                <span class="text-rose-600 dark:text-rose-400 font-medium">50%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-rose-500 rounded-xs transition-all duration-500 w-[50%] group-hover:bg-linear-to-r group-hover:from-rose-500 group-hover:to-amber-400"></div>
              </div>
            </div>

            <!-- Skill: Arquitetura de Software (Indigo/Blue) -->
            <div class="space-y-2">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-bold">Arquitetura de Software</span>
                <span class="text-indigo-600 dark:text-indigo-400 font-medium">65%</span>
              </div>
              <div class="h-2 w-full bg-slate-100 dark:bg-slate-950 rounded border border-slate-200/60 dark:border-slate-800 overflow-hidden p-0.5">
                <div class="h-full bg-indigo-500 rounded-xs transition-all duration-500 w-[65%] group-hover:bg-linear-to-r group-hover:from-indigo-500 group-hover:to-blue-400"></div>
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
