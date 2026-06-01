<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="inicio"
    class="min-h-screen flex items-center justify-center bg-slate-50 dark:bg-slate-900 pt-8 transition-colors duration-300 py-20 relative overflow-hidden"
  >
    <div class="absolute top-24 right-12 text-slate-200 dark:text-slate-800/60 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      + INIT.SYS_MAIN_0x1A01
    </div>
    <div class="absolute bottom-16 left-12 text-slate-200 dark:text-slate-800/60 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      // RUNNING_VERSION_V2.0
    </div>

    <div
      class="max-w-4xl mx-auto px-6 text-center md:text-left flex flex-col md:flex-row items-center gap-12 relative z-10"
    >
      <div class="flex-1 space-y-6 relative">
        <div class="flex items-center gap-2 text-purple-600 dark:text-purple-400 font-mono text-sm tracking-wider justify-center md:justify-start group/step">
          <span class="text-xs text-slate-300 dark:text-slate-600 select-none group-hover/step:text-purple-500 transition-colors duration-300">[00]</span>
          <span>console.log("Olá, meu nome é");</span>
        </div>

        <h1
          class="text-4xl sm:text-6xl font-extrabold text-slate-900 dark:text-white tracking-tight"
        >
          Bruno Amorim.
        </h1>

        <h2
          class="text-3xl sm:text-5xl font-bold bg-linear-to-r from-purple-600 to-indigo-600 dark:from-purple-400 dark:to-purple-500 bg-clip-text text-transparent tracking-tight"
        >
          Desenvolvedor Software & Web.
        </h2>

        <div class="relative border-l-2 border-slate-200 dark:border-slate-800 pl-4 py-1 text-left max-w-xl mx-auto md:mx-0">
          <p class="text-slate-600 dark:text-slate-400 text-base sm:text-lg leading-relaxed">
            Sou estudante de Ciência da Computação focado em construir experiências digitais modernas,
            eficientes e visualmente incríveis, utilizando tecnologias como Vue.js, Tailwind CSS e
            Node.js.
          </p>
        </div>

        <div class="flex flex-wrap justify-center md:justify-start gap-4 pt-4 font-mono text-sm">
          <a
            href="#projetos"
            class="group px-6 py-3 bg-purple-500 hover:bg-purple-600 text-slate-950 font-bold rounded-lg shadow-lg shadow-purple-500/20 transition-all hover:-translate-y-0.5 flex items-center gap-2"
          >
            <span>Ver meus projetos</span>
            <span class="text-xs opacity-70 group-hover:translate-x-0.5 transition-transform">-></span>
          </a>
          <a
            href="#contato"
            class="px-6 py-3 border border-slate-300 dark:border-slate-700 hover:border-purple-500 dark:hover:border-purple-400 text-slate-600 dark:text-slate-300 hover:text-purple-600 dark:hover:text-white font-medium rounded-lg transition-all hover:-translate-y-0.5"
          >
            ./contato.sh
          </a>
        </div>
      </div>

      <div class="relative w-48 h-48 sm:w-64 sm:h-64 shrink-0 group mt-4 md:mt-0">
        <div
          class="absolute inset-0 bg-linear-to-tr from-purple-500 to-indigo-500 rounded-2xl blur-2xl opacity-20 group-hover:opacity-35 transition-opacity duration-300 animate-pulse"
        ></div>

        <div
          class="w-full h-full rounded-2xl border border-slate-200 dark:border-slate-800 p-2 relative z-10 bg-white/40 dark:bg-slate-900/40 backdrop-blur-xs transition-colors duration-300"
        >
          <div class="absolute top-0 left-0 w-4 h-4 border-t-2 border-l-2 border-purple-500 rounded-tl-2xl"></div>
          <div class="absolute top-0 right-0 w-4 h-4 border-t-2 border-r-2 border-purple-500 rounded-tr-2xl"></div>
          <div class="absolute bottom-0 left-0 w-4 h-4 border-b-2 border-l-2 border-purple-500 rounded-bl-2xl"></div>
          <div class="absolute bottom-0 right-0 w-4 h-4 border-b-2 border-r-2 border-purple-500 rounded-br-2xl"></div>

          <div
            class="w-full h-full rounded-xl flex items-center justify-center overflow-hidden relative"
          >
            <img
              src="@/assets/images/Profile.jpg"
              alt="Foto de perfil de Bruno Amorim"
              class="w-full h-full object-cover object-top rounded-xl group-hover:scale-105 transition-transform duration-500"
            />
            <div class="absolute inset-0 bg-linear-to-b from-transparent via-purple-500/5 to-transparent pointer-events-none opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </div>
        </div>

        <div class="absolute -bottom-5 left-1/2 -translate-x-1/2 font-mono text-[10px] text-slate-400 dark:text-slate-600 tracking-widest whitespace-nowrap bg-slate-50 dark:bg-slate-900 px-2 select-none z-20 transition-colors duration-300">
          SYS.TARGET_IMG // ACTIVE
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
</script>
