<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <nav class="fixed top-0 left-0 w-full bg-white/80 dark:bg-slate-950/80 backdrop-blur-md border-b border-slate-200 dark:border-slate-800/60 z-50 transition-all duration-300">
    <div class="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between relative">

      <div class="flex items-center gap-4 sm:gap-6">
        <button
          @click="toggleTheme"
          class="group/btn w-9 h-9 border border-slate-200 dark:border-slate-800 hover:border-violet-500/50 dark:hover:border-purple-500/50 text-slate-600 dark:text-slate-300 hover:text-violet-600 dark:hover:text-purple-400 bg-slate-50/50 dark:bg-slate-900/40 rounded-lg flex items-center justify-center transition-all relative overflow-hidden"
          aria-label="Toggle Theme"
        >
          <svg v-if="isDarkMode" class="w-4 h-4 stroke-2 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
          </svg>
          <svg v-else class="w-4 h-4 stroke-2 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 009.002-5.998z" />
          </svg>
          <div class="absolute inset-0 bg-linear-to-b from-transparent via-violet-500/10 dark:via-purple-500/10 to-transparent translate-y-full group-hover/btn:-translate-y-full transition-transform duration-500 ease-out"></div>
        </button>


        <div class="h-5 w-px bg-slate-200 dark:bg-slate-800"></div>


        <a href="#home" class="flex items-center gap-2 group font-mono text-xs">
          <span class="text-violet-600 dark:text-purple-400 font-bold">&lt;/&gt;</span>
          <div class="flex items-center text-slate-400 dark:text-slate-500 select-none">
            <span>portfolio</span>
            <span class="mx-1 text-slate-300 dark:text-slate-700">/</span>
            <span class="text-slate-900 dark:text-white font-bold group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors">bruno</span>
          </div>
        </a>


        <div class="hidden lg:flex items-center gap-1.5 px-2 py-0.5 bg-slate-100 dark:bg-slate-900 border border-slate-200 dark:border-slate-800 text-slate-500 dark:text-slate-400 font-mono text-[10px] rounded-md select-none">
          <span>🌿</span>
          <span class="font-bold text-slate-700 dark:text-slate-300">main</span>
        </div>
      </div>


      <div class="flex items-center gap-8">
        <div class="hidden md:flex items-center space-x-6 text-xs font-mono font-bold tracking-wide text-slate-600 dark:text-slate-400">

          <a href="#home" class="group flex items-center transition-colors hover:text-violet-600 dark:hover:text-purple-400">
            <span class="text-slate-300 dark:text-slate-700 group-hover:text-violet-500 transition-colors mr-1 font-normal">1.</span>
            <span>index.html</span>
          </a>

          <a href="#about" class="group flex items-center transition-colors hover:text-violet-600 dark:hover:text-purple-400">
            <span class="text-slate-300 dark:text-slate-700 group-hover:text-violet-500 transition-colors mr-1 font-normal">2.</span>
            <span>README.md</span>
          </a>

          <a href="#skills" class="group flex items-center transition-colors hover:text-violet-600 dark:hover:text-purple-400">
            <span class="text-slate-300 dark:text-slate-700 group-hover:text-violet-500 transition-colors mr-1 font-normal">3.</span>
            <span>skills.json</span>
          </a>

          <a href="#projects" class="group flex items-center transition-colors hover:text-violet-600 dark:hover:text-purple-400">
            <span class="text-slate-300 dark:text-slate-700 group-hover:text-violet-500 transition-colors mr-1 font-normal">4.</span>
            <span>projects.go</span>
          </a>

          <a href="#contact" class="group flex items-center transition-colors hover:text-violet-600 dark:hover:text-purple-400">
            <span class="text-slate-300 dark:text-slate-700 group-hover:text-violet-500 transition-colors mr-1 font-normal">5.</span>
            <span>contact.js</span>
          </a>

        </div>
      </div>

    </div>
  </nav>
</template>

<script setup>
const emit = defineEmits(['toggle-theme'])

defineProps({
  isDarkMode: {
    type: Boolean,
    required: true
  }
})

const toggleTheme = () => {
  emit('toggle-theme')
}
</script>
