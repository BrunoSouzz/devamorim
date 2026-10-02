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
  color: #e0e7ff;
  font: 800 17px/1 ui-monospace, SFMono-Regular, Menlo, monospace;
  letter-spacing: -0.14em;
  text-shadow: 0 0 8px rgb(99 102 241 / 75%);
  filter: drop-shadow(0 1px 3px rgb(2 6 23 / 85%));
}

.site-cursor__trail {
  width: 25px;
  height: 25px;
  border: 1px solid rgb(129 140 248 / 55%);
  border-radius: 999px;
  background: rgb(99 102 241 / 8%);
  box-shadow:
    0 0 9px rgb(99 102 241 / 35%),
    inset 0 0 7px rgb(165 180 252 / 12%);
  opacity: 0.85;
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
  top: 18px;
  left: 18px;
  padding: 4px 6px;
  border: 1px solid rgb(129 140 248 / 35%);
  border-radius: 4px;
  background: rgb(9 9 11 / 82%);
  color: #a5b4fc;
  font: 700 7px/1 ui-monospace, SFMono-Regular, Menlo, monospace;
  letter-spacing: 0.1em;
  white-space: nowrap;
  opacity: 0;
  transform: translateY(3px);
  transition:
    opacity 180ms ease,
    transform 180ms ease;
}

.site-cursor.is-interactive .site-cursor__mark {
  transform: translate(-50%, -50%) scale(1.22);
  filter: drop-shadow(0 2px 5px rgb(2 6 23 / 90%));
}

.site-cursor.is-interactive .site-cursor__trail {
  transform: translate(-50%, -50%) scale(1.3);
  border-color: #a5b4fc;
  background: rgb(99 102 241 / 14%);
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
  transform: translate(-50%, -50%) scale(1.55);
  border-color: #c7d2fe;
  opacity: 0;
}

.site-cursor.is-clicking::after {
  position: absolute;
  top: 0;
  left: 0;
  width: 34px;
  height: 34px;
  border: 1px solid rgb(129 140 248 / 45%);
  border-radius: 999px;
  content: '';
  transform: translate(-50%, -50%);
  animation: cursor-click 260ms ease-out both;
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

@keyframes cursor-click {
  from {
    opacity: 0.8;
    transform: translate(-50%, -50%) scale(0.6);
  }

  to {
    opacity: 0;
    transform: translate(-50%, -50%) scale(1.25);
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
  .site-cursor__label,
  .site-cursor.is-clicking::after {
    transition: none;
    animation: none;
  }
}
</style>
