<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="contato" class="py-20 bg-slate-50 dark:bg-slate-900 transition-colors duration-300">
    <div class="w-full max-w-7xl mx-auto px-6 md:px-12 flex flex-col lg:flex-row gap-12 items-start">

      <div class="w-full lg:w-5/12 space-y-6">
        <div class="space-y-4">
          <div class="inline-flex items-center gap-2 font-mono text-xs text-violet-500 dark:text-purple-400 bg-violet-50 dark:bg-purple-950/30 px-3 py-1 rounded-full border border-violet-200/50 dark:border-purple-900/30 select-none">
            <span class="w-1.5 h-1.5 rounded-full bg-violet-500 dark:bg-purple-400 animate-pulse"></span>
            <span>bruno@portfolio:~$ ./contact.sh</span>
          </div>

          <h2 class="text-3xl font-mono font-bold text-slate-900 dark:text-white tracking-tight sm:text-4xl">
            Iniciar um Contato
          </h2>

          <div class="font-mono text-xs sm:text-sm text-slate-500 dark:text-slate-400 leading-relaxed bg-slate-100/60 dark:bg-slate-950/30 p-4 border border-slate-200/60 dark:border-slate-800/50 rounded-xl">
            <span class="text-purple-500/80 dark:text-purple-400/60">/**</span><br />
            <span class="pl-3 block border-l-2 border-slate-300 dark:border-slate-800 my-1">
              * Tem um projeto em mente ou quer começar um?<br />
              * Mande uma mensagem e vamos converter essa ideia.
            </span>
            <span class="text-purple-500/80 dark:text-purple-400/60"> */</span>
          </div>
        </div>

        <div class="space-y-3 w-full">
          <a
            href="mailto:devbrunoamorim@gmail.com"
            class="block p-4 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-800/80 rounded-xl transition-all duration-300 hover:border-violet-500/50 dark:hover:border-purple-500/50 hover:shadow-lg hover:shadow-purple-500/5 hover:-translate-y-0.5 group"
          >
            <span class="block font-mono text-[10px] font-bold text-slate-400 dark:text-slate-500 select-none mb-1">
              /* EMAIL_ADDRESS */
            </span>
            <span class="block font-mono text-sm font-bold text-slate-900 dark:text-slate-100 group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors duration-200">
              devbrunoamorim@gmail.com
            </span>
          </a>

          <a
            href="https://www.linkedin.com/in/dev-brunoamorim"
            target="_blank"
            class="block p-4 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-800/80 rounded-xl transition-all duration-300 hover:border-violet-500/50 dark:hover:border-purple-500/50 hover:shadow-lg hover:shadow-purple-500/5 hover:-translate-y-0.5 group"
          >
            <span class="block font-mono text-[10px] font-bold text-slate-400 dark:text-slate-500 select-none mb-1">
              /* LINKEDIN_PROFILE */
            </span>
            <span class="block font-mono text-sm font-bold text-slate-900 dark:text-slate-100 group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors duration-200">
              Bruno Amorim
            </span>
          </a>

          <a
            href="https://github.com/BrunoSouzz"
            target="_blank"
            class="block p-4 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-800/80 rounded-xl transition-all duration-300 hover:border-violet-500/50 dark:hover:border-purple-500/50 hover:shadow-lg hover:shadow-purple-500/5 hover:-translate-y-0.5 group"
          >
            <span class="block font-mono text-[10px] font-bold text-slate-400 dark:text-slate-500 select-none mb-1">
              /* GITHUB_REPOSITORY */
            </span>
            <span class="block font-mono text-sm font-bold text-slate-900 dark:text-slate-100 group-hover:text-violet-600 dark:group-hover:text-purple-400 transition-colors duration-200">
              @BrunoSouzz
            </span>
          </a>
        </div>

        <div class="inline-flex items-center gap-2 px-3 py-1.5 bg-emerald-500/5 dark:bg-emerald-950/20 border border-emerald-500/20 text-emerald-600 dark:text-emerald-400 font-mono text-[11px] font-bold uppercase tracking-wider rounded-lg select-none">
          <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 dark:bg-emerald-400 animate-pulse"></span>
          <span>Disponível para novos projetos</span>
        </div>
      </div>

      <div class="w-full lg:w-7/12 bg-white dark:bg-slate-900/40 border border-slate-200 dark:border-slate-800/80 rounded-xl p-6 sm:p-8 shadow-xs relative overflow-hidden group/form">

        <div class="absolute top-0 inset-x-0 bg-slate-100/60 dark:bg-slate-950/40 border-b border-slate-200 dark:border-slate-800/80 px-4 py-1.5 flex items-center justify-between font-mono text-[10px] text-slate-400 dark:text-slate-600 select-none">
          <span>// MSG_TRANSMISSION_PROTOCOL</span>
          <span class="tracking-widest">v1.0.2</span>
        </div>

        <form @submit.prevent="handleSubmit" class="space-y-5 pt-4">
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
            <div class="space-y-2">
              <label for="name" class="block font-mono text-xs font-bold text-slate-400 dark:text-slate-500 select-none">
                INPUT_NAME:
              </label>
              <input
                id="name"
                v-model="formData.name"
                type="text"
                required
                placeholder="Como te chamam?"
                class="w-full px-4 py-3 bg-slate-50 dark:bg-slate-950/60 border border-slate-200 dark:border-slate-800 text-slate-900 dark:text-slate-100 text-sm rounded-lg focus:outline-hidden focus:border-violet-500 dark:focus:border-purple-500 focus:ring-2 focus:ring-violet-500/10 dark:focus:ring-purple-500/10 transition-all duration-200 placeholder-slate-400 dark:placeholder-slate-600"
              />
            </div>

            <div class="space-y-2">
              <label for="email" class="block font-mono text-xs font-bold text-slate-400 dark:text-slate-500 select-none">
                INPUT_EMAIL:
              </label>
              <input
                id="email"
                v-model="formData.email"
                type="email"
                required
                placeholder="seu@email.com"
                class="w-full px-4 py-3 bg-slate-50 dark:bg-slate-950/60 border border-slate-200 dark:border-slate-800 text-slate-900 dark:text-slate-100 text-sm rounded-lg focus:outline-hidden focus:border-violet-500 dark:focus:border-purple-500 focus:ring-2 focus:ring-violet-500/10 dark:focus:ring-purple-500/10 transition-all duration-200 placeholder-slate-400 dark:placeholder-slate-600"
              />
            </div>
          </div>

          <div class="space-y-2">
            <label for="subject" class="block font-mono text-xs font-bold text-slate-400 dark:text-slate-500 select-none">
              INPUT_SUBJECT:
            </label>
            <input
              id="subject"
              v-model="formData.subject"
              type="text"
              required
              placeholder="Qual o assunto?"
              class="w-full px-4 py-3 bg-slate-50 dark:bg-slate-950/60 border border-slate-200 dark:border-slate-800 text-slate-900 dark:text-slate-100 text-sm rounded-lg focus:outline-hidden focus:border-violet-500 dark:focus:border-purple-500 focus:ring-2 focus:ring-violet-500/10 dark:focus:ring-purple-500/10 transition-all duration-200 placeholder-slate-400 dark:placeholder-slate-600"
            />
          </div>

          <div class="space-y-2">
            <label for="message" class="block font-mono text-xs font-bold text-slate-400 dark:text-slate-500 select-none">
              TEXTAREA_MESSAGE:
            </label>
            <textarea
              id="message"
              v-model="formData.message"
              rows="5"
              required
              placeholder="Escreva sua mensagem aqui..."
              class="w-full px-4 py-3 bg-slate-50 dark:bg-slate-950/60 border border-slate-200 dark:border-slate-800 text-slate-900 dark:text-slate-100 text-sm rounded-lg focus:outline-hidden focus:border-violet-500 dark:focus:border-purple-500 focus:ring-2 focus:ring-violet-500/10 dark:focus:ring-purple-500/10 transition-all duration-200 placeholder-slate-400 dark:placeholder-slate-600 resize-none"
            ></textarea>
          </div>

          <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 pt-2">

            <div class="flex-1 min-h-8">
              <div v-if="submitStatus === 'success'" class="inline-flex items-center gap-2 px-3 py-1 bg-emerald-500/10 border border-emerald-500/20 rounded-md font-mono text-xs text-emerald-600 dark:text-emerald-400">
                <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 animate-pulse"></span>
                <span>[SUCCESS]: Dados transmitidos com êxito!</span>
              </div>

              <div v-if="submitStatus === 'error'" class="inline-flex items-center gap-2 px-3 py-1 bg-red-500/10 border border-red-500/20 rounded-md font-mono text-xs text-red-600 dark:text-red-400">
                <span class="w-1.5 h-1.5 rounded-full bg-red-500 animate-pulse"></span>
                <span>[ERROR]: Falha na transmissão. Verifique a rede.</span>
              </div>
            </div>

            <Button type="submit" variant="primary" :disabled="isSubmitting" class="w-full sm:w-auto shrink-0">
              <template #icon-right>
                <span class="text-purple-200 font-normal select-none group-hover:translate-x-0.5 transition-transform">-></span>
              </template>
              {{ isSubmitting ? 'Transmitindo...' : 'Enviar Mensagem' }}
            </Button>
          </div>
        </form>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import Button from '@/components/button.vue'

const formData = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const isSubmitting = ref(false)
const submitStatus = ref(null)

const handleSubmit = async () => {
  if (!formData.value.email || !formData.value.message) {
    submitStatus.value = "error"
    return
  }

  isSubmitting.value = true
  submitStatus.value = null

  try {
    const CONTACT_EMAIL = "devbrunoamorim@gmail.com"

    const response = await fetch(`https://formsubmit.co/ajax/${CONTACT_EMAIL}`, {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Accept": "application/json"
      },
      body: JSON.stringify({
        Nome: formData.value.name,
        Email: formData.value.email,
        Assunto: formData.value.subject || "Sem Assunto",
        Mensagem: formData.value.message,
        "_subject": `🚀 Novo contato do Portfólio: ${formData.value.subject || formData.value.name}`,
        "_captcha": "false",
      })
    })

    if (response.ok) {
      submitStatus.value = "success"
      // Limpa os campos após o sucesso
      formData.value = { name: "", email: "", subject: "", message: "" }
    } else {
      console.error("Falha na resposta do servidor")
      submitStatus.value = "error"
    }
  } catch (error) {
    console.error("Erro no envio:", error)
    submitStatus.value = "error"
  } finally {
    isSubmitting.value = false
    // Esconde a mensagem de status após 5 segundos
    setTimeout(() => {
      submitStatus.value = null
    }, 5000)
  }
}
</script>
