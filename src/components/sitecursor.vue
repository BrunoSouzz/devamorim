<template>
  <div
    class="site-cursor"
    :class="{
      'is-visible': isVisible,
      'is-interactive': isInteractive,
      'is-clicking': isClicking,
    }"
    :style="{ '--cursor-x': `${position.x}px`, '--cursor-y': `${position.y}px` }"
    aria-hidden="true"
  >
    <span class="site-cursor__trail" aria-hidden="true"></span>
    <span class="site-cursor__mark" aria-hidden="true">
      <span class="site-cursor__prompt">&gt;</span>
      <span class="site-cursor__underscore">_</span>
    </span>
    <span v-if="cursorLabel" class="site-cursor__label">{{ cursorLabel }}</span>
  </div>
</template>

<script setup>
import { onBeforeUnmount, onMounted, reactive, ref } from 'vue'

const position = reactive({ x: 0, y: 0 })
const isVisible = ref(false)
const isInteractive = ref(false)
const isClicking = ref(false)
const cursorLabel = ref('')

let clickTimeout

const getInteractiveTarget = (target) => {
  if (!(target instanceof Element)) return null
  return target.closest('a, button, input, textarea, select, [role="button"], [data-cursor]')
}

const updateInteractiveState = (target) => {
  const interactiveTarget = getInteractiveTarget(target)
  isInteractive.value = Boolean(interactiveTarget)

  if (!interactiveTarget) {
    cursorLabel.value = ''
    return
  }

  cursorLabel.value =
    interactiveTarget.dataset.cursor ||
    ({
      A: 'OPEN',
      BUTTON: 'RUN',
      INPUT: 'TYPE',
      TEXTAREA: 'TYPE',
      SELECT: 'PICK',
    }[interactiveTarget.tagName] ||
      '')
}

const onPointerMove = (event) => {
  position.x = event.clientX
  position.y = event.clientY
  isVisible.value = true
  updateInteractiveState(event.target)
}

const onPointerLeave = () => {
  isVisible.value = false
}

const onPointerDown = () => {
  isClicking.value = true
  clearTimeout(clickTimeout)
  clickTimeout = window.setTimeout(() => {
    isClicking.value = false
  }, 260)
}

onMounted(() => {
  document.addEventListener('pointermove', onPointerMove)
  document.addEventListener('pointerleave', onPointerLeave)
  document.addEventListener('pointerdown', onPointerDown)
})

onBeforeUnmount(() => {
  document.removeEventListener('pointermove', onPointerMove)
  document.removeEventListener('pointerleave', onPointerLeave)
  document.removeEventListener('pointerdown', onPointerDown)
  clearTimeout(clickTimeout)
})
</script>

<style scoped>
.site-cursor {
  --cursor-x: 0px;
  --cursor-y: 0px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  width: 0;
  height: 0;
  pointer-events: none;
  opacity: 0;
  transform: translate3d(var(--cursor-x), var(--cursor-y), 0);
  transition: opacity 180ms ease;
}

.site-cursor.is-visible {
  opacity: 1;
}

.site-cursor__trail,
.site-cursor__mark {
  position: absolute;
  top: 0;
  left: 0;
  transform: translate(-50%, -50%);
  transition:
    transform 180ms ease,
    filter 180ms ease,
    opacity 180ms ease;
}

.site-cursor__mark {
  display: flex;
  align-items: baseline;
  color: #c7d2fe;
  font: 800 20px/1 ui-monospace, SFMono-Regular, Menlo, monospace;
  letter-spacing: -0.16em;
  text-shadow:
    0 0 6px rgb(165 180 252 / 100%),
    0 0 16px rgb(99 102 241 / 75%);
  filter: drop-shadow(0 2px 4px rgb(2 6 23 / 90%));
}

.site-cursor__trail {
  width: 27px;
  height: 27px;
  border: 1px solid rgb(165 180 252 / 70%);
  border-radius: 5px;
  background: rgb(99 102 241 / 16%);
  box-shadow:
    0 0 11px rgb(99 102 241 / 50%),
    inset 0 0 9px rgb(165 180 252 / 22%);
  opacity: 0.9;
}

.site-cursor__prompt {
  color: #818cf8;
}

.site-cursor__underscore {
  color: #e0e7ff;
  animation: cursor-blink 900ms steps(1) infinite;
}

.site-cursor__label {
  position: absolute;
  top: 22px;
  left: 22px;
  color: #c7d2fe;
  font: 700 8px/1 ui-monospace, SFMono-Regular, Menlo, monospace;
  letter-spacing: 0.12em;
  white-space: nowrap;
  opacity: 0;
  transform: translateY(4px);
  transition:
    opacity 180ms ease,
    transform 180ms ease;
}

.site-cursor.is-interactive .site-cursor__mark {
  transform: translate(-50%, -50%) scale(1.22);
  filter: drop-shadow(0 2px 5px rgb(2 6 23 / 90%));
}

.site-cursor.is-interactive .site-cursor__trail {
  transform: translate(-50%, -50%) scale(1.35) rotate(45deg);
  border-color: #a5b4fc;
  background: rgb(99 102 241 / 24%);
  opacity: 1;
}

.site-cursor.is-interactive .site-cursor__label {
  opacity: 1;
  transform: translateY(0);
}

.site-cursor.is-clicking .site-cursor__mark {
  transform: translate(-50%, -50%) scale(0.82);
  color: #ffffff;
}

.site-cursor.is-clicking .site-cursor__trail {
  transform: translate(-50%, -50%) scale(1.7);
  border-color: #c7d2fe;
  opacity: 0;
}

@keyframes cursor-blink {
  0%,
  45% {
    opacity: 1;
  }
  46%,
  100% {
    opacity: 0.25;
  }
}

@media (hover: hover) and (pointer: fine) {
  :global(html),
  :global(body),
  :global(a),
  :global(button),
  :global([role='button']) {
    cursor: none;
  }

  :global(input),
  :global(textarea) {
    cursor: text;
  }
}

@media (prefers-reduced-motion: reduce) {
  .site-cursor,
  .site-cursor__trail,
  .site-cursor__mark,
  .site-cursor__label {
    transition: none;
    animation: none;
  }
}
</style>
