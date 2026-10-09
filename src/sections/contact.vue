<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section
    id="contact"
    class="section-reveal relative overflow-hidden bg-slate-50 py-20 text-slate-900 transition-colors duration-300 dark:bg-[#09090b] dark:text-white"
  >
    <div class="w-full max-w-5xl mx-auto px-6 relative z-10">
      <div class="mb-12 flex flex-col items-center text-center">
        <div class="mb-3 flex items-center gap-2 font-mono text-xs text-slate-500 dark:text-zinc-500 sm:text-sm">
          <span class="text-slate-500 dark:text-slate-500">bruno@portfolio:~$</span>
          <span class="text-indigo-600 dark:text-indigo-400 font-semibold">node contact.js</span>
          <span class="terminal-blink h-3.5 w-1 bg-indigo-500"></span>
        </div>
        <h2 class="mb-4 text-3xl font-mono font-bold tracking-tight text-slate-900 dark:text-white sm:text-4xl md:text-5xl">
          Contato
        </h2>
        <p class="mx-auto max-w-2xl text-sm leading-relaxed text-slate-600 dark:text-zinc-400 sm:text-base">
          Envie uma requisição para iniciar uma nova conexão de projeto, discutir uma oportunidade ou apenas trocar uma ideia.
        </p>

        <button
          type="button"
          @click="copyEmail"
          class="mt-5 inline-flex items-center gap-2 rounded-md border border-slate-200 bg-white/70 px-3.5 py-2 font-mono text-xs text-slate-600 transition-colors hover:border-indigo-400/60 hover:text-indigo-600 dark:border-zinc-800 dark:bg-zinc-900/60 dark:text-zinc-300 dark:hover:border-indigo-400/60 dark:hover:text-indigo-300"
        >
          <span class="text-indigo-500" aria-hidden="true">&gt;_</span>
          <span>{{ emailCopyLabel }}</span>
        </button>
        <p v-if="emailCopyError" class="mt-2 text-xs text-red-500 dark:text-red-400" role="status">
          Não foi possível copiar automaticamente. Use: {{ contactEmail }}
        </p>

      </div>

      <div
        class="contact-panel relative flex h-auto w-full flex-col overflow-hidden rounded-lg border border-slate-200 bg-white/70 dark:border-zinc-800 dark:bg-zinc-900/35 md:min-h-145 md:flex-row"
      >
        <div class="contact-panel__scan pointer-events-none absolute inset-y-0 left-0 w-px bg-linear-to-b from-transparent via-indigo-400/70 to-transparent" aria-hidden="true"></div>
        <div
          class="hidden"
        >
          <div
            class="flex items-center gap-2 border-b border-slate-200 px-4 py-3.5 select-none dark:border-zinc-800"
          >
            <button
              type="button"
              class="group relative h-3 w-3 cursor-pointer rounded-full bg-red-400 transition-transform hover:scale-125 focus:outline-hidden focus:ring-2 focus:ring-red-400/50 dark:bg-red-500/60"
              aria-label="Limpar todos os campos do formulário"
              title="Limpar formulário"
              @click="clearForm"
            >
              <span class="pointer-events-none absolute left-1/2 top-1/2 hidden -translate-x-1/2 -translate-y-1/2 text-[8px] font-bold leading-none text-red-950 group-hover:block">×</span>
            </button>
            <button
              type="button"
              class="group relative h-3 w-3 cursor-pointer rounded-full bg-yellow-400 transition-transform hover:scale-125 focus:outline-hidden focus:ring-2 focus:ring-yellow-400/50 dark:bg-yellow-500/60"
              :aria-label="isComposerMinimized ? 'Restaurar formulário de contato' : 'Minimizar formulário de contato'"
              :title="isComposerMinimized ? 'Restaurar formulário' : 'Minimizar formulário'"
              @click="toggleMinimize"
            >
              <span class="pointer-events-none absolute left-1/2 top-1/2 hidden -translate-x-1/2 -translate-y-1/2 text-[8px] font-bold leading-none text-yellow-950 group-hover:block">−</span>
            </button>
            <button
              type="button"
              class="group relative h-3 w-3 cursor-pointer rounded-full bg-emerald-400 transition-transform hover:scale-125 focus:outline-hidden focus:ring-2 focus:ring-emerald-400/50 dark:bg-emerald-500/60"
              aria-label="Focar no primeiro campo do formulário"
              title="Começar a escrever"
              @click="focusComposer"
            >
              <span class="pointer-events-none absolute left-1/2 top-1/2 hidden -translate-x-1/2 -translate-y-1/2 text-[7px] font-bold leading-none text-emerald-950 group-hover:block">↗</span>
            </button>
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
                  class="flex items-center gap-2 px-2 py-1.5 rounded-lg hover:bg-slate-200/60 dark:hover:bg-slate-800/50 text-slate-600 dark:text-slate-400 hover:text-indigo-600 dark:hover:text-indigo-400 transition-all duration-200 group"
                >
                  <svg class="w-3.5 h-3.5 text-slate-400 group-hover:text-indigo-500 dark:group-hover:text-indigo-400 fill-none stroke-current stroke-2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                  </svg>
                  <span>mail.txt</span>
                </a>

                <a
                  href="https://www.linkedin.com/in/dev-brunoamorim"
                  target="_blank"
                  class="flex items-center gap-2 px-2 py-1.5 rounded-lg hover:bg-slate-200/60 dark:hover:bg-slate-800/50 text-slate-600 dark:text-slate-400 hover:text-indigo-600 dark:hover:text-indigo-400 transition-all duration-200 group"
                >
                  <svg class="w-3.5 h-3.5 text-slate-400 group-hover:text-indigo-500 dark:group-hover:text-indigo-400 fill-current" viewBox="0 0 24 24">
                    <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.8v8h2.8v-4.16c0-.22 0-.45.06-.62a1.12 1.12 0 0 1 1-.77c.76 0 1 .56 1 1.39v4.16h2.8M6.5 8.37a1.37 1.37 0 1 0 0-2.75 1.37 1.37 0 0 0 0 2.75M8 18.5v-8H5v8h3z"/>
                  </svg>
                  <span>linkedin.url</span>
                </a>

                <a
                  href="https://github.com/BrunoSouzz"
                  target="_blank"
                  class="flex items-center gap-2 px-2 py-1.5 rounded-lg hover:bg-slate-200/60 dark:hover:bg-slate-800/50 text-slate-600 dark:text-slate-400 hover:text-indigo-600 dark:hover:text-indigo-400 transition-all duration-200 group"
                >
                  <svg class="w-3.5 h-3.5 text-slate-400 group-hover:text-indigo-500 dark:group-hover:text-indigo-400 fill-current" viewBox="0 0 24 24">
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

        <div class="flex flex-1 flex-col bg-white/30 dark:bg-zinc-950/10">
          <nav class="flex flex-wrap items-center gap-1 border-b border-slate-200 bg-slate-50/70 px-3 py-2 dark:border-zinc-800 dark:bg-zinc-950/30" aria-label="Abas de contato">
            <button
              v-for="tab in contactTabs"
              :key="tab.id"
              type="button"
              :class="[
                'rounded-md px-3 py-1.5 font-mono text-[11px] transition-colors',
                activeTab === tab.id
                  ? 'bg-white text-indigo-600 shadow-xs dark:bg-zinc-900 dark:text-indigo-300'
                  : 'text-slate-500 hover:bg-white/70 hover:text-indigo-600 dark:text-zinc-500 dark:hover:bg-zinc-900/60 dark:hover:text-indigo-300',
              ]"
              :aria-selected="activeTab === tab.id"
              role="tab"
              @click="activeTab = tab.id"
            >
              {{ tab.label }}
            </button>
          </nav>
          <div
            v-if="activeTab === 'email'"
            class="flex items-center border-b border-slate-200 bg-slate-50/70 px-4 select-none dark:border-zinc-800 dark:bg-zinc-950/30"
          >
            <div
              class="bg-white dark:bg-slate-900 border-r border-l border-t-2 border-t-indigo-500 dark:border-t-indigo-400 border-slate-200 dark:border-slate-800 px-4 py-2.5 flex items-center gap-2 text-xs font-mono font-bold text-slate-800 dark:text-slate-200"
            >
              <span class="text-yellow-500 font-bold">{}</span> payload_message.json
            </div>
          </div>

          <form
            v-if="activeTab === 'email'"
            @submit.prevent="handleSubmit"
            :class="[
              'relative flex flex-1 flex-col justify-between font-mono text-sm transition-[max-height,padding] duration-300',
              'p-6 md:p-8',
            ]"
          >
            <div class="space-y-4">

              <div class="flex items-center gap-4">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none">01</span>
                <span class="text-slate-400 dark:text-slate-600 font-bold text-base">{</span>
              </div>

              <div class="flex items-start sm:items-center gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1 sm:pt-0">02</span>
                <div class="flex-1 flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2 pl-4">
                  <label for="name" class="text-indigo-600 dark:text-indigo-400 shrink-0 font-medium">"remetente_nome"</label>
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="name"
                    ref="nameInput"
                    v-model="formData.name"
                    type="text"
                    required
                    placeholder='"Como quer ser chamado?"'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-indigo-500 dark:focus:border-indigo-500 text-slate-900 dark:text-slate-100 text-sm py-0.5 px-1 outline-hidden transition-all placeholder-slate-400/60 dark:placeholder-slate-600 focus:placeholder-slate-300"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>
              </div>

              <div class="flex items-start sm:items-center gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1 sm:pt-0">03</span>
                <div class="flex-1 flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2 pl-4">
                  <label for="email" class="text-indigo-600 dark:text-indigo-400 shrink-0 font-medium">"remetente_email"</label>
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="email"
                    v-model="formData.email"
                    type="email"
                    required
                    placeholder='"seu@email.com"'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-indigo-500 dark:focus:border-indigo-500 text-slate-900 dark:text-slate-100 text-sm py-0.5 px-1 outline-hidden transition-all placeholder-slate-400/60 dark:placeholder-slate-600 focus:placeholder-slate-300"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>
              </div>

              <div class="flex items-start sm:items-center gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1 sm:pt-0">04</span>
                <div class="flex-1 flex flex-col sm:flex-row sm:items-center gap-1 sm:gap-2 pl-4">
                  <label for="subject" class="text-indigo-600 dark:text-indigo-400 shrink-0 font-medium">"assunto_escopo"</label>
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">:</span>
                  <input
                    id="subject"
                    v-model="formData.subject"
                    type="text"
                    required
                    placeholder='"Motivo do contato..."'
                    class="flex-1 bg-transparent border-b border-dashed border-slate-300 dark:border-slate-700 focus:border-indigo-500 dark:focus:border-indigo-500 text-slate-900 dark:text-slate-100 text-sm py-0.5 px-1 outline-hidden transition-all placeholder-slate-400/60 dark:placeholder-slate-600 focus:placeholder-slate-300"
                  />
                  <span class="text-slate-400 dark:text-slate-500 hidden sm:inline">,</span>
                </div>
              </div>

              <div class="flex items-start gap-4 group">
                <span class="w-6 text-right text-xs text-slate-300 dark:text-slate-600 select-none pt-1">05</span>
                <div class="flex-1 flex flex-col gap-2 pl-4">
                  <div class="flex items-center gap-2">
                    <label for="message" class="text-indigo-600 dark:text-indigo-400 font-medium">"corpo_mensagem"</label>
                    <span class="text-slate-400 dark:text-slate-500">:</span>
                  </div>
                  <textarea
                    id="message"
                    v-model="formData.message"
                    rows="4"
                    required
                    placeholder='"Escreva os detalhes da ideia ou projeto que deseja desenvolver..."'
                    class="w-full bg-slate-50 dark:bg-slate-950/40 border border-slate-200 dark:border-slate-800/80 rounded-xl p-3 text-slate-900 dark:text-slate-100 text-sm outline-hidden focus:border-indigo-500 dark:focus:border-indigo-500 focus:ring-1 focus:ring-indigo-500/20 transition-all placeholder-slate-400/60 dark:placeholder-slate-600 resize-none"
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
                class="w-full sm:w-auto shrink-0 group/btn relative overflow-hidden shadow-lg shadow-indigo-500/10 dark:shadow-indigo-500/5"
              >
                <template #icon-right>
                  <span
                    class="text-indigo-300 dark:text-indigo-400 font-bold transition-transform group-hover/btn:translate-x-1 duration-200"
                    >▶</span
                  >
                </template>
                {{ isSubmitting ? 'executing_payload...' : 'execute_contact.sh' }}
              </Button>
            </div>
          </form>

          <div v-else-if="activeTab === 'profiles'" class="relative grid flex-1 gap-6 overflow-hidden p-6 md:grid-cols-2 md:p-8" role="tabpanel">
            <div class="pointer-events-none absolute inset-x-8 top-5 flex items-end gap-1 opacity-40" aria-hidden="true">
              <span class="h-2 w-1 animate-pulse rounded-full bg-indigo-400"></span>
              <span class="h-4 w-1 animate-pulse rounded-full bg-indigo-500 [animation-delay:150ms]"></span>
              <span class="h-7 w-1 animate-pulse rounded-full bg-indigo-400 [animation-delay:300ms]"></span>
              <span class="h-3 w-1 animate-pulse rounded-full bg-indigo-500 [animation-delay:450ms]"></span>
              <span class="ml-1 font-mono text-[10px] text-indigo-500">syncing_profiles...</span>
            </div>
            <div class="group relative overflow-hidden rounded-lg border border-slate-200 bg-white/60 p-5 transition-all duration-300 hover:-translate-y-1 hover:border-sky-400/60 hover:shadow-lg hover:shadow-sky-500/10 dark:border-zinc-800 dark:bg-zinc-900/30 dark:hover:border-sky-400/50">
              <div class="absolute right-0 top-0 h-24 w-24 rounded-full bg-sky-400/10 blur-2xl transition-opacity group-hover:opacity-100 dark:bg-sky-500/10" aria-hidden="true"></div>
              <div class="relative mb-5 flex items-start justify-between">
                <div class="flex items-center gap-3">
                  <div class="flex h-14 w-14 items-center justify-center rounded-xl border border-sky-400/30 bg-sky-500/10 text-sky-600 dark:text-sky-300">
                    <svg class="h-7 w-7" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                      <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.35V8.999h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.287ZM5.337 7.433a2.062 2.062 0 1 1 0-4.125 2.062 2.062 0 0 1 0 4.125ZM3.555 20.452h3.563V8.999H3.555v11.453Z"/>
                    </svg>
                  </div>
                  <div>
                    <h3 class="font-mono text-base font-bold text-slate-900 dark:text-white">LinkedIn</h3>
                    <p class="font-mono text-[11px] text-slate-500 dark:text-zinc-500">@dev-brunoamorim</p>
                  </div>
                </div>
                <span class="flex items-center gap-1.5 font-mono text-[10px] text-emerald-600 dark:text-emerald-400">
                  <span class="h-1.5 w-1.5 rounded-full bg-emerald-500 animate-pulse"></span>
                  online
                </span>
              </div>
              <p class="relative mb-5 min-h-18 text-sm leading-relaxed text-slate-600 dark:text-zinc-400">
                Acompanhe minha trajetória profissional, experiências acadêmicas e os projetos em que estou transformando ideias em soluções digitais.
              </p>
              <a href="https://www.linkedin.com/in/dev-brunoamorim" target="_blank" rel="noopener noreferrer" class="relative inline-flex items-center gap-2 rounded-md border border-sky-400/40 bg-sky-500/5 px-3 py-2 font-mono text-xs text-sky-700 transition-colors hover:border-sky-400 hover:bg-sky-500/10 dark:text-sky-300">
                abrir_linkedin <span aria-hidden="true">↗</span>
              </a>
            </div>
            <div class="group relative overflow-hidden rounded-lg border border-slate-200 bg-white/60 p-5 transition-all duration-300 hover:-translate-y-1 hover:border-indigo-400/60 hover:shadow-lg hover:shadow-indigo-500/10 dark:border-zinc-800 dark:bg-zinc-900/30 dark:hover:border-indigo-400/50">
              <div class="absolute right-0 top-0 h-24 w-24 rounded-full bg-indigo-400/10 blur-2xl transition-opacity group-hover:opacity-100 dark:bg-indigo-500/10" aria-hidden="true"></div>
              <div class="relative mb-5 flex items-start justify-between">
                <div class="flex items-center gap-3">
                  <div class="flex h-14 w-14 items-center justify-center rounded-xl border border-indigo-400/30 bg-indigo-500/10 text-indigo-600 dark:text-indigo-300">
                    <svg class="h-7 w-7" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
                      <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.5.5.092.682-.217.682-.483 0-.237-.008-.866-.013-1.7-2.782.605-3.369-1.342-3.369-1.342-.454-1.157-1.11-1.465-1.11-1.465-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.094.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0 1 12 6.844a9.5 9.5 0 0 1 2.504.337c1.909-1.296 2.747-1.026 2.747-1.026.546 1.378.203 2.397.1 2.65.64.7 1.028 1.594 1.028 2.688 0 3.848-2.339 4.69-4.566 4.943.359.31.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.02 10.02 0 0 0 22 12.017C22 6.484 17.523 2 12 2Z" clip-rule="evenodd"/>
                    </svg>
                  </div>
                  <div>
                    <h3 class="font-mono text-base font-bold text-slate-900 dark:text-white">GitHub</h3>
                    <p class="font-mono text-[11px] text-slate-500 dark:text-zinc-500">@BrunoSouzz</p>
                  </div>
                </div>
                <span class="flex items-center gap-1.5 font-mono text-[10px] text-emerald-600 dark:text-emerald-400">
                  <span class="h-1.5 w-1.5 rounded-full bg-emerald-500 animate-pulse"></span>
                  active
                </span>
              </div>
              <p class="relative mb-5 min-h-18 text-sm leading-relaxed text-slate-600 dark:text-zinc-400">
                Explore meus repositórios, estudos e projetos em produção. É onde compartilho código, experimentos e minha evolução como desenvolvedor.
              </p>
              <a href="https://github.com/BrunoSouzz" target="_blank" rel="noopener noreferrer" class="relative inline-flex items-center gap-2 rounded-md border border-indigo-400/40 bg-indigo-500/5 px-3 py-2 font-mono text-xs text-indigo-700 transition-colors hover:border-indigo-400 hover:bg-indigo-500/10 dark:text-indigo-300">
                abrir_github <span aria-hidden="true">↗</span>
              </a>
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import Button from '@/components/button.vue'

const contactEmail = 'devbrunoamorim@gmail.com'
const activeTab = ref('email')
const isComposerMinimized = ref(false)
const nameInput = ref(null)
const contactTabs = [
  { id: 'email', label: 'payload_message.json' },
  { id: 'profiles', label: 'profiles.json' },
]
const emailCopyLabel = ref('Copiar e-mail')
const emailCopyError = ref(false)

const copyEmail = async () => {
  emailCopyError.value = false

  try {
    await navigator.clipboard.writeText(contactEmail)
    emailCopyLabel.value = 'E-mail copiado!'
    setTimeout(() => {
      emailCopyLabel.value = 'Copiar e-mail'
    }, 2500)
  } catch (error) {
    console.error('Erro ao copiar e-mail:', error)
    emailCopyError.value = true
  }
}

const clearForm = () => {
  formData.value = { name: '', email: '', subject: '', message: '' }
  submitStatus.value = null
  emailCopyError.value = false
}

const toggleMinimize = () => {
  isComposerMinimized.value = !isComposerMinimized.value
}

const focusComposer = () => {
  isComposerMinimized.value = false
  requestAnimationFrame(() => nameInput.value?.focus())
}

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
    const response = await fetch(`https://formsubmit.co/ajax/${contactEmail}`, {
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

<style scoped>
.contact-panel {
  animation: contact-panel-in 700ms ease-out both;
}

.contact-panel::before {
  position: absolute;
  inset: 0;
  border: 1px solid transparent;
  border-radius: inherit;
  background: linear-gradient(120deg, transparent 25%, rgb(99 102 241 / 0.28), transparent 75%) border-box;
  content: '';
  pointer-events: none;
  mask: linear-gradient(#000 0 0) padding-box, linear-gradient(#000 0 0);
  mask-composite: exclude;
  animation: contact-border-flow 5s ease-in-out infinite;
}

.contact-panel__scan {
  animation: contact-scan 4.5s ease-in-out infinite;
}

@keyframes contact-panel-in {
  from {
    opacity: 0;
    transform: translateY(10px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes contact-border-flow {
  0%,
  100% {
    opacity: 0.25;
    background-position: 0% 50%;
  }

  50% {
    opacity: 0.75;
    background-position: 100% 50%;
  }
}

@keyframes contact-scan {
  0%,
  100% {
    opacity: 0;
    transform: translateY(-15%);
  }

  20%,
  80% {
    opacity: 0.7;
  }

  50% {
    opacity: 1;
    transform: translateY(115%);
  }
}

@media (prefers-reduced-motion: reduce) {
  .contact-panel,
  .contact-panel::before,
  .contact-panel__scan {
    animation: none;
  }
}
</style>
