<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="about"
    class="py-20 bg-white dark:bg-slate-950 text-slate-900 dark:text-white scroll-mt-20 transition-colors duration-300 relative overflow-hidden"
  >
    <div class="absolute top-8 left-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden sm:block tracking-widest">
      + SYS.LOC_0x7A2F
    </div>
    <div class="absolute bottom-8 right-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden sm:block tracking-widest">
      // SEC_ABOUT_END
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">

      <div class="flex flex-col items-center text-center mb-16">

        <div class="font-mono text-sm sm:text-base mb-4 flex items-center gap-2 select-none">
          <span class="text-slate-500 dark:text-slate-500">bruno@portfolio:~$</span>
          <span class="text-violet-600 dark:text-purple-400 font-semibold">cat about_me.md</span>
          <span class="w-2.5 h-5 bg-violet-600 dark:bg-purple-400 animate-pulse"></span>
        </div>

        <h2 class="text-3xl sm:text-4xl md:text-5xl font-mono font-bold text-slate-900 dark:text-white tracking-wide mb-5">
          Sobre Mim
        </h2>

        <p class="text-slate-600 dark:text-slate-400 text-sm sm:text-base max-w-2xl mx-auto leading-relaxed">
          Um pouco sobre minha trajetória, minha paixão por tecnologia e o que me motiva a construir soluções digitais de alto impacto.
        </p>

      </div>

      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-12 items-start">

        <div class="lg:col-span-7 bg-slate-50 dark:bg-slate-900/40 border border-slate-200 dark:border-slate-900 rounded-xl overflow-hidden shadow-xs">
          <div class="flex items-center justify-between px-4 py-2.5 border-b border-slate-200 dark:border-slate-900 bg-slate-100/50 dark:bg-slate-950/50 select-none">
            <div class="flex items-center gap-2">
              <span class="w-2.5 h-2.5 rounded-full bg-slate-300 dark:bg-slate-800"></span>
              <span class="font-mono text-[11px] text-slate-400 dark:text-slate-500">about_me.md</span>
            </div>
            <span class="font-mono text-[10px] text-violet-500 dark:text-purple-500/80 font-bold">UTF-8</span>
          </div>

          <div class="p-6 space-y-5 font-mono text-xs sm:text-sm border-l-2 border-violet-500 dark:border-purple-500">

            <div class="flex items-start gap-4 group/line">
              <span class="text-slate-300 dark:text-slate-700 select-none text-right w-5 group-hover/line:text-violet-500">01</span>
              <p class="text-slate-600 dark:text-slate-400 font-sans text-sm sm:text-base leading-relaxed">
                Sou <strong class="font-semibold text-violet-600 dark:text-purple-400">Bruno Amorim</strong>, desenvolvedor focado em construir aplicações eficientes, limpas e com interfaces intuitivas. Busco transformar lógicas complexas em código bem estruturado.
              </p>
            </div>

            <div class="flex items-start gap-4 group/line">
              <span class="text-slate-300 dark:text-slate-700 select-none text-right w-5 group-hover/line:text-violet-500">02</span>
              <p class="text-slate-600 dark:text-slate-400 font-sans text-sm sm:text-base leading-relaxed">
                Atualmente cursando <strong class="font-semibold text-violet-600 dark:text-purple-400">Ciência da Computação</strong> na Uninassau Aracaju, concilio a base teórica acadêmica (algoritmos e estruturas de dados) com a criação de projetos full-stack reais.
              </p>
            </div>

            <div class="flex items-start gap-4 group/line">
              <span class="text-slate-300 dark:text-slate-700 select-none text-right w-5 group-hover/line:text-violet-500">03</span>
              <p class="text-slate-600 dark:text-slate-400 font-sans text-sm sm:text-base leading-relaxed">
                Minhas principais frentes cobrem ecossistemas reativos no front-end com <strong class="font-semibold text-violet-600 dark:text-purple-400">Vue.js</strong> e <strong class="font-semibold text-violet-600 dark:text-purple-400">Tailwind CSS</strong>, além de soluções integradas no back-end utilizando <strong class="font-semibold text-violet-600 dark:text-purple-400">Node.js</strong> e <strong class="font-semibold text-violet-600 dark:text-purple-400">Python</strong>.
              </p>
            </div>

          </div>
        </div>

        <div class="lg:col-span-5 grid grid-cols-1 sm:grid-cols-2 gap-4 w-full">

          <div class="group relative p-5 bg-slate-50 dark:bg-slate-900/20 border border-slate-200 dark:border-slate-900 rounded-xl space-y-3 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-200 hover:-translate-y-0.5">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-violet-600 dark:text-purple-400 font-bold bg-violet-50 dark:bg-purple-950/30 px-2 py-0.5 rounded border border-violet-100 dark:border-purple-900/40">
                [_EDU]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// ACADEMIC</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Graduação</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Ciência da Computação<br />
                <span class="text-[11px] text-slate-400 dark:text-slate-500 font-mono">Uninassau Aracaju</span>
              </p>
              <div class="pt-1">
                <span class="inline-flex items-center gap-1.5 px-2 py-0.5 rounded bg-emerald-50 dark:bg-emerald-950/30 border border-emerald-100 dark:border-emerald-900/30 text-[10px] text-emerald-600 dark:text-emerald-400 font-mono">
                  <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 dark:bg-emerald-400 animate-pulse"></span>
                  3º Período
                </span>
              </div>
            </div>
          </div>

          <div class="group relative p-5 bg-slate-50 dark:bg-slate-900/20 border border-slate-200 dark:border-slate-900 rounded-xl space-y-3 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-200 hover:-translate-y-0.5">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-violet-600 dark:text-purple-400 font-bold bg-violet-50 dark:bg-purple-950/30 px-2 py-0.5 rounded border border-violet-100 dark:border-purple-900/40">
                [_STACK]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// ENV_FOCUS</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Foco Atual</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Aplicações Web SPA modernas, desenvolvimento mobile e microsserviços integrados.
              </p>
            </div>
          </div>

          <div class="group relative p-5 bg-slate-50 dark:bg-slate-900/20 border border-slate-200 dark:border-slate-900 rounded-xl space-y-3 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-200 hover:-translate-y-0.5">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-violet-600 dark:text-purple-400 font-bold bg-violet-50 dark:bg-purple-950/30 px-2 py-0.5 rounded border border-violet-100 dark:border-purple-900/40">
                [_LOGIC]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// METRICS</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Diretrizes</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Código limpo (Clean Code), componentização reutilizável e otimização de performance.
              </p>
            </div>
          </div>

          <div class="group relative p-5 bg-slate-50 dark:bg-slate-900/20 border border-slate-200 dark:border-slate-900 rounded-xl space-y-3 hover:border-violet-500/40 dark:hover:border-purple-500/40 transition-all duration-200 hover:-translate-y-0.5">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-violet-600 dark:text-purple-400 font-bold bg-violet-50 dark:bg-purple-950/30 px-2 py-0.5 rounded border border-violet-100 dark:border-purple-900/40">
                [_IDLE]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// RUNTIME</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Hobbies</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Violão acústico (MPB), composição musical autoral e jogos de estratégia/RPG de mesa.
              </p>
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
