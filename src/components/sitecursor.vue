<template>
  <div
    class="site-cursor"
    :class="{ 'is-visible': isVisible, 'is-interactive': isInteractive, 'is-clicking': isClicking }"
    :style="{ '--cursor-x': `${position.x}px`, '--cursor-y': `${position.y}px` }"
    aria-hidden="true"
  >
    <span class="site-cursor__orbit site-cursor__orbit--one"></span>
    <span class="site-cursor__orbit site-cursor__orbit--two"></span>
    <span class="site-cursor__crosshair site-cursor__crosshair--horizontal"></span>
    <span class="site-cursor__crosshair site-cursor__crosshair--vertical"></span>
    <span class="site-cursor__core"></span>
    <span
      v-for="particle in particles"
      :key="particle.id"
      class="site-cursor__particle"
      :style="{
        '--particle-x': `${particle.x}px`,
        '--particle-y': `${particle.y}px`,
        '--particle-delay': `${particle.delay}ms`,
      }"
    ></span>
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
const particles = Array.from({ length: 7 }, (_, index) => ({
  id: index,
  x: Math.cos(index * 0.9) * (18 + index * 2),
  y: Math.sin(index * 0.9) * (18 + index * 2),
  delay: index * 45,
}))

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

.site-cursor__crosshair,
.site-cursor__core,
.site-cursor__orbit,
.site-cursor__particle,
.site-cursor__label {
  position: absolute;
  display: block;
  transform: translate(-50%, -50%);
}

.site-cursor__core {
  width: 9px;
  height: 9px;
  border: 2px solid #c7d2fe;
  border-radius: 2px;
  background: #6366f1;
  box-shadow:
    0 0 9px 2px rgb(129 140 248 / 85%),
    0 0 24px rgb(99 102 241 / 40%);
  rotate: 45deg;
  transition:
    scale 180ms ease,
    rotate 180ms ease,
    background-color 180ms ease;
}

.site-cursor__crosshair {
  background: rgb(165 180 252 / 80%);
  transition:
    width 180ms ease,
    height 180ms ease,
    background-color 180ms ease;
}

.site-cursor__crosshair--horizontal {
  width: 38px;
  height: 1px;
}

.site-cursor__crosshair--vertical {
  width: 1px;
  height: 38px;
}

.site-cursor__orbit {
  width: 28px;
  height: 28px;
  border: 1px solid rgb(129 140 248 / 65%);
  border-radius: 9999px;
  border-left-color: transparent;
  border-bottom-color: transparent;
  animation: cursor-spin 2.8s linear infinite;
  transition:
    width 180ms ease,
    height 180ms ease,
    border-color 180ms ease;
}

.site-cursor__orbit--one {
  rotate: 25deg;
}

.site-cursor__orbit--two {
  width: 38px;
  height: 38px;
  rotate: 205deg;
  animation-duration: 4.2s;
  animation-direction: reverse;
  opacity: 0.6;
}

.site-cursor__particle {
  width: 3px;
  height: 3px;
  left: var(--particle-x);
  top: var(--particle-y);
  border-radius: 9999px;
  background: #818cf8;
  box-shadow: 0 0 7px 1px rgb(129 140 248 / 70%);
  opacity: 0;
  animation: particle-fade 900ms ease-in-out infinite alternate;
  animation-delay: var(--particle-delay);
}

.site-cursor__label {
  top: 27px;
  left: 25px;
  color: #c7d2fe;
  font: 700 8px/1 ui-monospace, SFMono-Regular, Menlo, monospace;
  letter-spacing: 0.12em;
  white-space: nowrap;
  opacity: 0;
  transition: opacity 180ms ease;
}

.site-cursor.is-interactive .site-cursor__orbit--one {
  width: 42px;
  height: 42px;
  border-color: #818cf8;
  animation-duration: 1.5s;
}

.site-cursor.is-interactive .site-cursor__orbit--two {
  width: 52px;
  height: 52px;
  border-color: rgb(165 180 252 / 70%);
}

.site-cursor.is-interactive .site-cursor__core {
  scale: 1.35;
  rotate: 135deg;
  background: #818cf8;
}

.site-cursor.is-interactive .site-cursor__crosshair--horizontal {
  width: 52px;
}

.site-cursor.is-interactive .site-cursor__crosshair--vertical {
  height: 52px;
}

.site-cursor.is-interactive .site-cursor__label {
  opacity: 1;
}

.site-cursor.is-clicking .site-cursor__orbit {
  width: 64px;
  height: 64px;
  border-color: #e0e7ff;
}

.site-cursor.is-clicking .site-cursor__core {
  scale: 0.8;
  rotate: 225deg;
}

@keyframes cursor-spin {
  to {
    rotate: 385deg;
  }
}

@keyframes particle-fade {
  from {
    opacity: 0.15;
    scale: 0.65;
  }
  to {
    opacity: 0.85;
    scale: 1.25;
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
  .site-cursor__core,
  .site-cursor__crosshair,
  .site-cursor__orbit,
  .site-cursor__particle,
  .site-cursor__label {
    transition: none;
    animation: none;
  }
}
</style>
