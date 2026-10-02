<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="home"
    class="relative flex min-h-screen items-center justify-center overflow-hidden bg-slate-50 pt-20 pb-16 transition-colors duration-300 dark:bg-[#09090b]"
  >
    <div class="relative z-10 mx-auto flex w-full max-w-6xl flex-col items-center gap-12 px-6 md:flex-row md:justify-between md:gap-20">
      <div class="order-2 w-full max-w-2xl space-y-7 text-left md:order-1">
        <div class="flex items-center gap-2 font-mono text-[11px] text-slate-400 dark:text-zinc-500">
          <span class="text-indigo-500">bruno@portfolio:~$</span>
          <span>whoami</span>
          <span class="terminal-blink h-3.5 w-1 bg-indigo-500"></span>
        </div>

        <div class="space-y-3">
          <h1 class="text-4xl font-mono font-black tracking-tight text-slate-950 dark:text-white sm:text-6xl">
            Bruno Amorim<span class="text-indigo-600 dark:text-indigo-400">.</span>
          </h1>
          <h2 class="text-2xl font-mono font-bold tracking-tight text-indigo-600 dark:text-indigo-400 sm:text-4xl">
            Software &amp; Web Developer
          </h2>
        </div>

        <p class="max-w-xl text-sm leading-7 text-slate-600 dark:text-zinc-400 sm:text-base">
          Estudante de Ciência da Computação focado em criar experiências digitais modernas, performáticas e visualmente limpas com Vue.js, Tailwind CSS e Node.js.
        </p>

        <div class="flex flex-wrap gap-3 pt-1 font-mono text-xs font-bold">
          <a
            href="#projetos"
            class="group flex items-center gap-2 rounded-lg bg-slate-950 px-4 py-2.5 text-white transition-colors hover:bg-indigo-600 dark:bg-white dark:text-slate-950 dark:hover:bg-indigo-200"
          >
            <span>./view_projects</span>
            <span class="font-normal text-indigo-300 transition-transform group-hover:translate-x-0.5 dark:text-indigo-600">→</span>
          </a>

          <a
            href="#contact"
            class="flex items-center gap-2 rounded-lg border border-slate-200 bg-white/60 px-4 py-2.5 text-slate-600 transition-colors hover:border-indigo-400 hover:text-indigo-600 dark:border-zinc-800 dark:bg-zinc-900/40 dark:text-zinc-400 dark:hover:border-indigo-400 dark:hover:text-indigo-300"
          >
            <span>sh contact.sh</span>
          </a>
        </div>
      </div>

      <div class="group relative order-1 shrink-0 md:order-2">
        <div class="absolute -inset-5 rounded-3xl bg-indigo-500/10 blur-2xl transition-opacity duration-300 group-hover:bg-indigo-500/15"></div>
        <div class="relative h-52 w-52 overflow-hidden rounded-2xl border border-slate-200 bg-white p-1.5 shadow-xl shadow-slate-950/5 transition-colors dark:border-zinc-800 dark:bg-zinc-900 sm:h-64 sm:w-64">
          <img
            src="@/assets/images/Profile.jpg"
            alt="Foto de perfil de Bruno Amorim"
            class="h-full w-full rounded-xl object-cover object-top brightness-95 contrast-105 transition-transform duration-500 group-hover:scale-105 dark:brightness-90"
          />
        </div>
        <span class="absolute -bottom-3 left-1/2 -translate-x-1/2 whitespace-nowrap bg-slate-50 px-2 font-mono text-[9px] font-bold tracking-wider text-slate-400 dark:bg-[#09090b] dark:text-zinc-500">
          AVAILABLE_FOR_BUILD
        </span>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
