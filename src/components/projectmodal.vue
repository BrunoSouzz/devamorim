<!-- eslint-disable vue/multi-word-component-names -->

<template>
  <Transition name="project-modal">
    <div
      v-if="project"
      class="fixed inset-0 z-70 flex items-center justify-center p-4 sm:p-6"
      role="dialog"
      aria-modal="true"
      :aria-label="`Detalhes do projeto ${project.title}`"
      @click.self="$emit('close')"
    >
      <div class="absolute inset-0 bg-slate-950/70 backdrop-blur-sm"></div>

      <article
        class="relative z-10 w-full max-w-5xl max-h-[calc(100vh-3rem)] overflow-y-auto rounded-2xl border border-slate-200 dark:border-zinc-800/90 bg-white dark:bg-zinc-950 shadow-2xl shadow-black/30"
      >
        <div class="flex items-center justify-between border-b border-slate-200 dark:border-zinc-800 px-4 py-3 font-mono text-xs">
          <div class="flex items-center gap-2 text-slate-500 dark:text-zinc-400">
            <span class="text-indigo-500">&gt;_</span>
            <span>project.details</span>
            <span class="text-slate-300 dark:text-zinc-700">/</span>
            <span class="text-slate-900 dark:text-zinc-100">{{ project.title }}</span>
          </div>
          <span class="text-indigo-500">cd ..</span>
        </div>

        <div class="grid gap-8 p-6 sm:p-9 md:grid-cols-[minmax(0,0.9fr)_minmax(360px,1.1fr)]">
          <div>
            <p class="mb-3 font-mono text-[10px] font-bold uppercase tracking-[0.18em] text-indigo-500">
              PROJECT_OVERVIEW
            </p>
            <h2 class="mb-4 text-3xl font-mono font-bold text-slate-950 dark:text-white sm:text-4xl">
              {{ project.title }}
            </h2>
            <p class="text-base leading-8 text-slate-600 dark:text-zinc-400">
              {{ project.details || project.description }}
            </p>

            <div class="mt-6 flex flex-wrap gap-2">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="rounded border border-indigo-200 bg-indigo-500/5 px-2.5 py-1 font-mono text-[10px] font-bold tracking-wide text-indigo-600 dark:border-indigo-500/20 dark:bg-indigo-500/10 dark:text-indigo-300"
              >
                {{ tag }}
              </span>
            </div>

            <div class="mt-7 flex flex-wrap gap-3">
              <a
                v-if="project.githubLink"
                :href="project.githubLink"
                target="_blank"
                rel="noopener noreferrer"
                class="rounded-lg border border-slate-200 px-3 py-2 font-mono text-xs font-bold text-slate-600 transition-colors hover:border-indigo-400 hover:text-indigo-600 dark:border-zinc-800 dark:text-zinc-300 dark:hover:border-indigo-400 dark:hover:text-indigo-300"
              >
                ~ git
              </a>
              <a
                v-if="project.liveLink"
                :href="project.liveLink"
                target="_blank"
                rel="noopener noreferrer"
                class="rounded-lg bg-indigo-600 px-3 py-2 font-mono text-xs font-bold text-white transition-colors hover:bg-indigo-500"
              >
                ~ live
              </a>
            </div>
          </div>

          <div v-if="project.image" class="flex min-h-64 items-center">
            <img
              :src="project.image"
              :alt="`Imagem do projeto ${project.title}`"
              class="max-h-[28rem] w-full rounded-xl border border-slate-200 object-cover shadow-lg shadow-slate-950/10 dark:border-zinc-800 dark:shadow-black/20"
            />
          </div>
          <div
            v-else
            class="flex min-h-64 items-center justify-center rounded-xl border border-dashed border-slate-200 bg-slate-50 font-mono text-xs text-slate-400 dark:border-zinc-800 dark:bg-zinc-900/50 dark:text-zinc-500"
          >
            IMAGE_NOT_AVAILABLE
          </div>
        </div>
      </article>
    </div>
  </Transition>
</template>

<script setup>
import { onBeforeUnmount, onMounted, watch } from 'vue'

const props = defineProps({
  project: {
    type: Object,
    default: null,
  },
})

const emit = defineEmits(['close'])

const onKeydown = (event) => {
  if (event.key === 'Escape' && props.project) {
    emit('close')
  }
}

const updateBodyLock = (project) => {
  document.body.style.overflow = project ? 'hidden' : ''
}

watch(() => props.project, updateBodyLock, { immediate: true })

onMounted(() => {
  document.addEventListener('keydown', onKeydown)
})

onBeforeUnmount(() => {
  document.removeEventListener('keydown', onKeydown)
  document.body.style.overflow = ''
})
</script>

<style scoped>
.project-modal-enter-active,
.project-modal-leave-active {
  transition: opacity 180ms ease;
}

.project-modal-enter-active article,
.project-modal-leave-active article {
  transition: transform 180ms ease, opacity 180ms ease;
}

.project-modal-enter-from,
.project-modal-leave-to {
  opacity: 0;
}

.project-modal-enter-from article,
.project-modal-leave-to article {
  opacity: 0;
  transform: translateY(12px) scale(0.98);
}
</style>
