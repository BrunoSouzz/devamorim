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
    <img class="site-cursor__trail" :src="logoUrl" alt="" />
    <img class="site-cursor__logo" :src="logoUrl" alt="" />
    <span v-if="cursorLabel" class="site-cursor__label">{{ cursorLabel }}</span>
  </div>
</template>

<script setup>
import { onBeforeUnmount, onMounted, reactive, ref } from 'vue'
import logoUrl from '../assets/images/l32.svg'

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

.site-cursor__logo,
.site-cursor__trail {
  position: absolute;
  top: 0;
  left: 0;
  width: 30px;
  height: 30px;
  object-fit: contain;
  transform: translate(-7px, -7px);
  transition:
    width 180ms ease,
    height 180ms ease,
    transform 180ms ease,
    filter 180ms ease,
    opacity 180ms ease;
}

.site-cursor__logo {
  filter: drop-shadow(0 0 5px rgb(99 102 241 / 55%));
}

.site-cursor__trail {
  transform: translate(-2px, -2px) scale(0.72);
  filter: blur(5px) drop-shadow(0 0 8px rgb(99 102 241 / 45%));
  opacity: 0.35;
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

.site-cursor.is-interactive .site-cursor__logo {
  width: 38px;
  height: 38px;
  transform: translate(-9px, -9px) rotate(-8deg);
  filter: drop-shadow(0 0 9px rgb(129 140 248 / 85%));
}

.site-cursor.is-interactive .site-cursor__trail {
  transform: translate(3px, 3px) scale(0.85) rotate(-8deg);
  opacity: 0.5;
}

.site-cursor.is-interactive .site-cursor__label {
  opacity: 1;
  transform: translateY(0);
}

.site-cursor.is-clicking .site-cursor__logo {
  transform: translate(-9px, -9px) scale(0.78) rotate(8deg);
  filter: drop-shadow(0 0 14px rgb(165 180 252 / 100%));
}

.site-cursor.is-clicking .site-cursor__trail {
  transform: translate(7px, 7px) scale(1);
  opacity: 0;
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
  .site-cursor__logo,
  .site-cursor__trail,
  .site-cursor__label {
    transition: none;
  }
}
</style>
