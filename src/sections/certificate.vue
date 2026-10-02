<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="certificados"
    class="relative scroll-mt-20 overflow-hidden bg-slate-50 py-20 text-slate-900 transition-colors duration-300 dark:bg-[#09090b] dark:text-white"
  >
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="mb-12 flex flex-col items-center text-center">
        <div class="mb-3 flex items-center gap-2 font-mono text-xs text-slate-500 dark:text-zinc-500 sm:text-sm">
          <span>bruno@portfolio:~$</span>
          <span class="font-semibold text-indigo-600 dark:text-indigo-400">ls --certificates</span>
          <span class="terminal-blink h-3.5 w-1 bg-indigo-500"></span>
        </div>
        <h2 class="mb-4 text-3xl font-mono font-bold tracking-tight text-slate-900 dark:text-white sm:text-4xl">
          Certificações & Cursos
        </h2>
        <p class="mx-auto max-w-2xl text-sm leading-relaxed text-slate-600 dark:text-zinc-400 sm:text-base">
          Cursos concluídos e certificações técnicas que comprovam minha bagagem prática.
        </p>
      </div>

      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
        <CertificateCard
          v-for="cert in certificates"
          :key="cert.id"
          :certificate="cert"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import CertificateCard from '../components/certificatecard.vue'

const certificates = ref([
  {
    id: "1",
    title: "Introduction to Cybersecurity",
    issuer: "Cisco Networking Academy",
    date: "2026",
    category: "CYBERSECURITY",
    preview: "/certificates/introduction-to-cybersecurity.png",
    link: "https://www.linkedin.com/posts/dev-brunoamorim_cybersecurity-seguranaexadainformaaexaeto-activity-7439001813426716672-ArCY",
    linkType: "linkedin",
    skills: ["Cybersecurity", "Network Security", "Ethical Hacking"]
  },
  {
    id: "2",
    title: "Python Essentials",
    issuer: "SENAI",
    date: "2026",
    category: "PROGRAMMING",
    preview: "/certificates/preview_senai.png",
    link: "/certificates/Certificado_SENAI - python essentianls.pdf",
    linkType: "file",
    skills: ["Python", "HTML", "CSS", "JavaScript", "PostgreSQL"]
  },
  {
    id: "3",
    title: "Startupday - Sebrae",
    issuer: "Sebrae",
    date: "2026",
    category: "EVENTS",
    preview: "/certificates/preview_starup.png",
    link: "/certificates/Certificado_startuday.pdf",
    linkType: "file",
    skills: ["Innovation", "Entrepreneurship", "Business Development"]
  }
])
</script>
