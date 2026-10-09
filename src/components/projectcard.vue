<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="group flex flex-col justify-between overflow-hidden rounded-lg border border-slate-200 bg-white/70 p-5 transition-colors duration-300 hover:border-indigo-500/50 dark:border-zinc-800 dark:bg-zinc-900/35 dark:hover:border-indigo-500/50"
    role="button"
    tabindex="0"
    @click="emit('open')"
    @keydown.enter="emit('open')"
    @keydown.space.prevent="emit('open')"
  >
    <div>
      <!-- Header do Card -->
      <div class="mb-4 flex items-center select-none">
        <span
          class="font-mono text-[10px] text-slate-400 dark:text-slate-500 uppercase tracking-wider flex items-center gap-1.5 group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors duration-200"
        >
          <span
            class="h-1.5 w-1.5 rounded-full bg-slate-300 transition-colors group-hover:bg-indigo-500 dark:bg-zinc-700 dark:group-hover:bg-indigo-400"
          ></span>
          PROJECT_ARTIFACT
        </span>

      </div>

      <!-- Título do Projeto (Identidade Mono) -->
      <h3
        class="mb-2 text-base font-mono font-bold text-slate-950 transition-colors duration-200 group-hover:text-indigo-600 dark:text-white dark:group-hover:text-indigo-400"
      >
        {{ title }}
      </h3>

      <!-- Descrição do Projeto -->
      <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed font-sans">
        {{ description }}
      </p>
    </div>

    <!-- Footer: Dependências/Tags Técnicas com Syntax Highlighting -->
    <div
      class="mt-5 flex flex-wrap gap-1.5 border-t border-slate-200 pt-4 font-mono text-[10px] dark:border-zinc-800"
    >
      <span
        v-for="tag in tags"
        :key="tag"
        :class="[
          'px-2 py-0.5 rounded border tracking-wide select-none transition-all duration-200 font-bold',
          getThemeClass(tag),
        ]"
      >
        {{ tag }}
      </span>
    </div>
  </div>
</template>

<script setup>
const emit = defineEmits(['open'])

defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  tags: {
    type: Array,
    default: () => [],
  },
})

// Dicionário de estilos focado em Syntax Highlighting legível em Light e Dark Mode
const techThemes = {
  python:
    'text-blue-600 dark:text-blue-400 bg-blue-500/5 dark:bg-blue-500/10 border-blue-200/60 dark:border-blue-500/20',
  javascript:
    'text-amber-600 dark:text-amber-400 bg-amber-500/5 dark:bg-amber-500/10 border-amber-200/80 dark:border-amber-500/20',
  flask:
    'text-slate-600 dark:text-slate-300 bg-slate-500/5 dark:bg-slate-400/10 border-slate-200 dark:border-slate-700',
  html: 'text-orange-600 dark:text-orange-400 bg-orange-500/5 dark:bg-orange-500/10 border-orange-200 dark:border-orange-500/20',
  css: 'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20',
  'gemini api':
    'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20',
  postgresql:
    'text-cyan-600 dark:text-cyan-400 bg-cyan-500/5 dark:bg-cyan-500/10 border-cyan-200 dark:border-cyan-500/20',
  mysql:
    'text-sky-600 dark:text-sky-400 bg-sky-500/5 dark:bg-sky-500/10 border-sky-200 dark:border-sky-500/20',
  dart: 'text-teal-600 dark:text-teal-400 bg-teal-500/5 dark:bg-teal-500/10 border-teal-200 dark:border-teal-500/20',
  flutter:
    'text-sky-500 dark:text-sky-400 bg-sky-500/5 dark:bg-sky-500/10 border-sky-200 dark:border-sky-500/20',
  'node.js':
    'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
  vue: 'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
  'vue.js':
    'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200 dark:border-emerald-500/20',
  tailwindcss:
    'text-teal-600 dark:text-teal-400 bg-teal-500/5 dark:bg-teal-500/10 border-teal-200 dark:border-teal-500/20',
  express:
    'text-gray-600 dark:text-gray-400 bg-gray-500/5 dark:bg-gray-500/10 border-gray-200 dark:border-gray-500/20',
  java: 'text-red-600 dark:text-red-400 bg-red-500/5 dark:bg-red-500/10 border-red-200/60 dark:border-red-500/20',
  'spring boot':
    'text-green-600 dark:text-green-400 bg-green-500/5 dark:bg-green-500/10 border-green-200/60 dark:border-green-500/20',

  'spring data jpa':
    'text-emerald-600 dark:text-emerald-400 bg-emerald-500/5 dark:bg-emerald-500/10 border-emerald-200/60 dark:border-emerald-500/20',

  jpa: 'text-orange-600 dark:text-orange-400 bg-orange-500/5 dark:bg-orange-500/10 border-orange-200/60 dark:border-orange-500/20',

  'rest api':
    'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200/60 dark:border-indigo-500/20',
}

// Retorna a cor específica ou um roxo padrão do sistema caso a tecnologia seja nova
const getThemeClass = (tag) => {
  const normalized = tag.toLowerCase().trim()
  return (
    techThemes[normalized] ||
    'text-indigo-600 dark:text-indigo-400 bg-indigo-500/5 dark:bg-indigo-500/10 border-indigo-200 dark:border-indigo-500/20'
  )
}
</script>
