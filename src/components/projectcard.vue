<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="group relative bg-white dark:bg-slate-900/40 rounded-xl border border-slate-200 dark:border-slate-800/80 p-6 flex flex-col justify-between transition-all duration-300 hover:-translate-y-1.5 hover:border-violet-500/40 dark:hover:border-purple-500/40 hover:shadow-xl hover:shadow-violet-500/5 dark:hover:shadow-purple-500/5 overflow-hidden"
  >
    <div class="absolute -inset-px bg-linear-to-br from-violet-500/10 to-purple-500/10 rounded-xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 blur-sm -z-10"></div>

    <div>
      <div class="flex items-center justify-between mb-4">
        <span class="font-mono text-xs text-slate-400 dark:text-slate-600 select-none group-hover:text-violet-500 dark:group-hover:text-purple-500 transition-colors duration-300">
          [project_log]
        </span>

        <div class="flex items-center gap-2 font-mono text-xs">
          <a
            v-if="githubLink"
            :href="githubLink"
            target="_blank"
            class="flex items-center gap-1 px-2.5 py-1 bg-slate-100 hover:bg-violet-600/10 dark:bg-slate-950 dark:hover:bg-purple-500/10 border border-slate-200/80 dark:border-slate-800/80 hover:border-violet-500/50 dark:hover:border-purple-500/50 text-slate-600 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 rounded-md shadow-xs transition-all duration-200 hover:-translate-y-0.5"
          >
            <span class="text-violet-400 dark:text-purple-500 font-bold transition-colors duration-200">~/</span>
            <span class="font-medium">git</span>
          </a>

          <a
            v-if="liveLink"
            :href="liveLink"
            target="_blank"
            class="flex items-center gap-1 px-2.5 py-1 bg-slate-100 hover:bg-violet-600/10 dark:bg-slate-950 dark:hover:bg-purple-500/10 border border-slate-200/80 dark:border-slate-800/80 hover:border-violet-500/50 dark:hover:border-purple-500/50 text-slate-600 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 rounded-md shadow-xs transition-all duration-200 hover:-translate-y-0.5"
          >
            <span class="text-violet-400 dark:text-purple-500 font-bold transition-colors duration-200">~/</span>
            <span class="font-medium">live</span>
          </a>
        </div>
      </div>

      <h3 class="text-lg font-bold text-slate-900 dark:text-slate-100 mb-2 group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors duration-300">
        {{ title }}
      </h3>

      <p class="text-sm text-slate-500 dark:text-slate-400 leading-relaxed">
        {{ description }}
      </p>
    </div>

    <div class="flex flex-wrap gap-1.5 mt-6 pt-4 border-t border-slate-100 dark:border-slate-900/60 font-mono text-[11px]">
      <span
        v-for="tag in tags"
        :key="tag"
        class="px-2 py-0.5 bg-slate-100 dark:bg-slate-950 text-slate-600 dark:text-slate-400 rounded border border-slate-200/60 dark:border-slate-800/60"
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
</script>
