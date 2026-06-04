<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="group relative bg-white dark:bg-slate-900/40 rounded-xl border border-slate-200 dark:border-slate-900 p-5 flex flex-col justify-between transition-all duration-300 hover:-translate-y-1 hover:border-violet-500/40 dark:hover:border-purple-500/40 hover:shadow-xl hover:shadow-violet-500/5 dark:hover:shadow-purple-500/5 overflow-hidden"
  >
    <!-- Brilho de Alocação de Recurso (Hover) -->
    <div class="absolute -inset-px bg-linear-to-br from-violet-500/5 to-purple-500/5 rounded-xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 blur-xs -z-10 pointer-events-none"></div>

    <div>
      <!-- Header do Card: Metadados e Links -->
      <div class="flex items-center justify-between mb-4 select-none">
        <span class="font-mono text-[10px] text-slate-400 dark:text-slate-500 uppercase tracking-wider flex items-center gap-1.5 group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors duration-200">
          <span class="w-1 h-1 rounded-full bg-slate-300 dark:bg-slate-700 group-hover:bg-violet-500 dark:group-hover:bg-purple-400 animate-pulse"></span>
          PROJECT_ARTIFACT
        </span>

        <!-- Botões de Ação Estilizados de Terminal -->
        <div class="flex items-center gap-2 font-mono text-[11px]">
          <a
            v-if="githubLink"
            :href="githubLink"
            target="_blank"
            class="flex items-center gap-1 px-2 py-0.5 bg-slate-50 dark:bg-slate-950 border border-slate-200 dark:border-slate-900 hover:border-violet-500/40 dark:hover:border-purple-500/40 text-slate-500 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 rounded-md transition-all duration-200 hover:-translate-y-0.5"
          >
            <span class="text-violet-500 dark:text-purple-400 font-bold">~</span>
            <span>git</span>
          </a>

          <a
            v-if="liveLink"
            :href="liveLink"
            target="_blank"
            class="flex items-center gap-1 px-2 py-0.5 bg-slate-50 dark:bg-slate-950 border border-slate-200 dark:border-slate-900 hover:border-violet-500/40 dark:hover:border-purple-500/40 text-slate-500 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 rounded-md transition-all duration-200 hover:-translate-y-0.5"
          >
            <span class="text-violet-500 dark:text-purple-400 font-bold">~</span>
            <span>live</span>
          </a>
        </div>
      </div>

      <!-- Título do Projeto (Identidade Mono) -->
      <h3 class="text-base font-mono font-bold text-slate-950 dark:text-white mb-2 group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors duration-200">
        {{ title }}
      </h3>

      <!-- Descrição do Projeto -->
      <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
        {{ description }}
      </p>
    </div>

    <!-- Footer: Dependências/Tags Técnicas com Syntax Highlighting -->
    <div class="flex flex-wrap gap-1.5 mt-5 pt-3.5 border-t border-slate-100 dark:border-slate-900 font-mono text-[10px]">
      <span
        v-for="tag in tags"
        :key="tag"
        :class="[
          'px-2 py-0.5 rounded border tracking-wide select-none transition-all duration-200 font-bold',
          getThemeClass(tag)
        ]"
      >
        {{ tag }}
      </span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  tags: {
    type: Array,
    default: () => []
  },
  githubLink: {
    type: String,
    default: ''
  },
  liveLink: {
    type: String,
    default: ''
  }
})

// Dicionário de estilos focado em Syntax Highlighting legível em Light e Dark Mode
const techThemes = {
  python: 'text-blue-600 dark:text-blue-400 bg-blue-500/5 dark:bg-blue-500/10 border-blue-200/60 dark:border-blue-500/20',
  javascript: 'text-amber-600 dark:text-amber-400 bg-amber-500/5 dark:bg-amber-500/10 border-amber-200/80 dark:border-amber-500/20',
  flask: 'text-slate-600 dark:text-slate-300 bg-slate-500/5 dark:bg-slate-400/10 border-slate-200 dark:border-slate-700',
  html: 'text-orange-600 dark:text-orange-400 bg-orange-500/5 dark:bg-orange-500/10 border-orange-200 dark:border-orange-500/20',
  css: 'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20',
  'gemini api': 'text-fuchsia-600 dark:text-fuchsia-400 bg-fuchsia-500/5 dark:bg-fuchsia-500/10 border-fuchsia-200 dark:border-fuchsia-500/20',
  postgresql: 'text-cyan-600 dark:text-cyan-400 bg-cyan-500/5 dark:bg-cyan-500/10 border-cyan-200 dark:border-cyan-500/20',
  mysql: 'text-sky-600 dark:text-sky-400 bg-sky-500/5 dark:bg-sky-500/10 border-sky-200 dark:border-sky-500/20',
  dart: 'text-teal-600 dark:text-teal-400 bg-teal-500/5 dark:bg-teal-500/10 border-teal-200 dark:border-teal-500/20',
  flutter: 'text-sky-500 dark:text-sky-400 bg-sky-500/5 dark:bg-sky-500/10 border-sky-200 dark:border-sky-500/20',
  'node.js': 'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
  vue: 'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
  'vue.js': 'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
  tailwindcss: 'text-teal-600 dark:text-teal-400 bg-teal-500/5 dark:bg-teal-500/10 border-teal-200 dark:border-teal-500/20',
  express: 'text-gray-600 dark:text-gray-400 bg-gray-500/5 dark:bg-gray-500/10 border-gray-200 dark:border-gray-500/20',
}

// Retorna a cor específica ou um roxo padrão do sistema caso a tecnologia seja nova
const getThemeClass = (tag) => {
  const normalized = tag.toLowerCase().trim()
  return techThemes[normalized] || 'text-violet-600 dark:text-purple-400 bg-violet-500/5 dark:bg-purple-500/10 border-violet-200 dark:border-purple-500/20'
}
</script>
