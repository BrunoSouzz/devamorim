<template>
  <div
    class="site-cursor"
    :class="{ 'is-visible': isVisible, 'is-interactive': isInteractive, 'is-clicking': isClicking }"
    :style="{ '--cursor-x': `${position.x}px`, '--cursor-y': `${position.y}px` }"
    aria-hidden="true"
  >
    <span class="site-cursor__ring"></span>
    <span class="site-cursor__dot"></span>
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
  }, 280)
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

.site-cursor__ring,
.site-cursor__dot,
.site-cursor__label {
  position: absolute;
  display: block;
  transform: translate(-50%, -50%);
}

.site-cursor__ring {
  width: 34px;
  height: 34px;
  border: 1px solid rgb(129 140 248 / 75%);
  border-radius: 9999px;
  background: rgb(99 102 241 / 8%);
  box-shadow: 0 0 14px rgb(99 102 241 / 25%);
  transition:
    width 180ms ease,
    height 180ms ease,
    border-color 180ms ease,
    background-color 180ms ease,
    box-shadow 180ms ease;
}

.site-cursor__dot {
  width: 5px;
  height: 5px;
  border-radius: 9999px;
  background: #a5b4fc;
  box-shadow: 0 0 10px 2px rgb(129 140 248 / 80%);
}

.site-cursor__label {
  top: 28px;
  left: 28px;
  color: #c7d2fe;
  font: 700 8px/1 ui-monospace, SFMono-Regular, Menlo, monospace;
  letter-spacing: 0.12em;
  white-space: nowrap;
  opacity: 0;
  transition: opacity 180ms ease;
}

.site-cursor.is-interactive .site-cursor__ring {
  width: 48px;
  height: 48px;
  border-color: #818cf8;
  background: rgb(99 102 241 / 14%);
  box-shadow: 0 0 22px rgb(99 102 241 / 40%);
}

.site-cursor.is-interactive .site-cursor__dot {
  width: 7px;
  height: 7px;
  background: #e0e7ff;
}

.site-cursor.is-interactive .site-cursor__label {
  opacity: 1;
}

.site-cursor.is-clicking .site-cursor__ring {
  width: 58px;
  height: 58px;
  border-color: #c7d2fe;
  background: rgb(129 140 248 / 20%);
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
  .site-cursor__ring,
  .site-cursor__dot,
  .site-cursor__label {
    transition: none;
  }
}
</style>
