<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="about"
    class="py-20 bg-white dark:bg-slate-900 text-slate-900 dark:text-white scroll-mt-20 transition-colors duration-300 relative overflow-hidden"
  >
    <div class="absolute top-8 left-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden sm:block">
      + SYS.LOC_0x7A2F
    </div>
    <div class="absolute bottom-8 right-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden sm:block">
      // SEC_ABOUT_END
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">
      
      <div class="flex flex-col items-center text-center mb-16">
        <div class="flex items-center gap-1.5 text-violet-600 dark:text-violet-400 font-mono text-sm tracking-widest uppercase mb-2">
          <span>&lt;</span>
          <span>Conheça-me</span>
          <span class="animate-pulse">/&gt;</span>
        </div>
        <h2 class="text-3xl sm:text-4xl font-extrabold text-slate-900 dark:text-white tracking-tight">
          Sobre Mim
        </h2>
        <div class="h-0.5 w-24 bg-linear-to-r from-transparent via-violet-500 to-transparent mt-4"></div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        
        <div class="lg:col-span-7 space-y-6 relative border-l border-slate-200 dark:border-slate-800/80 pl-6 sm:pl-8 py-2">
          <div class="absolute left-[-4.5px] top-0 w-2 h-2 rounded-full bg-violet-500"></div>
          <div class="absolute left-[-4.5px] bottom-0 w-2 h-2 rounded-full bg-slate-300 dark:bg-slate-700"></div>
          
          <div class="flex items-start gap-4 group/text">
            <span class="font-mono text-xs text-slate-300 dark:text-slate-600 pt-1.5 select-none group-hover/text:text-violet-500 dark:group-hover/text:text-violet-400 transition-colors duration-300">[01]</span>
            <p class="text-slate-600 dark:text-slate-400 text-base sm:text-lg leading-relaxed">
              Olá! Sou o <strong class="text-slate-900 dark:text-white font-semibold group-hover/text:text-violet-600 dark:group-hover/text:text-violet-400 transition-colors duration-300">Bruno Amorim</strong>, um
              desenvolvedor focado em criar soluções digitais modernas, fluidas e visualmente
              impactantes. Minha jornada na tecnologia é movida pela curiosidade de entender como as
              coisas funcionam sob o capô e pela paixão de transformar linhas de código em
              experiências incríveis.
            </p>
          </div>

          <div class="flex items-start gap-4 group/text">
            <span class="font-mono text-xs text-slate-300 dark:text-slate-600 pt-1.5 select-none group-hover/text:text-violet-500 dark:group-hover/text:text-violet-400 transition-colors duration-300">[02]</span>
            <p class="text-slate-600 dark:text-slate-400 text-base sm:text-lg leading-relaxed">
              Atualmente, estou cursando
              <strong class="text-violet-600 dark:text-violet-400 font-semibold">Ciência da Computação</strong> na
              Uninassau Aracaju. No ambiente acadêmico e em projetos pessoais, dedico-me profundamente
              ao estudo de estruturas de dados, algoritmos e boas práticas de engenharia de software
              para construir códigos limpos e eficientes.
            </p>
          </div>

          <div class="flex items-start gap-4 group/text">
            <span class="font-mono text-xs text-slate-300 dark:text-slate-600 pt-1.5 select-none group-hover/text:text-violet-500 dark:group-hover/text:text-violet-400 transition-colors duration-300">[03]</span>
            <p class="text-slate-600 dark:text-slate-400 text-base sm:text-lg leading-relaxed">
              No dia a dia, divido meu foco principal entre duas frentes: o ecossistema Web
              (utilizando <strong class="text-slate-900 dark:text-white font-semibold">Vue.js</strong> e
              <strong class="text-slate-900 dark:text-white font-semibold">Tailwind CSS</strong>) e o desenvolvimento
              Back-End multiplataforma com o
              <strong class="text-slate-900 dark:text-white font-semibold">Node.js</strong>. Adoro o desafio de
              transformar designs estáticos em interfaces totalmente interativas, responsivas e
              funcionais.
            </p>
          </div>
        </div>

        <div class="lg:col-span-5 grid grid-cols-1 sm:grid-cols-2 gap-4 w-full">
          
          <div
            class="group relative p-6 bg-slate-50 dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-4 hover:border-violet-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-violet-500/5 overflow-hidden"
          >
            <div
              class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"
            ></div>

            <div class="flex items-center justify-between">
              <div
                class="w-10 h-10 rounded-lg bg-white dark:bg-slate-900/90 border border-slate-200 dark:border-slate-800 flex items-center justify-center text-lg group-hover:border-violet-500/30 group-hover:bg-violet-50 dark:group-hover:bg-violet-950/20 transition-colors duration-300"
              >
                🎓
              </div>
              <span
                class="font-mono text-xs text-slate-400 dark:text-slate-600 group-hover:text-violet-600 dark:group-hover:text-violet-400 transition-colors duration-300"
              >// 01</span>
            </div>

            <div class="space-y-1.5">
              <h3
                class="font-bold text-slate-900 dark:text-white text-base tracking-tight group-hover:text-violet-600 dark:group-hover:text-violet-300 transition-colors duration-300"
              >
                Educação
              </h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 leading-snug">
                Ciência da Computação<br />
                <span class="text-xs text-slate-400 dark:text-slate-500 font-mono">Uninassau Aracaju</span><br />
                <span class="text-xs text-emerald-600 dark:text-emerald-400/90 font-mono flex items-center gap-1 mt-1">
                  <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 dark:bg-emerald-400 animate-pulse"></span> 3º
                  Período
                </span>
              </p>
            </div>
          </div>

          <div
            class="group relative p-6 bg-slate-50 dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-4 hover:border-violet-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-violet-500/5 overflow-hidden"
          >
            <div
              class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"
            ></div>

            <div class="flex items-center justify-between">
              <div
                class="w-10 h-10 rounded-lg bg-white dark:bg-slate-900/90 border border-slate-200 dark:border-slate-800 flex items-center justify-center text-lg group-hover:border-violet-500/30 group-hover:bg-violet-50 dark:group-hover:bg-violet-950/20 transition-colors duration-300"
              >
                💻
              </div>
              <span
                class="font-mono text-xs text-slate-400 dark:text-slate-600 group-hover:text-violet-600 dark:group-hover:text-violet-400 transition-colors duration-300"
              >// 02</span>
            </div>

            <div class="space-y-1.5">
              <h3
                class="font-bold text-slate-900 dark:text-white text-base tracking-tight group-hover:text-violet-600 dark:group-hover:text-violet-300 transition-colors duration-300"
              >
                Foco Atual
              </h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 leading-snug">
                Aplicações Web SPA e apps Back-End robustos.
              </p>
            </div>
          </div>

          <div
            class="group relative p-6 bg-slate-50 dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-4 hover:border-violet-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-violet-500/5 overflow-hidden"
          >
            <div
              class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"
            ></div>

            <div class="flex items-center justify-between">
              <div
                class="w-10 h-10 rounded-lg bg-white dark:bg-slate-900/90 border border-slate-200 dark:border-slate-800 flex items-center justify-center text-lg group-hover:border-violet-500/30 group-hover:bg-violet-50 dark:group-hover:bg-violet-950/20 transition-colors duration-300"
              >
                🧩
              </div>
              <span
                class="font-mono text-xs text-slate-400 dark:text-slate-600 group-hover:text-violet-600 dark:group-hover:text-violet-400 transition-colors duration-300"
              >// 03</span>
            </div>

            <div class="space-y-1.5">
              <h3
                class="font-bold text-slate-900 dark:text-white text-base tracking-tight group-hover:text-violet-600 dark:group-hover:text-violet-300 transition-colors duration-300"
              >
                Mindset
              </h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 leading-snug">
                Código limpo, componentização e resolução de problemas estruturados.
              </p>
            </div>
          </div>

          <div
            class="group relative p-6 bg-slate-50 dark:bg-slate-950/60 backdrop-blur-xs border border-slate-200 dark:border-slate-800/80 rounded-xl space-y-4 hover:border-violet-500/60 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-violet-500/5 overflow-hidden"
          >
            <div
              class="absolute top-0 left-0 w-full h-0.5 bg-linear-to-r from-transparent via-violet-500 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"
            ></div>

            <div class="flex items-center justify-between">
              <div
                class="w-10 h-10 rounded-lg bg-white dark:bg-slate-900/90 border border-slate-200 dark:border-slate-800 flex items-center justify-center text-lg group-hover:border-violet-500/30 group-hover:bg-violet-50 dark:group-hover:bg-violet-950/20 transition-colors duration-300"
              >
                🎸
              </div>
              <span
                class="font-mono text-xs text-slate-400 dark:text-slate-600 group-hover:text-violet-600 dark:group-hover:text-violet-400 transition-colors duration-300"
              >// 04</span>
            </div>

            <div class="space-y-1.5">
              <h3
                class="font-bold text-slate-900 dark:text-white text-base tracking-tight group-hover:text-violet-600 dark:group-hover:text-violet-300 transition-colors duration-300"
              >
                Hobbies
              </h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 leading-snug">
                Composição musical, violão (MPB) e jogos de estratégia.
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