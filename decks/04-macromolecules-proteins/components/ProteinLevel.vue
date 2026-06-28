<script setup lang="ts">
// The four levels of protein structure as clean schematic SVGs.
// level: 1 primary · 2 secondary · 3 tertiary · 4 quaternary
import { computed } from 'vue'
const props = withDefaults(defineProps<{ level?: 1 | 2 | 3 | 4; color?: string }>(), {
  level: 1, color: '#1E6FB8',
})
// alpha-helix coil path
const helix = computed(() => {
  const pts: string[] = []
  for (let i = 0; i <= 60; i++) {
    const t = i / 60
    const x = 20 + t * 120
    const y = 50 + 26 * Math.sin(t * Math.PI * 6)
    pts.push(`${x.toFixed(1)},${y.toFixed(1)}`)
  }
  return 'M' + pts.join(' L')
})
</script>

<template>
  <svg viewBox="0 0 160 100" class="lvl">
    <!-- Primary: bead chain -->
    <template v-if="level === 1">
      <line x1="16" y1="50" x2="144" y2="50" :stroke="color" stroke-width="2.5" />
      <circle v-for="(x, i) in [16,38,60,82,104,126,144]" :key="i" :cx="x" cy="50" r="9"
        :fill="color" fill-opacity="0.85" />
    </template>

    <!-- Secondary: alpha helix -->
    <template v-else-if="level === 2">
      <path :d="helix" fill="none" :stroke="color" stroke-width="6" stroke-linecap="round" />
    </template>

    <!-- Tertiary: folded globular blob -->
    <template v-else-if="level === 3">
      <path d="M40 50 q-15 -28 18 -30 q30 -2 26 22 q-2 22 22 18 q26 -4 16 24 q-10 26 -36 14 q-26 -12 -40 6 q-16 16 -22 -10 q-6 -28 22 -36 z"
        :fill="color" fill-opacity="0.18" :stroke="color" stroke-width="3" stroke-linejoin="round" />
      <path :d="helix" fill="none" :stroke="color" stroke-width="3" stroke-linecap="round" opacity="0.7"
        transform="translate(20 6) scale(0.7)" />
    </template>

    <!-- Quaternary: multiple subunits -->
    <template v-else>
      <g v-for="(p, i) in [[52,40],[108,40],[52,66],[108,66]]" :key="i">
        <path d="M0 0 q-10 -16 11 -17 q18 -1 15 13 q-1 13 13 11 q15 -2 9 14 q-6 15 -21 8 q-15 -7 -23 4 q-9 9 -12 -6 q-3 -16 13 -21 z"
          :transform="`translate(${p[0]-22} ${p[1]-14}) scale(0.62)`"
          :fill="i % 2 ? '#14B8A6' : color" fill-opacity="0.22"
          :stroke="i % 2 ? '#14B8A6' : color" stroke-width="3.5" stroke-linejoin="round" />
      </g>
    </template>
  </svg>
</template>

<style scoped>
.lvl { width: 100%; max-width: 160px; height: auto; }
</style>
