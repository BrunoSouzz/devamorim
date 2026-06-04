<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="home"
    class="min-h-screen flex items-center justify-center bg-slate-50 dark:bg-slate-950 pt-20 pb-16 transition-colors duration-300 relative overflow-hidden"
  >
    <!-- Grid de fundo sutil sincronizado com a seção de contato -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#8080800a_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] bg-size-[14px_24px] pointer-events-none"></div>

    <!-- Linhas Laser Decorativas do Sistema -->
    <div class="absolute top-32 left-0 w-1/3 h-px bg-linear-to-r from-violet-500/0 via-violet-500/20 to-transparent hidden lg:block"></div>
    <div class="absolute bottom-32 right-0 w-1/3 h-px bg-linear-to-l from-purple-500/0 via-purple-500/20 to-transparent hidden lg:block"></div>

    <div class="max-w-6xl w-full mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-12 relative z-10">

      <!-- Bloco de Texto / Shell Core -->
      <div class="flex-1 space-y-6 text-left w-full order-2 md:order-1">

        <!-- Logs de Inicialização -->
        <div class="space-y-1 font-mono text-[11px] text-slate-400 dark:text-slate-500 select-none">
          <div class="flex items-center gap-2">
            <span class="text-violet-500 font-bold">[KERNEL]</span>
            <span>Initializing core_profile_sequence... DONE</span>
          </div>
          <div class="flex items-center gap-2">
            <span class="text-purple-500 font-bold">[ACADEMIC]</span>
            <span>Current scope: Computer Science _</span>
            <span class="w-1 h-3.5 bg-violet-500 dark:bg-purple-500 animate-pulse"></span>
          </div>
        </div>

        <!-- Nome Principal -->
        <div class="space-y-2">
          <h1 class="text-4xl sm:text-6xl font-mono font-black text-slate-950 dark:text-white tracking-tight">
            Bruno Amorim<span class="text-violet-600 dark:text-purple-400">.</span>
          </h1>

          <h2 class="text-2xl sm:text-4xl font-mono font-bold bg-linear-to-r from-violet-600 to-indigo-600 dark:from-purple-400 dark:to-purple-500 bg-clip-text text-transparent tracking-tight">
            &gt; Software &amp; Web Developer
          </h2>
        </div>

        <!-- Terminal Output da Bio -->
        <div class="relative bg-white dark:bg-slate-900/60 border border-slate-200 dark:border-slate-800 p-4 rounded-xl shadow-xs font-mono max-w-xl">
          <div class="absolute top-0 right-4 -translate-y-1/2 bg-slate-100 dark:bg-slate-800 px-2 py-0.5 text-[10px] text-slate-400 dark:text-slate-500 rounded border border-slate-200 dark:border-slate-700/60 select-none">
            STDOUT / BIO_DATA
          </div>

          <p class="text-slate-600 dark:text-slate-400 text-xs sm:text-sm leading-relaxed">
            Estudante de Ciência da Computação focado em projetar e compilar experiências digitais modernas, de alta performance e visualmente limpas. Especializado em converter arquiteturas lógicas complexas em interfaces fluidas usando Vue.js, Tailwind CSS e Node.js.
          </p>
        </div>

        <!-- Botões Operacionais (Scripts Executáveis) -->
        <div class="flex flex-wrap gap-4 pt-2 font-mono text-xs font-bold">
          <a
            href="#projects"
            class="group px-5 py-3 bg-slate-950 dark:bg-white text-white dark:text-slate-950 rounded-lg transition-all duration-200 hover:-translate-y-0.5 shadow-md hover:shadow-violet-500/10 flex items-center gap-2"
          >
            <span>./view_projects --detailed</span>
            <span class="text-violet-400 dark:text-purple-600 font-normal transition-transform group-hover:translate-x-0.5">▶</span>
          </a>

          <a
            href="#contact"
            class="group px-5 py-3 border border-slate-200 dark:border-slate-800 hover:border-violet-500/50 dark:hover:border-purple-500/50 text-slate-600 dark:text-slate-400 hover:text-slate-950 dark:hover:text-white bg-white/40 dark:bg-slate-900/20 rounded-lg transition-all duration-200 hover:-translate-y-0.5 flex items-center gap-2"
          >
            <span>sh contact.sh</span>
          </a>
        </div>
      </div>

      <!-- Container da Imagem de Perfil / Target Scanner -->
      <div class="w-48 h-48 sm:w-64 sm:h-64 shrink-0 order-1 md:order-2 group relative">
        <!-- Glow de Fundo Sincronizado -->
        <div class="absolute inset-0 bg-linear-to-tr from-violet-500 to-purple-500 rounded-2xl blur-2xl opacity-15 group-hover:opacity-25 transition-opacity duration-300"></div>

        <!-- Janela de Inspeção da Imagem -->
        <div class="w-full h-full rounded-2xl border border-slate-200 dark:border-slate-800 p-2 relative z-10 bg-white/60 dark:bg-slate-900/40 backdrop-blur-xs transition-colors duration-300">

          <!-- Cantos Simulando Mira/Scanner de Código -->
          <div class="absolute top-0 left-0 w-3 h-3 border-t-2 border-l-2 border-violet-500 dark:border-purple-500 rounded-tl-xl"></div>
          <div class="absolute top-0 right-0 w-3 h-3 border-t-2 border-r-2 border-violet-500 dark:border-purple-500 rounded-tr-xl"></div>
          <div class="absolute bottom-0 left-0 w-3 h-3 border-b-2 border-l-2 border-violet-500 dark:border-purple-500 rounded-bl-xl"></div>
          <div class="absolute bottom-0 right-0 w-3 h-3 border-b-2 border-r-2 border-violet-500 dark:border-purple-500 rounded-br-xl"></div>

          <!-- Div de corte da imagem -->
          <div class="w-full h-full rounded-xl flex items-center justify-center overflow-hidden relative bg-slate-100 dark:bg-slate-950">
            <img
              src="@/assets/images/Profile.jpg"
              alt="Foto de perfil de Bruno Amorim"
              class="w-full h-full object-cover object-top rounded-xl scale-102 group-hover:scale-105 transition-transform duration-500 brightness-95 dark:brightness-90 contrast-105"
            />

            <!-- Linha de Scan Dinâmica (Aparece no Hover) -->
            <div class="absolute inset-x-0 h-0.5 bg-linear-to-r from-transparent via-violet-500/40 to-transparent top-0 opacity-0 group-hover:opacity-100 group-hover:top-full transition-all duration-1000 ease-in-out pointer-events-none"></div>
          </div>
        </div>

        <!-- Identificador Inferior Estilizado -->
        <div class="absolute -bottom-4 left-1/2 -translate-x-1/2 font-mono text-[9px] font-bold text-slate-400 dark:text-slate-600 tracking-wider whitespace-nowrap bg-slate-50 dark:bg-slate-950 px-2 select-none z-20 transition-colors duration-300 flex items-center gap-1.5">
          <span class="w-1 h-1 rounded-full bg-violet-500 animate-pulse"></span>
          <span>B_AMORIM_RENDER.SYS</span>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
</script>
