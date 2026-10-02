<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="about"
    class="relative scroll-mt-20 overflow-hidden bg-white py-20 text-slate-900 transition-colors duration-300 dark:bg-[#09090b] dark:text-white"
  >
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="mb-12 flex flex-col items-center text-center">
        <div class="mb-3 flex items-center gap-2 font-mono text-xs text-slate-500 dark:text-zinc-500 sm:text-sm">
          <span class="text-slate-500 dark:text-slate-500">bruno@portfolio:~$</span>
          <span class="text-indigo-600 dark:text-indigo-400 font-semibold">cat about_me.md</span>
          <span class="terminal-blink h-3.5 w-1 bg-indigo-500"></span>
        </div>
        <h2 class="mb-4 text-3xl font-mono font-bold tracking-tight text-slate-900 dark:text-white sm:text-4xl md:text-5xl">
          Sobre Mim
        </h2>
        <p class="mx-auto max-w-2xl text-sm leading-relaxed text-slate-600 dark:text-zinc-400 sm:text-base">
          Um pouco sobre minha trajetória, minha paixão por tecnologia e o que me motiva a construir soluções digitais de alto impacto.
        </p>
      </div>

      <div class="grid grid-cols-1 items-start gap-10 lg:grid-cols-12 lg:gap-14">

        <!-- Coluna Esquerda: Texto Principal (Markdown style) -->
        <div class="lg:col-span-7 border-l-2 border-indigo-500/70 pl-5 sm:pl-7">
          <div class="space-y-6 font-mono text-xs sm:text-sm">

            <div class="flex items-start gap-4 group/line">
              <span class="w-5 select-none text-right text-slate-300 group-hover/line:text-indigo-500 dark:text-zinc-700">01</span>
              <p class="text-slate-600 dark:text-slate-400 font-sans text-sm sm:text-base leading-relaxed">
                Sou <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Bruno Amorim</strong>, desenvolvedor focado em construir aplicações eficientes, limpas e com interfaces intuitivas. Busco transformar lógicas complexas em código bem estruturado seguindo princípios de Clean Code.
              </p>
            </div>

            <div class="flex items-start gap-4 group/line">
              <span class="w-5 select-none text-right text-slate-300 group-hover/line:text-indigo-500 dark:text-zinc-700">02</span>
              <p class="text-slate-600 dark:text-slate-400 font-sans text-sm sm:text-base leading-relaxed">
                Atualmente cursando <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Ciência da Computação</strong> na Uninassau Aracaju. Unindo a base acadêmica teórica com a prática profissional, estagio atualmente na área de TI do laboratório <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Patologika</strong>.
              </p>
            </div>

            <div class="flex items-start gap-4 group/line">
              <span class="w-5 select-none text-right text-slate-300 group-hover/line:text-indigo-500 dark:text-zinc-700">03</span>
              <p class="text-slate-600 dark:text-slate-400 font-sans text-sm sm:text-base leading-relaxed">
                Minhas principais frentes cobrem ecossistemas reativos no front-end com <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Vue.js</strong> e <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Tailwind CSS</strong>, além de soluções integradas no back-end utilizando <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Node.js</strong> e <strong class="font-semibold text-indigo-600 dark:text-indigo-400">Python</strong>.
              </p>
            </div>

          </div>
        </div>

        <!-- Coluna Direita: Cards de Destaque -->
        <div class="grid w-full grid-cols-1 gap-x-6 gap-y-8 sm:grid-cols-2 lg:col-span-5">

          <!-- CARD EDUCAÇÃO -->
          <div class="group space-y-3 border-b border-slate-200 pb-6 transition-colors duration-200 hover:border-indigo-500/50 dark:border-zinc-800 dark:hover:border-indigo-500/50">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-indigo-600 dark:text-indigo-400 font-bold bg-indigo-50 dark:bg-indigo-950/30 px-2 py-0.5 rounded border border-indigo-100 dark:border-indigo-900/40">
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
                  4º Período
                </span>
              </div>
            </div>
          </div>

          <!-- CARD FOCO -->
          <div class="group space-y-3 border-b border-slate-200 pb-6 transition-colors duration-200 hover:border-indigo-500/50 dark:border-zinc-800 dark:hover:border-indigo-500/50">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-indigo-600 dark:text-indigo-400 font-bold bg-indigo-50 dark:bg-indigo-950/30 px-2 py-0.5 rounded border border-indigo-100 dark:border-indigo-900/40">
                [_STACK]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// ENV_FOCUS</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Foco Atual</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Aplicações Web SPA modernas, desenvolvimento Full-stack e microsserviços.
              </p>
            </div>
          </div>


          <!-- eslint-disable-next-line vue/multiline-html-element-content-newline -->
          <!-- CARD ESTÁGIO - Substituindo o card anterior de Diretrizes -->
          <div class="group space-y-3 border-b border-slate-200 pb-6 transition-colors duration-200 hover:border-indigo-500/50 dark:border-zinc-800 dark:hover:border-indigo-500/50">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-indigo-600 dark:text-indigo-400 font-bold bg-indigo-50 dark:bg-indigo-950/30 px-2 py-0.5 rounded border border-indigo-100 dark:border-indigo-900/40">
                [_EXP]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// CURRENT_ROLE</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Estagiário de TI</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Atuação no laboratório de patologia <strong class="font-medium text-slate-800 dark:text-slate-200">Patologika</strong>, focando em suporte, infraestrutura e otimização de fluxos digitais.
              </p>
            </div>
          </div>

          <!-- CARD HOBBIES -->
          <div class="group space-y-3 border-b border-slate-200 pb-6 transition-colors duration-200 hover:border-indigo-500/50 dark:border-zinc-800 dark:hover:border-indigo-500/50">
            <div class="flex items-center justify-between font-mono text-[10px] select-none">
              <span class="text-indigo-600 dark:text-indigo-400 font-bold bg-indigo-50 dark:bg-indigo-950/30 px-2 py-0.5 rounded border border-indigo-100 dark:border-indigo-900/40">
                [_IDLE]
              </span>
              <span class="text-slate-400 dark:text-slate-600">// RUNTIME</span>
            </div>
            <div class="space-y-1">
              <h3 class="font-mono font-bold text-slate-950 dark:text-white text-sm">Hobbies</h3>
              <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
                Violão acústico (MPB), composição musical autoral e jogos de estratégia.
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
