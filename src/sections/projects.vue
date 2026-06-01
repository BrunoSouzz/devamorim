<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="projetos" class="py-20 bg-slate-50 dark:bg-slate-900 transition-colors duration-300">
    <div class="max-w-6xl mx-auto px-6">

      <div class="mb-12 space-y-2 text-center md:text-left">
        <div class="inline-flex items-center gap-2 font-mono text-xs text-violet-500 dark:text-purple-400 bg-violet-50 dark:bg-purple-950/30 px-3 py-1 rounded-full border border-violet-200/50 dark:border-purple-900/30">
          <span class="w-1.5 h-1.5 rounded-full bg-violet-500 dark:bg-purple-400 animate-pulse"></span>
          <span>bruno@portfolio:~$ ls --projects</span>
        </div>
        <h2 class="text-3xl font-extrabold text-slate-900 dark:text-white tracking-tight sm:text-4xl">
          Projetos em Destaque
        </h2>
        <p class="text-slate-500 dark:text-slate-400 max-w-xl text-sm sm:text-base">
          Uma seleção de aplicações e sistemas que desenvolvi, focando em arquitetura limpa, performance e experiência do usuário.
        </p>
      </div>

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
import ProjectCard from 'src/components/ProjectCard.vue'

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
