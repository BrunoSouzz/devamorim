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
          /contact_<span class="text-violet-600 dark:text-purple-400 animate-pulse">api</span>
        </h2>
        <p class="text-slate-500 dark:text-slate-400 font-mono text-xs sm:text-sm mt-2">
          // Envie uma requisição para iniciar uma nova conexão de projeto.
        </p>
      </div>

      <div
        class="w-full bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-800 rounded-2xl shadow-2xl overflow-hidden flex flex-col md:flex-row h-auto md:min-h-145"
      >
        <div
          class="w-full md:w-64 bg-slate-50 dark:bg-slate-900/60 border-b md:border-b-0 md:border-r border-slate-200 dark:border-slate-800 flex flex-col shrink-0"
        >
          <div
            class="px-4 py-3.5 border-b border-slate-200 dark:border-slate-800/60 flex items-center gap-2 select-none"
          >
            <span class="w-3 h-3 rounded-full bg-red-400 dark:bg-red-500/70"></span>
            <span class="w-3 h-3 rounded-full bg-yellow-400 dark:bg-yellow-500/70"></span>
            <span class="w-3 h-3 rounded-full bg-emerald-400 dark:bg-emerald-500/70"></span>
            <span class="ml-2 font-mono text-[10px] text-slate-400 dark:text-slate-500"
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
              <div class="space-y-1.5 pl-2">
                <a
                  href="mailto:devbrunoamorim@gmail.com"
                  class="flex items-center gap-2 p-2 rounded-lg hover:bg-slate-200/50 dark:hover:bg-slate-800/50 hover:text-violet-600 dark:hover:text-purple-400 transition-all duration-200 group"
                >
                  <span class="text-slate-400 group-hover:text-violet-500">✉️</span> mail.txt
                </a>
                <a
                  href="https://www.linkedin.com/in/dev-brunoamorim"
                  target="_blank"
                  class="flex items-center gap-2 p-2 rounded-lg hover:bg-slate-200/50 dark:hover:bg-slate-800/50 hover:text-violet-600 dark:hover:text-purple-400 transition-all duration-200 group"
                >
                  <span class="text-slate-400 group-hover:text-violet-500">💼</span> linkedin.url
                </a>
                <a
                  href="https://github.com/BrunoSouzz"
                  target="_blank"
                  class="flex items-center gap-2 p-2 rounded-lg hover:bg-slate-200/50 dark:hover:bg-slate-800/50 hover:text-violet-600 dark:hover:text-purple-400 transition-all duration-200 group"
                >
                  <span class="text-slate-400 group-hover:text-violet-500">🐙</span> github.sh
                </a>
              </div>
            </div>

            <div>
              <p
                class="text-[10px] font-bold text-slate-400 dark:text-slate-500 uppercase tracking-wider mb-2 select-none"
              >
                ⚡ system_status
              </p>
              <div class="pl-2">
                <div
                  class="inline-flex items-center gap-2 p-2 bg-emerald-500/5 dark:bg-emerald-500/10 border border-emerald-500/20 text-emerald-600 dark:text-emerald-400 rounded-lg text-[11px] font-bold uppercase tracking-wide"
                >
                  <span class="w-1.5 h-1.5 rounded-full bg-emerald-500 animate-pulse"></span>
                  <span>ONLINE_TO_HIRE</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="flex-1 flex flex-col bg-slate-100/30 dark:bg-slate-900/20">
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
            <div class="space-y-4 relative pl-8 sm:pl-12">
              <div
                class="absolute left-0 top-0 bottom-0 w-6 sm:w-8 border-r border-slate-200 dark:border-slate-800/60 text-right pr-2 text-xs text-slate-300 dark:text-slate-600 select-none space-y-7 pt-1"
              >
                <div>01</div>
                <div>02</div>
                <div>03</div>
                <div>04</div>
                <div>05</div>
                <div>06</div>
              </div>

              <div class="text-slate-400 dark:text-slate-600 font-bold text-base">{</div>

              <div class="space-y-5 pl-4 sm:pl-6">
                <div class="flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2">
                  <span class="text-violet-600 dark:text-purple-400 shrink-0"
                    >"remetente_nome"</span
                  >
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="name"
                    v-model="formData.name"
                    type="text"
                    required
                    placeholder='"Como quer ser chamado?"'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-violet-500 dark:focus:border-purple-500 text-slate-900 dark:text-slate-100 text-sm py-1 px-1 outline-hidden transition-colors placeholder-slate-400/70 dark:placeholder-slate-600"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>

                <div class="flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2">
                  <span class="text-violet-600 dark:text-purple-400 shrink-0"
                    >"remetente_email"</span
                  >
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="email"
                    v-model="formData.email"
                    type="email"
                    required
                    placeholder='"seu@email.com"'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-violet-500 dark:focus:border-purple-500 text-slate-900 dark:text-slate-100 text-sm py-1 px-1 outline-hidden transition-colors placeholder-slate-400/70 dark:placeholder-slate-600"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>

                <div class="flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2">
                  <span class="text-violet-600 dark:text-purple-400 shrink-0"
                    >"assunto_escopo"</span
                  >
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="subject"
                    v-model="formData.subject"
                    type="text"
                    required
                    placeholder='"Motivo do contato..."'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-violet-500 dark:focus:border-purple-500 text-slate-900 dark:text-slate-100 text-sm py-1 px-1 outline-hidden transition-colors placeholder-slate-400/70 dark:placeholder-slate-600"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>

                <div class="flex flex-col gap-1">
                  <div class="flex items-center gap-2">
                    <span class="text-violet-600 dark:text-purple-400">"corpo_mensagem"</span>
                    <span class="text-slate-400 dark:text-slate-500">:</span>
                  </div>
                  <textarea
                    id="message"
                    v-model="formData.message"
                    rows="4"
                    required
                    placeholder='"Escreva os detalhes da ideia ou projeto que deseja desenvolver..."'
                    class="w-full bg-slate-50 dark:bg-slate-950/40 border border-slate-200 dark:border-slate-800/80 rounded-xl p-3 text-slate-900 dark:text-slate-100 text-sm outline-hidden focus:border-violet-500 dark:focus:border-purple-500 transition-colors placeholder-slate-400/70 dark:placeholder-slate-600 resize-none mt-1"
                  ></textarea>
                </div>
              </div>

              <div class="text-slate-400 dark:text-slate-600 font-bold text-base">}</div>
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
                    class="inline-flex items-center gap-2 text-emerald-600 dark:text-emerald-400 text-xs"
                  >
                    <span class="w-2 h-2 rounded-full bg-emerald-500 animate-ping"></span>
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
                    class="inline-flex items-center gap-2 text-red-600 dark:text-red-400 text-xs"
                  >
                    <span class="w-2 h-2 rounded-full bg-red-500 animate-ping"></span>
                    <span>❌ [500 Error]: Falha no disparo. Verifique os parâmetros de rede.</span>
                  </div>
                </transition>
              </div>

              <Button
                type="submit"
                variant="primary"
                :disabled="isSubmitting"
                class="w-full sm:w-auto shrink-0 group/btn relative overflow-hidden"
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
