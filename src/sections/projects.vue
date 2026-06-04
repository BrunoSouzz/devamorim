<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="projetos"
    class="py-20 bg-slate-50 dark:bg-slate-950 text-slate-900 dark:text-white scroll-mt-20 transition-colors duration-300 relative overflow-hidden"
  >
    <!-- Background Grid Alinhado com a Identidade de Workspace -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#80808007_1px,transparent_1px),linear-gradient(to_bottom,#80808007_1px,transparent_1px)] bg-size-[24px_24px] pointer-events-none"></div>

    <!-- Linhas de Telemetria Laterais -->
    <div class="absolute top-12 left-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      + SYS.REPOS_INIT_0x04
    </div>
    <div class="absolute bottom-12 right-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      // TOTAL_DEPLOYED_MODULES [05]
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">

      <!-- Cabeçalho (Prompt de Terminal Centralizado) -->
      <div class="flex flex-col items-center text-center mb-16">
        <div class="flex items-center gap-1.5 text-violet-600 dark:text-purple-400 font-mono text-sm tracking-wide mb-2 select-none">
          <span class="text-slate-400 dark:text-slate-600">bruno@portfolio:~$</span>
          <span>ls --projects</span>
          <span class="w-1.5 h-3.5 bg-violet-500 dark:bg-purple-400 animate-pulse ml-0.5"></span>
        </div>
        <h2 class="text-3xl sm:text-4xl font-mono font-black text-slate-950 dark:text-white tracking-tight">
          Projetos em Destaque
        </h2>
        <p class="text-slate-500 dark:text-slate-400 max-w-xl text-xs sm:text-sm mt-3 font-sans leading-relaxed">
          Uma seleção de aplicações e sistemas desenvolvidos focando em arquitetura limpa, performance isolada e experiência do usuário.
        </p>
        <div class="h-0.5 w-20 bg-linear-to-r from-transparent via-violet-500/40 dark:via-purple-500/40 to-transparent mt-5"></div>
      </div>

      <!-- Grid de Artefatos Compilados -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <ProjectCard
          v-for="(project, index) in myProjects"
          :key="index"
          :title="project.title"
          :description="project.description"
          :tags="project.tags"
          :github-link="project.githubLink"
          :live-link="project.liveLink"
        />
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ProjectCard from '@/components/projectcard.vue'

// Lista de dados dos seus projetos
const myProjects = ref([
  {
    title: 'Spectra I.A',
    description: 'Um chatbot inteligente, desenvolvido com Python e Flask, utilizando a API do gemini para fornecer respostas automáticas.',
    tags: ['Python', 'HTML', 'CSS', 'JavaScript', 'Flask', 'Gemini API'],
    githubLink: 'https://github.com/BrunoSouzz/Spectra-AI-Assistant',
  },
  {
    title: 'VitalMen',
    description: 'Um projeto proposto pela faculdade para ser feito em grupo, o objetivo é criar um site para os homens saberem mais sobre saúde e bem-estar proprio. As ferramentas utilizadas incluem HTML, CSS e JavaScript no frontend. Python, Flask no backend. PostgreSQL no banco de dados.',
    tags: ['Python', 'Flask', 'HTML', 'CSS', 'JavaScript', 'PostgreSQL'],
    githubLink: 'https://github.com/BrunoSouzz/VitalMen-Project',
    liveLink: 'https://vitalmen.vercel.app/'
  },
  {
    title: 'Neuroguia',
    description: 'Um projeto proposto pela faculdade para ser feito em grupo, o objetivo é criar um aplicativo para ajudar pessoas com deficiências cognitivas a se orientarem melhor no dia a dia. As ferramentas utilizadas incluem Dart e Flutter para o desenvolvimento do aplicativo, e Node.js para o backend.',
    tags: ['Dart', 'Flutter', 'Node.js', 'PostgreSQL'],
    githubLink: 'https://github.com/neuro-guia',
  },
  {
    title: 'Downloader de Vídeos',
    description: 'Uma aplicação para baixar vídeos do youtube de forma simples e eficiente.',
    tags: ['Python', 'Flask', 'HTML', 'CSS', 'JavaScript', 'pytube'],
    githubLink: 'https://github.com/BrunoSouzz/videodownloader'
  },
  {
    title: 'Calculadora de Orçamento',
    description: 'Uma aplicação web para calcular orçamentos de forma simples e eficiente.',
    tags: ['Python', 'Flask', 'HTML', 'CSS', 'JavaScript', 'MySQL'],
    githubLink: 'https://github.com/BrunoSouzz/budget-calculator'
  }
])
</script>
