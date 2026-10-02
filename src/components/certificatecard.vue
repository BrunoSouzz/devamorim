<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="group relative bg-white dark:bg-slate-900/40 rounded-xl border border-slate-200 dark:border-slate-900 p-5 flex flex-col justify-between transition-all duration-300 hover:-translate-y-1 hover:border-indigo-500/40 dark:hover:border-indigo-500/40 hover:shadow-xl hover:shadow-indigo-500/5 dark:hover:shadow-indigo-500/5 overflow-hidden"
  >
    <!-- Brilho de Alocação de Recurso (Hover) -->
    <div
      class="absolute -inset-px bg-linear-to-br from-indigo-500/5 to-purple-500/5 rounded-xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 blur-xs -z-10 pointer-events-none"
    ></div>

    <div>
      <!-- Header do Card: Categoria & Ano -->
      <div class="flex items-center justify-between mb-4 select-none">
        <span
          class="font-mono text-[10px] text-slate-400 dark:text-slate-500 uppercase tracking-wider flex items-center gap-1.5 group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors duration-200"
        >
          <span
            class="w-1 h-1 rounded-full bg-slate-300 dark:bg-slate-700 group-hover:bg-indigo-500 dark:group-hover:bg-indigo-400 animate-pulse"
          ></span>
          {{ certificate.category || 'CERTIFICATE' }}
        </span>

        <span class="font-mono text-[11px] text-slate-400 dark:text-slate-500">
          {{ certificate.date }}
        </span>
      </div>

      <!-- Título do Certificado -->
      <h3
        class="text-base font-mono font-bold text-slate-950 dark:text-white mb-2 group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors duration-200"
      >
        {{ certificate.title }}
      </h3>

      <!-- Emissor / Instituição -->
      <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 font-sans mb-4 flex items-center gap-1.5">
        <svg class="w-3.5 h-3.5 text-slate-400 dark:text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
        </svg>
        <span>{{ certificate.issuer }}</span>
      </p>

      <!-- Tags de Tecnologias com o mesmo Syntax Highlighting do projectcard -->
      <div
        v-if="certificate.skills && certificate.skills.length"
        class="flex flex-wrap gap-1.5 mb-5 font-mono text-[10px]"
      >
        <span
          v-for="skill in certificate.skills"
          :key="skill"
          :class="[
            'px-2 py-0.5 rounded border tracking-wide select-none transition-all duration-200 font-bold',
            getThemeClass(skill),
          ]"
        >
          {{ skill }}
        </span>
      </div>
    </div>

    <!-- Botão de Ação Estilizado de Terminal -->
    <div class="pt-3.5 border-t border-slate-100 dark:border-slate-900">
      <a
        v-if="certificate.link"
        :href="certificate.link"
        target="_blank"
        rel="noopener noreferrer"
        class="flex items-center justify-center gap-2 w-full px-3 py-2 bg-slate-50 dark:bg-slate-950 border border-slate-200 dark:border-slate-900 hover:border-indigo-500/40 dark:hover:border-indigo-500/40 text-slate-600 dark:text-slate-400 hover:text-indigo-600 dark:hover:text-indigo-400 rounded-md transition-all duration-200 font-mono text-xs hover:-translate-y-0.5"
      >
        <span class="text-indigo-500 dark:text-indigo-400 font-bold">~</span>
        <span>{{ certificate.linkType === 'linkedin' ? 'view_linkedin' : 'view_pdf' }}</span>
      </a>
    </div>
  </div>
</template>

<script setup>
defineProps({
  certificate: {
    type: Object,
    required: true,
  },
})

// Dicionário de estilos compartilhado com o projectcard
const techThemes = {
  python: 'text-blue-600 dark:text-blue-400 bg-blue-500/5 dark:bg-blue-500/10 border-blue-200/60 dark:border-blue-500/20',
  javascript: 'text-amber-600 dark:text-amber-400 bg-amber-500/5 dark:bg-amber-500/10 border-amber-200/80 dark:border-amber-500/20',
  html: 'text-orange-600 dark:text-orange-400 bg-orange-500/5 dark:bg-orange-500/10 border-orange-200 dark:border-orange-500/20',
  css: 'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20',
  postgresql: 'text-cyan-600 dark:text-cyan-400 bg-cyan-500/5 dark:bg-cyan-500/10 border-cyan-200 dark:border-cyan-500/20',
  dart: 'text-teal-600 dark:text-teal-400 bg-teal-500/5 dark:bg-teal-500/10 border-teal-200 dark:border-teal-500/20',
  flutter: 'text-sky-500 dark:text-sky-400 bg-sky-500/5 dark:bg-sky-500/10 border-sky-200 dark:border-sky-500/20',
  firebase: 'text-amber-500 dark:text-amber-400 bg-amber-500/5 dark:bg-amber-500/10 border-amber-200 dark:border-amber-500/20',
  cybersecurity: 'text-red-600 dark:text-red-400 bg-red-500/5 dark:bg-red-500/10 border-red-200/60 dark:border-red-500/20',
  'network security': 'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20',
  'ethical hacking': 'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
}

const getThemeClass = (tag) => {
  const normalized = tag.toLowerCase().trim()
  return (
    techThemes[normalized] ||
    'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20'
  )
}
</script>
