<template>
  <div class="min-h-screen bg-white text-slate-800 dark:bg-slate-900 dark:text-white font-sans antialiased selection:bg-emerald-500/30 transition-colors duration-300">
    <Navbar :isDarkMode="isDarkMode" @toggle-theme="onToggleTheme" />

    <main>
      <Hero id="home" />

      <About id="about" />

      <Skills id="skills" />

      <Projects id="projects" />

      <Contact id="contact" />
    </main>

    <Footer class="bg-slate-950 dark:bg-black border-t border-slate-900 dark:border-slate-800 py-8 text-center text-sm text-slate-500 dark:text-slate-600 transition-colors duration-300"/>
  </div>
</template>

<script setup>
import { ref, watch, onMounted } from 'vue'
import Navbar from './components/navbar.vue'
import Footer from './components/footer.vue'
import Hero from './sections/hero.vue'
import About from './sections/about.vue'
import Skills from './sections/skills.vue'
import Projects from './sections/projects.vue'
import Contact from './sections/contact.vue'

const isDarkMode = ref(true)

const applyTheme = () => {
  if (isDarkMode.value) {
    document.documentElement.classList.add('dark')
  } else {
    document.documentElement.classList.remove('dark')
  }
}

const onToggleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  applyTheme()
}

onMounted(applyTheme)


watch(isDarkMode, applyTheme)
</script>
