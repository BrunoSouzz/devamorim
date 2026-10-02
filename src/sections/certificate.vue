<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="certificados"
    class="py-20 bg-slate-50 dark:bg-slate-950 text-slate-900 dark:text-white scroll-mt-20 transition-colors duration-300 relative overflow-hidden"
  >
    <!-- Background Grid Alinhado com a Identidade de Workspace -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#80808007_1px,transparent_1px),linear-gradient(to_bottom,#80808007_1px,transparent_1px)] bg-size-[24px_24px] pointer-events-none"></div>

    <!-- Linhas de Telemetria Laterais -->
    <div class="absolute top-12 left-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      + SYS.CERTS_INIT_0x05
    </div>
    <div class="absolute bottom-12 right-8 text-slate-300 dark:text-slate-800 font-mono text-xs select-none pointer-events-none hidden lg:block tracking-widest">
      // TOTAL_CERTIFICATES [03]
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <!-- Cabeçalho de Terminal Centralizado -->
      <div class="flex flex-col items-center text-center mb-16">
        <div class="flex items-center gap-1.5 text-indigo-600 dark:text-indigo-400 font-mono text-sm tracking-wide mb-2 select-none">
          <span class="text-slate-400 dark:text-slate-600">bruno@portfolio:~$</span>
          <span>ls --certificates</span>
          <span class="w-1.5 h-3.5 bg-indigo-500 dark:bg-indigo-400 animate-pulse ml-0.5"></span>
        </div>
        <h2 class="text-3xl sm:text-4xl font-mono font-black text-slate-950 dark:text-white tracking-tight">
          Certificações & Cursos
        </h2>
        <p class="text-slate-500 dark:text-slate-400 max-w-xl text-xs sm:text-sm mt-3 font-sans leading-relaxed">
          Cursos concluídos e certificações técnicas que comprovam minha bagagem prática.
        </p>
        <div class="h-0.5 w-20 bg-linear-to-r from-transparent via-emerald-500/40 dark:via-emerald-500/40 to-transparent mt-5"></div>
      </div>

      <!-- Grid de Certificados -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
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
    link: "/certificates/Certificado_startuday.pdf",
    linkType: "file",
    skills: ["Innovation", "Entrepreneurship", "Business Development"]
  }
])
</script>
