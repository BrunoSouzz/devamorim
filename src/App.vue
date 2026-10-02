<template>
  <div class="min-h-screen bg-white text-slate-900 dark:bg-[#09090b] dark:text-white font-sans antialiased selection:bg-indigo-500/20 transition-colors duration-300">
    <SiteCursor />
    <Navbar
      :isDarkMode="isDarkMode"
      :is-project-open="Boolean(selectedProject)"
      @toggle-theme="onToggleTheme"
      @close-project="closeProject"
    />

    <main>
      <Hero id="home" />

      <About id="about" />

      <Skills id="skills" />

      <Projects id="projetos" @open-project="openProject" />

      <Certificados id="certificados" />

      <Contact id="contact" />
    </main>

    <Footer class="bg-slate-950 dark:bg-[#09090b] border-t border-slate-900 dark:border-zinc-800/80 py-8 text-center text-sm text-slate-500 dark:text-slate-600 transition-colors duration-300"/>
    <ProjectModal :project="selectedProject" @close="closeProject" />
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
import Certificados from './sections/certificate.vue'
import Contact from './sections/contact.vue'
import SiteCursor from './components/sitecursor.vue'
import ProjectModal from './components/projectmodal.vue'

const isDarkMode = ref(true)
const selectedProject = ref(null)

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

const openProject = (project) => {
  selectedProject.value = project
}

const closeProject = () => {
  selectedProject.value = null
}

onMounted(applyTheme)

watch(isDarkMode, applyTheme)
</script>
