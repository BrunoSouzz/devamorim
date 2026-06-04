<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <nav class="fixed top-0 left-0 w-full bg-white/80 dark:bg-slate-950/80 backdrop-blur-md border-b border-slate-200 dark:border-slate-900 z-50 transition-all duration-300">
    <div class="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between relative">

      <div class="flex items-center gap-4 sm:gap-6">
        <button
          @click="toggleTheme"
          class="group/btn w-9 h-9 border border-slate-200 dark:border-slate-900 hover:border-violet-500/50 dark:hover:border-purple-500/50 text-slate-600 dark:text-slate-300 hover:text-violet-600 dark:hover:text-purple-400 bg-slate-50/50 dark:bg-slate-900/40 rounded-lg flex items-center justify-center transition-all relative overflow-hidden cursor-pointer"
          aria-label="Toggle Theme"
        >
          <svg v-if="isDarkMode" class="w-4 h-4 stroke-2 relative z-10 transition-transform duration-300 group-hover/btn:rotate-45" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
          </svg>
          <svg v-else class="w-4 h-4 stroke-2 relative z-10 transition-transform duration-300 group-hover/btn:-rotate-12" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 009.002-5.998z" />
          </svg>
          <div class="absolute inset-0 bg-linear-to-b from-transparent via-violet-500/10 dark:via-purple-500/10 to-transparent translate-y-full group-hover/btn:-translate-y-full transition-transform duration-500 ease-out"></div>
        </button>

        <div class="h-5 w-px bg-slate-200 dark:bg-slate-900"></div>

        <a href="#home" class="flex items-center gap-2 group font-mono text-xs">
          <span class="text-violet-600 dark:text-purple-400 font-bold transition-transform duration-300 group-hover:scale-110">&lt;/&gt;</span>
          <div class="flex items-center text-slate-400 dark:text-slate-500 select-none">
            <span>portfolio</span>
            <span class="mx-1 text-slate-300 dark:text-slate-800">/</span>
            <span class="text-slate-900 dark:text-white font-bold group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors">bruno</span>
          </div>
        </a>

        <div class="hidden sm:flex items-center gap-1.5 px-2 py-0.5 bg-slate-100 dark:bg-slate-900/60 border border-slate-200 dark:border-slate-900 text-slate-500 dark:text-slate-400 font-mono text-[10px] rounded-md select-none">
          <span class="text-xs">🌿</span>
          <span class="font-bold text-slate-700 dark:text-slate-300">main</span>
        </div>
      </div>

      <div class="flex items-center gap-4 lg:gap-6">

        <div class="hidden md:flex items-center h-16 font-mono text-[11px] font-bold tracking-wide text-slate-500 dark:text-slate-400">

          <a href="#home" class="group flex items-center h-full px-3 border-b-2 border-transparent hover:border-orange-500 hover:bg-slate-500/5 dark:hover:bg-slate-400/5 hover:text-slate-900 dark:hover:text-white transition-all duration-200">
            <span class="w-1.5 h-1.5 rounded-full bg-orange-500 mr-2 opacity-60 group-hover:opacity-100"></span>
            <span class="text-slate-300 dark:text-slate-700 font-normal mr-1">1.</span>
            <span>index.html</span>
          </a>

          <a href="#about" class="group flex items-center h-full px-3 border-b-2 border-transparent hover:border-blue-400 hover:bg-slate-500/5 dark:hover:bg-slate-400/5 hover:text-slate-900 dark:hover:text-white transition-all duration-200">
            <span class="w-1.5 h-1.5 rounded-full bg-blue-400 mr-2 opacity-60 group-hover:opacity-100"></span>
            <span class="text-slate-300 dark:text-slate-700 font-normal mr-1">2.</span>
            <span>README.md</span>
          </a>

          <a href="#skills" class="group flex items-center h-full px-3 border-b-2 border-transparent hover:border-amber-400 hover:bg-slate-500/5 dark:hover:bg-slate-400/5 hover:text-slate-900 dark:hover:text-white transition-all duration-200">
            <span class="w-1.5 h-1.5 rounded-full bg-amber-400 mr-2 opacity-60 group-hover:opacity-100"></span>
            <span class="text-slate-300 dark:text-slate-700 font-normal mr-1">3.</span>
            <span>skills.json</span>
          </a>

          <a href="#projects" class="group flex items-center h-full px-3 border-b-2 border-transparent hover:border-cyan-400 hover:bg-slate-500/5 dark:hover:bg-slate-400/5 hover:text-slate-900 dark:hover:text-white transition-all duration-200">
            <span class="w-1.5 h-1.5 rounded-full bg-cyan-400 mr-2 opacity-60 group-hover:opacity-100"></span>
            <span class="text-slate-300 dark:text-slate-700 font-normal mr-1">4.</span>
            <span>projects.go</span>
          </a>

          <a href="#contact" class="group flex items-center h-full px-3 border-b-2 border-transparent hover:border-yellow-400 hover:bg-slate-500/5 dark:hover:bg-slate-400/5 hover:text-slate-900 dark:hover:text-white transition-all duration-200">
            <span class="w-1.5 h-1.5 rounded-full bg-yellow-400 mr-2 opacity-60 group-hover:opacity-100"></span>
            <span class="text-slate-300 dark:text-slate-700 font-normal mr-1">5.</span>
            <span>contact.js</span>
          </a>

        </div>

        <div class="hidden lg:block h-5 w-px bg-slate-200 dark:bg-slate-900"></div>

        <div class="hidden lg:flex items-center gap-2 px-2.5 py-1 bg-slate-50 dark:bg-slate-900/40 border border-slate-200 dark:border-slate-900 rounded-md font-mono text-[10px] text-slate-500 dark:text-slate-400 select-none">
          <span class="relative flex h-1.5 w-1.5">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-1.5 w-1.5 bg-emerald-500"></span>
          </span>
          <span>STABLE_PORT_443</span>
        </div>

        <button
          @click="isMenuOpen = !isMenuOpen"
          class="md:hidden w-9 h-9 flex items-center justify-center border border-slate-200 dark:border-slate-900 rounded-lg bg-slate-50/50 dark:bg-slate-900/40 text-slate-600 dark:text-slate-300 cursor-pointer"
          aria-label="Toggle Menu"
        >
          <div class="w-4 h-4 flex flex-col justify-between items-center relative">
            <span :class="['w-full h-0.5 bg-current rounded-sm transition-all duration-300 origin-left', isMenuOpen ? 'rotate-45 translate-x-0.5 -translate-y-px' : '']"></span>
            <span :class="['w-full h-0.5 bg-current rounded-sm transition-all duration-300', isMenuOpen ? 'opacity-0 scale-0' : '']"></span>
            <span :class="['w-full h-0.5 bg-current rounded-sm transition-all duration-300 origin-left', isMenuOpen ? '-rotate-45 translate-x-0.5 translate-y-px' : '']"></span>
          </div>
        </button>

      </div>
    </div>

    <div
      :class="[
        'absolute top-16 left-0 w-full bg-white dark:bg-slate-950 border-b border-slate-200 dark:border-slate-900 md:hidden font-mono text-xs transition-all duration-300 overflow-hidden shadow-xl',
        isMenuOpen ? 'max-h-64 opacity-100' : 'max-h-0 opacity-0 pointer-events-none'
      ]"
    >
      <div class="px-6 py-4 space-y-3 bg-slate-50/50 dark:bg-slate-950/40">
        <div class="text-[10px] text-slate-400 dark:text-slate-600 font-bold tracking-wider uppercase select-none mb-1">
          📁 EXPLORER: PORTFOLIO
        </div>

        <a @click="isMenuOpen = false" href="#home" class="flex items-center gap-2.5 py-1.5 text-slate-600 dark:text-slate-400 hover:text-orange-500 dark:hover:text-orange-400 font-bold">
          <span class="w-1.5 h-1.5 rounded-full bg-orange-500"></span>
          <span>index.html</span>
        </a>

        <a @click="isMenuOpen = false" href="#about" class="flex items-center gap-2.5 py-1.5 text-slate-600 dark:text-slate-400 hover:text-blue-400 dark:hover:text-blue-400 font-bold">
          <span class="w-1.5 h-1.5 rounded-full bg-blue-400"></span>
          <span>README.md</span>
        </a>

        <a @click="isMenuOpen = false" href="#skills" class="flex items-center gap-2.5 py-1.5 text-slate-600 dark:text-slate-400 hover:text-amber-400 dark:hover:text-amber-400 font-bold">
          <span class="w-1.5 h-1.5 rounded-full bg-amber-400"></span>
          <span>skills.json</span>
        </a>

        <a @click="isMenuOpen = false" href="#projects" class="flex items-center gap-2.5 py-1.5 text-slate-600 dark:text-slate-400 hover:text-cyan-400 dark:hover:text-cyan-400 font-bold">
          <span class="w-1.5 h-1.5 rounded-full bg-cyan-400"></span>
          <span>projects.go</span>
        </a>

        <a @click="isMenuOpen = false" href="#contact" class="flex items-center gap-2.5 py-1.5 text-slate-600 dark:text-slate-400 hover:text-yellow-400 dark:hover:text-yellow-400 font-bold">
          <span class="w-1.5 h-1.5 rounded-full bg-yellow-400"></span>
          <span>contact.js</span>
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const emit = defineEmits(['toggle-theme'])
const isMenuOpen = ref(false)

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
