<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="projetos"
    class="section-reveal relative scroll-mt-20 overflow-hidden bg-slate-50 py-20 text-slate-900 transition-colors duration-300 dark:bg-[#09090b] dark:text-white"
  >
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="mb-12 flex flex-col items-center text-center">
        <div class="mb-3 flex items-center gap-2 font-mono text-xs text-slate-500 dark:text-zinc-500 sm:text-sm">
          <span class="text-slate-400 dark:text-slate-600">bruno@portfolio:~$</span>
          <span class="font-semibold text-indigo-600 dark:text-indigo-400">ls --projects</span>
          <span class="terminal-blink h-3.5 w-1 bg-indigo-500"></span>
        </div>
        <h2 class="mb-4 text-3xl font-mono font-bold tracking-tight text-slate-900 dark:text-white sm:text-4xl">
          Projetos em Destaque
        </h2>
        <p class="mx-auto max-w-2xl text-sm leading-relaxed text-slate-600 dark:text-zinc-400 sm:text-base">
          Clique em um card para ver os detalhes e acessar os links do projeto.
        </p>
      </div>

      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
        <ProjectCard
          v-for="(project, index) in myProjects"
          :key="index"
          :title="project.title"
          :description="project.description"
          :tags="project.tags"
          @open="emit('open-project', project)"
        />
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ProjectCard from '@/components/projectcard.vue'
import spectraImage from '@/assets/images/projects/Spectra.png'
import vitalmenImage from '@/assets/images/projects/Vitalmen.png'
import neuroguiaImage from '@/assets/images/projects/neuroguia.png'
import downloaderImage from '@/assets/images/projects/vdown.png'
import budgetImage from '@/assets/images/projects/BudgetCalculator.png'
import hypersafeImage from '@/assets/images/hypersafe.png'

const emit = defineEmits(['open-project'])

// Lista de dados dos meus projetos
const myProjects = ref([
  {
    title: 'Spectra I.A',
    description: 'Um chatbot inteligente, desenvolvido com Python e Flask, utilizando a API do gemini para fornecer respostas automáticas.',
    tags: ['Python', 'HTML', 'CSS', 'JavaScript', 'Flask', 'Gemini API'],
    githubLink: 'https://github.com/BrunoSouzz/Spectra-AI-Assistant',
    liveLink: 'https://spectra-ai-assistant.vercel.app',
    image: spectraImage,
    details: 'Assistente conversacional que combina uma interface web simples com Python, Flask e a API Gemini para responder perguntas de forma rápida e natural.',
  },
  {
    title: 'VitalMen',
    description: 'Um projeto proposto pela faculdade para ser feito em grupo, o objetivo é criar um site para os homens saberem mais sobre saúde e bem-estar proprio. As ferramentas utilizadas incluem HTML, CSS e JavaScript no frontend. Python, Flask no backend. PostgreSQL no banco de dados.',
    tags: ['Python', 'Flask', 'HTML', 'CSS', 'JavaScript', 'PostgreSQL'],
    githubLink: 'https://github.com/BrunoSouzz/VitalMen-Project',
    image: vitalmenImage,
    details: 'Plataforma acadêmica de saúde e bem-estar masculino, com frontend web, API em Flask e persistência de dados em PostgreSQL.',
  },
  {
    title: 'HyperSave',
    description: 'HyperSave é uma aplicação desenvolvida para facilitar o download e gerenciamento de vídeos e áudios a partir de diferentes plataformas, oferecendo uma experiência simples, rápida e intuitiva.',
    tags: ['Node.js', 'Express', 'Tailwindcss', 'JavaScript','Vue.js', 'ytdl-core'],
    githubLink: 'https://github.com/BrunoSouzz/HyperSave',
    liveLink: 'https://hyper-save.vercel.app/',
    image: hypersafeImage,
    details: 'Aplicação web para baixar e gerenciar vídeos e áudios de diferentes plataformas, com uma experiência rápida construída em Vue, Node.js e Tailwind CSS.',
  },
  {
    title: 'Neuroguia',
    description: 'Um projeto proposto pela faculdade para ser feito em grupo, o objetivo é criar um aplicativo para ajudar pessoas com deficiências cognitivas a se orientarem melhor no dia a dia. As ferramentas utilizadas incluem Dart e Flutter para o desenvolvimento do aplicativo, e Node.js para o backend.',
    tags: ['Dart', 'Flutter', 'Node.js', 'PostgreSQL'],
    githubLink: 'https://github.com/neuro-guia',
    image: neuroguiaImage,
    details: 'Aplicativo pensado para apoiar pessoas com deficiências cognitivas na organização e orientação de tarefas do dia a dia.',
  },
  {
    title: 'Downloader de Vídeos',
    description: 'Uma aplicação para baixar vídeos do youtube de forma simples e eficiente.',
    tags: ['Python', 'Flask', 'HTML', 'CSS', 'JavaScript', 'pytube'],
    githubLink: 'https://github.com/BrunoSouzz/videodownloader',
    image: downloaderImage,
    details: 'Aplicação web com fluxo direto para baixar vídeos, construída com uma API em Flask e uma interface leve.',
  },
  {
    title: 'Calculadora de Orçamento',
    description: 'Uma aplicação web para calcular orçamentos de forma simples e eficiente.',
    tags: ['Python', 'Flask', 'HTML', 'CSS', 'JavaScript', 'MySQL'],
    githubLink: 'https://github.com/BrunoSouzz/budget-calculator',
    image: budgetImage,
    details: 'Ferramenta web para montar e calcular orçamentos de forma simples, com processamento no backend em Python.',
  },
  {
    title: 'NutriExpress',
    description: 'API REST desenvolvida para gerenciamento de pedidos e produtos de um serviço de alimentação saudável, aplicando arquitetura em camadas e persistência de dados.',
    tags: ['Java', 'Spring Boot', 'JPA', 'PostgreSQL', 'REST API'],
    githubLink: 'https://github.com/BrunoSouzz/NutriExpress'
  }
])
</script>
