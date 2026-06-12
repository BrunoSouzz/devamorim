<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="contato"
    class="py-24 bg-slate-50 dark:bg-slate-950 transition-colors duration-300 relative overflow-hidden"
  >
    <div
      class="absolute inset-0 bg-[linear-gradient(to_right,#8080800a_1px,transparent_1px),linear-gradient(to_bottom,#8080800a_1px,transparent_1px)] bg-size-[14px_24px] pointer-events-none"
    ></div>

    <div class="w-full max-w-5xl mx-auto px-6 relative z-10">
      <div class="mb-12 text-center md:text-left">
        <h2 class="text-4xl font-mono font-black text-slate-950 dark:text-white tracking-tight">
          /contact_<span class="text-violet-600 dark:text-purple-400">js</span>
        </h2>
        <p class="text-slate-500 dark:text-slate-400 font-mono text-xs sm:text-sm mt-2">
          // Envie uma requisição para iniciar uma nova conexão de projeto.
        </p>
      </div>

      <div
        class="w-full bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-800 rounded-2xl shadow-2xl overflow-hidden flex flex-col md:flex-row h-auto md:min-h-145"
      >
        <div
          class="w-full md:w-64 bg-slate-50/80 dark:bg-slate-900/40 border-b md:border-b-0 md:border-r border-slate-200 dark:border-slate-800 flex flex-col shrink-0"
        >
          <div
            class="px-4 py-3.5 border-b border-slate-200 dark:border-slate-800/60 flex items-center gap-2 select-none"
          >
            <span class="w-3 h-3 rounded-full bg-red-400 dark:bg-red-500/60"></span>
            <span class="w-3 h-3 rounded-full bg-yellow-400 dark:bg-yellow-500/60"></span>
            <span class="w-3 h-3 rounded-full bg-emerald-400 dark:bg-emerald-500/60"></span>
            <span class="ml-2 font-mono text-[10px] tracking-wider font-bold text-slate-400 dark:text-slate-500"
              >EXPLORER</span
            >
          </div>

          <div class="p-4 flex-1 space-y-6 font-mono text-xs text-slate-600 dark:text-slate-400">
            <div>
              <p
                class="text-[10px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider mb-2 select-none"
              >
                📂 active_connections
              </p>
              <div class="space-y-1 pl-1">
                <a
                  href="mailto:devbrunoamorim@gmail.com"
                  class="flex items-center gap-2 px-2 py-1.5 rounded-lg hover:bg-slate-200/60 dark:hover:bg-slate-800/50 text-slate-600 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 transition-all duration-200 group"
                >
                  <svg class="w-3.5 h-3.5 text-slate-400 group-hover:text-violet-500 dark:group-hover:text-purple-400 fill-none stroke-current stroke-2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                  </svg>
                  <span>mail.txt</span>
                </a>

                <a
                  href="https://www.linkedin.com/in/dev-brunoamorim"
                  target="_blank"
                  class="flex items-center gap-2 px-2 py-1.5 rounded-lg hover:bg-slate-200/60 dark:hover:bg-slate-800/50 text-slate-600 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 transition-all duration-200 group"
                >
                  <svg class="w-3.5 h-3.5 text-slate-400 group-hover:text-violet-500 dark:group-hover:text-purple-400 fill-current" viewBox="0 0 24 24">
                    <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.8v8h2.8v-4.16c0-.22 0-.45.06-.62a1.12 1.12 0 0 1 1-.77c.76 0 1 .56 1 1.39v4.16h2.8M6.5 8.37a1.37 1.37 0 1 0 0-2.75 1.37 1.37 0 0 0 0 2.75M8 18.5v-8H5v8h3z"/>
                  </svg>
                  <span>linkedin.url</span>
                </a>

                <a
                  href="https://github.com/BrunoSouzz"
                  target="_blank"
                  class="flex items-center gap-2 px-2 py-1.5 rounded-lg hover:bg-slate-200/60 dark:hover:bg-slate-800/50 text-slate-600 dark:text-slate-400 hover:text-violet-600 dark:hover:text-purple-400 transition-all duration-200 group"
                >
                  <svg class="w-3.5 h-3.5 text-slate-400 group-hover:text-violet-500 dark:group-hover:text-purple-400 fill-current" viewBox="0 0 24 24">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.603-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.462-1.11-1.462-.908-.62.069-.061.069-.061 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.831.092-.646.35-1.086.636-1.336-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.579.688.481C19.138 20.161 22 16.418 22 12c0-5.523-4.477-10-10-10z" />
                  </svg>
                  <span>github.sh</span>
                </a>
              </div>
            </div>

            <div>
              <p
                class="text-[10px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider mb-2 select-none"
              >
                ⚡ system_status
              </p>
              <div class="pl-1">
                <div
                  class="inline-flex items-center gap-2 px-2.5 py-1.5 bg-emerald-500/5 dark:bg-emerald-500/10 border border-emerald-500/20 text-emerald-600 dark:text-emerald-400 rounded-lg text-[10px] font-bold uppercase tracking-wide select-none"
                >
                  <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 animate-pulse"></span>
                  <span>ONLINE_TO_HIRE</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="flex-1 flex flex-col bg-slate-100/20 dark:bg-slate-900/10">
          <div
            class="bg-slate-50 dark:bg-slate-900/80 border-b border-slate-200 dark:border-slate-800 px-4 flex items-center select-none"
          >
            <div
              class="bg-white dark:bg-slate-900 border-r border-l border-t-2 border-t-violet-500 dark:border-t-purple-500 border-slate-200 dark:border-slate-800 px-4 py-2.5 flex items-center gap-2 text-xs font-mono font-bold text-slate-800 dark:text-slate-200"
            >
              <span class="text-yellow-500 font-bold">{}</span> payload_message.json
            </div>
          </div>

          <form
            @submit.prevent="handleSubmit"
            class="p-6 md:p-8 flex-1 flex flex-col justify-between font-mono text-sm relative"
          >
            <div class="space-y-4">

              <div class="flex items-center gap-4">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none">01</span>
                <span class="text-slate-400 dark:text-slate-600 font-bold text-base">{</span>
              </div>

              <div class="flex items-start sm:items-center gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1 sm:pt-0">02</span>
                <div class="flex-1 flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2 pl-4">
                  <label for="name" class="text-violet-600 dark:text-purple-400 shrink-0 font-medium">"remetente_nome"</label>
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="name"
                    v-model="formData.name"
                    type="text"
                    required
                    placeholder='"Como quer ser chamado?"'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-violet-500 dark:focus:border-purple-500 text-slate-900 dark:text-slate-100 text-sm py-0.5 px-1 outline-hidden transition-all placeholder-slate-400/60 dark:placeholder-slate-600 focus:placeholder-slate-300"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>
              </div>

              <div class="flex items-start sm:items-center gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1 sm:pt-0">03</span>
                <div class="flex-1 flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2 pl-4">
                  <label for="email" class="text-violet-600 dark:text-purple-400 shrink-0 font-medium">"remetente_email"</label>
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="email"
                    v-model="formData.email"
                    type="email"
                    required
                    placeholder='"seu@email.com"'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-violet-500 dark:focus:border-purple-500 text-slate-900 dark:text-slate-100 text-sm py-0.5 px-1 outline-hidden transition-all placeholder-slate-400/60 dark:placeholder-slate-600 focus:placeholder-slate-300"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>
              </div>

              <div class="flex items-start sm:items-center gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1 sm:pt-0">04</span>
                <div class="flex-1 flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2 pl-4">
                  <label for="subject" class="text-violet-600 dark:text-purple-400 shrink-0 font-medium">"assunto_escopo"</label>
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="subject"
                    v-model="formData.subject"
                    type="text"
                    required
                    placeholder='"Motivo do contato..."'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-violet-500 dark:focus:border-purple-500 text-slate-900 dark:text-slate-100 text-sm py-0.5 px-1 outline-hidden transition-all placeholder-slate-400/60 dark:placeholder-slate-600 focus:placeholder-slate-300"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>
              </div>

              <div class="flex items-start gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1">05</span>
                <div class="flex-1 flex flex-col gap-2 pl-4">
                  <div class="flex items-center gap-2">
                    <label for="message" class="text-violet-600 dark:text-purple-400 font-medium">"corpo_mensagem"</label>
                    <span class="text-slate-400 dark:text-slate-500">:</span>
                  </div>
                  <textarea
                    id="message"
                    v-model="formData.message"
                    rows="4"
                    required
                    placeholder='"Escreva os detalhes da ideia ou projeto que deseja desenvolver..."'
                    class="w-full bg-slate-50 dark:bg-slate-950/40 border border-slate-200 dark:border-slate-800/80 rounded-xl p-3 text-slate-900 dark:text-slate-100 text-sm outline-hidden focus:border-violet-500 dark:focus:border-purple-500 focus:ring-1 focus:ring-purple-500/20 transition-all placeholder-slate-400/60 dark:placeholder-slate-600 resize-none"
                  ></textarea>
                </div>
              </div>

              <div class="flex items-center gap-4">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none">06</span>
                <span class="text-slate-400 dark:text-slate-600 font-bold text-base">}</span>
              </div>
            </div>

            <div
              class="border-t border-slate-200 dark:border-slate-800/80 pt-6 mt-8 flex flex-col sm:flex-row sm:items-center justify-between gap-4"
            >
              <div class="flex-1 min-h-8">
                <transition
                  enter-active-class="transition duration-300 ease-out"
                  enter-from-class="opacity-0 -translate-x-2"
                  enter-to-class="opacity-100 translate-x-0"
                >
                  <div
                    v-if="submitStatus === 'success'"
                    class="inline-flex items-center gap-2 px-2.5 py-1 bg-emerald-500/5 dark:bg-emerald-500/10 border border-emerald-500/20 text-emerald-600 dark:text-emerald-400 rounded-md text-xs font-semibold"
                  >
                    <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 animate-ping"></span>
                    <span>⚡ [200 OK]: Mensagem transmitida e indexada com sucesso!</span>
                  </div>
                </transition>

                <transition
                  enter-active-class="transition duration-300 ease-out"
                  enter-from-class="opacity-0 -translate-x-2"
                  enter-to-class="opacity-100 translate-x-0"
                >
                  <div
                    v-if="submitStatus === 'error'"
                    class="inline-flex items-center gap-2 px-2.5 py-1 bg-red-500/5 dark:bg-red-500/10 border border-red-500/20 text-red-600 dark:text-red-400 rounded-md text-xs font-semibold"
                  >
                    <span class="w-1.5 h-1.5 rounded-full bg-red-500 animate-ping"></span>
                    <span>❌ [500 Error]: Falha no disparo. Verifique os parâmetros de rede.</span>
                  </div>
                </transition>
              </div>

              <Button
                type="submit"
                variant="primary"
                :disabled="isSubmitting"
                class="w-full sm:w-auto shrink-0 group/btn relative overflow-hidden shadow-lg shadow-violet-500/10 dark:shadow-purple-500/5"
              >
                <template #icon-right>
                  <span
                    class="text-purple-300 dark:text-purple-400 font-bold transition-transform group-hover/btn:translate-x-1 duration-200"
                    >▶</span
                  >
                </template>
                {{ isSubmitting ? 'executing_payload...' : 'execute_contact.sh' }}
              </Button>
            </div>
          </form>
        </div>
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
  message: '',
})

const isSubmitting = ref(false)
const submitStatus = ref(null)

const handleSubmit = async () => {
  if (!formData.value.email || !formData.value.message) {
    submitStatus.value = 'error'
    return
  }

  isSubmitting.value = true
  submitStatus.value = null

  try {
    const CONTACT_EMAIL = 'devbrunoamorim@gmail.com'

    const response = await fetch(`https://formsubmit.co/ajax/${CONTACT_EMAIL}`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        Accept: 'application/json',
      },
      body: JSON.stringify({
        Nome: formData.value.name,
        Email: formData.value.email,
        Assunto: formData.value.subject || 'Sem Assunto',
        Mensagem: formData.value.message,
        _subject: `🚀 Novo contato do Portfólio: ${formData.value.subject || formData.value.name}`,
        _captcha: 'false',
      }),
    })

    if (response.ok) {
      submitStatus.value = 'success'
      formData.value = { name: '', email: '', subject: '', message: '' }
    } else {
      submitStatus.value = 'error'
    }
  } catch (error) {
    console.error('Erro no envio:', error)
    submitStatus.value = 'error'
  } finally {
    isSubmitting.value = false
    setTimeout(() => {
      submitStatus.value = null
    }, 5000)
  }
}
</script>
