<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="group flex flex-col justify-between overflow-hidden rounded-lg border border-slate-200 bg-white/70 p-5 transition-colors duration-300 hover:border-indigo-500/50 dark:border-zinc-800 dark:bg-zinc-900/35 dark:hover:border-indigo-500/50"
  >
    <div>
      <div class="mb-4 flex items-center justify-between select-none">
        <span
          class="font-mono text-[10px] text-slate-400 dark:text-slate-500 uppercase tracking-wider flex items-center gap-1.5 group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors duration-200"
        >
          <span
            class="h-1.5 w-1.5 rounded-full bg-slate-300 transition-colors group-hover:bg-indigo-500 dark:bg-zinc-700 dark:group-hover:bg-indigo-400"
          ></span>
          {{ certificate.category || 'CERTIFICATE' }}
        </span>

        <span class="font-mono text-[11px] text-slate-400 dark:text-slate-500">
          {{ certificate.date }}
        </span>
      </div>

      <h3
        class="mb-2 text-base font-mono font-bold text-slate-950 transition-colors duration-200 group-hover:text-indigo-600 dark:text-white dark:group-hover:text-indigo-400"
      >
        {{ certificate.title }}
      </h3>

      <p class="mb-4 flex items-center gap-1.5 text-xs font-sans text-slate-600 dark:text-slate-400 sm:text-sm">
        <svg class="w-3.5 h-3.5 text-slate-400 dark:text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
        </svg>
        <span>{{ certificate.issuer }}</span>
      </p>

      <div class="relative mb-5 flex h-36 items-center justify-center overflow-hidden rounded-md border border-slate-200 bg-slate-100 dark:border-zinc-800 dark:bg-zinc-950">
        <img
          v-if="certificate.preview"
          :src="certificate.preview"
          :alt="`Prévia desfocada do certificado ${certificate.title}`"
          class="h-full w-full scale-105 object-cover opacity-75 blur-[5px] transition duration-500 group-hover:scale-110"
        />
        <div v-else class="flex flex-col items-center gap-2 text-slate-400 dark:text-zinc-600">
          <span class="font-mono text-3xl">.pdf</span>
          <span class="font-mono text-[10px] uppercase tracking-widest">document_preview</span>
        </div>
        <div class="absolute inset-0 bg-slate-950/25"></div>
        <span class="absolute rounded border border-white/20 bg-slate-950/60 px-2 py-1 font-mono text-[10px] text-white/90">
          PREVIEW_LOCKED
        </span>
      </div>

      <div
        v-if="certificate.skills && certificate.skills.length"
        class="mb-5 flex flex-wrap gap-1.5 font-mono text-[10px]"
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

    <div class="border-t border-slate-200 pt-4 dark:border-zinc-800">
      <a
        v-if="certificate.link"
        :href="certificate.link"
        target="_blank"
        rel="noopener noreferrer"
        class="flex w-full items-center justify-center gap-2 rounded-md border border-indigo-500/30 bg-indigo-500/5 px-3 py-2 font-mono text-xs text-indigo-600 transition-colors hover:border-indigo-500/60 hover:bg-indigo-500/10 dark:text-indigo-300"
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
