<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="skills"
    class="py-20 bg-slate-50 dark:bg-slate-900 text-slate-900 dark:text-white scroll-mt-20 transition-colors duration-300 relative overflow-hidden"
  >
    <div class="absolute top-12 left-8 text-slate-200 dark:text-slate-800/50 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      + MATRIX.DIAG_0x99FF
    </div>
    <div class="absolute bottom-12 right-8 text-slate-200 dark:text-slate-800/50 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      // CORE_STACK_LOADED [OK]
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">
      
      <div class="flex flex-col items-center text-center mb-16">
        <div class="flex items-center gap-1.5 text-purple-600 dark:text-purple-400 font-mono text-sm tracking-widest uppercase mb-2">
          <span>&lt;</span>
          <span>Habilidades</span>
          <span class="animate-pulse">/&gt;</span>
        </div>
        <h2 class="text-3xl sm:text-4xl font-extrabold text-slate-900 dark:text-white tracking-tight">
          Competências Técnicas
        </h2>
        <div class="h-0.5 w-24 bg-linear-to-r from-transparent via-purple-500 to-transparent mt-4"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        
        <div class="group relative p-6 bg-white dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-6 hover:border-purple-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-purple-500/5 overflow-hidden">
          <div class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-purple-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          
          <div class="flex items-center justify-between">
            <h3 class="font-mono text-xs text-purple-600 dark:text-purple-400 font-bold uppercase tracking-widest flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-purple-500"></span>
              [01] Front-End Engine
            </h3>
            <span class="font-mono text-[10px] text-slate-400 dark:text-slate-600">// ONLINE</span>
          </div>

          <div class="space-y-4">
            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Vue.js</span>
                <span class="text-emerald-500">55%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-emerald-500 rounded-full transition-all duration-500 w-[55%] group-hover:bg-linear-to-r group-hover:from-emerald-500 group-hover:to-green-500"></div>
              </div>
            </div>

            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Tailwind CSS</span>
                <span class="text-cyan-500">90%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-cyan-500 rounded-full transition-all duration-500 w-[90%] group-hover:bg-linear-to-r group-hover:from-cyan-500 group-hover:to-blue-500"></div>
              </div>
            </div>

            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">JavaScript (ES6+)</span>
                <span class="text-yellow-500">90%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-yellow-500 rounded-full transition-all duration-500 w-[90%] group-hover:bg-linear-to-r group-hover:from-yellow-500 group-hover:to-orange-500"></div>
              </div>
            </div>
          </div>
        </div>

        <div class="group relative p-6 bg-white dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-6 hover:border-purple-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-purple-500/5 overflow-hidden">
          <div class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-purple-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          
          <div class="flex items-center justify-between">
            <h3 class="font-mono text-xs text-purple-600 dark:text-purple-400 font-bold uppercase tracking-widest flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-purple-500"></span>
              [02] Back-End Core
            </h3>
            <span class="font-mono text-[10px] text-slate-400 dark:text-slate-600">// RUNNING</span>
          </div>

          <div class="space-y-4">
            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Node.js</span>
                <span class="text-green-500">75%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-green-500 rounded-full transition-all duration-500 w-[75%] group-hover:bg-linear-to-r group-hover:from-green-500 group-hover:to-emerald-500"></div>
              </div>
            </div>

            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Python / Flask</span>
                <span class="text-blue-500">54%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-blue-500 rounded-full transition-all duration-500 w-[54%] group-hover:bg-linear-to-r group-hover:from-blue-500 group-hover:to-yellow-500"></div>
              </div>
            </div>

            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">REST APIs & SQL</span>
                <span class="text-purple-500">65%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-purple-500 rounded-full transition-all duration-500 w-[65%] group-hover:bg-linear-to-r group-hover:from-purple-500 group-hover:to-indigo-500"></div>
              </div>
            </div>
          </div>
        </div>

        <div class="group relative p-6 bg-white dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-6 hover:border-purple-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-purple-500/5 overflow-hidden">
          <div class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-purple-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          
          <div class="flex items-center justify-between">
            <h3 class="font-mono text-xs text-purple-600 dark:text-purple-400 font-bold uppercase tracking-widest flex items-center gap-2">
              <span class="w-1.5 h-1.5 rounded-full bg-purple-500"></span>
              [03] Mobile & CS Core
            </h3>
            <span class="font-mono text-[10px] text-slate-400 dark:text-slate-600">// COMPILED</span>
          </div>

          <div class="space-y-4">
            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Flutter / Dart</span>
                <span class="text-blue-400">45%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-blue-500 rounded-full transition-all duration-500 w-[45%] group-hover:bg-linear-to-r group-hover:from-blue-500 group-hover:to-white"></div>
              </div>
            </div>

            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Estruturas de Dados</span>
                <span class="text-purple-500">50%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-purple-500 rounded-full transition-all duration-500 w-[50%] group-hover:bg-linear-to-r group-hover:from-purple-500 group-hover:to-indigo-500"></div>
              </div>
            </div>

            <div class="space-y-1.5">
              <div class="flex justify-between font-mono text-xs">
                <span class="text-slate-700 dark:text-slate-300 font-semibold">Análise de Algoritmos</span>
                <span class="text-purple-500">65%</span>
              </div>
              <div class="h-1.5 w-full bg-slate-100 dark:bg-slate-900 rounded-full overflow-hidden p-px border border-slate-200/50 dark:border-slate-800/50">
                <div class="h-full bg-purple-500 rounded-full transition-all duration-500 w-[65%] group-hover:bg-linear-to-r group-hover:from-purple-500 group-hover:to-indigo-500"></div>
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
