<script setup lang="ts">
// Polysaccharide schematic: a chain of glucose units (small hexagons) linked by
// glycosidic O-bridges. `variant` = straight (starch/cellulose) or branched (glycogen).
import { computed } from 'vue'
const props = withDefaults(defineProps<{
  variant?: 'straight' | 'branched'
  color?: string
}>(), { variant: 'straight', color: '#1E6FB8' })

function hex(cx: number, cy: number, r = 13) {
  const pts: string[] = []
  for (let i = 0; i < 6; i++) {
    const a = Math.PI / 6 + i * Math.PI / 3
    pts.push(`${(cx + r * Math.cos(a)).toFixed(1)},${(cy + r * Math.sin(a)).toFixed(1)}`)
  }
  return pts.join(' ')
}
const units = computed(() => [40, 95, 150, 205, 260, 315])
const branch = computed(() => props.variant === 'branched')
</script>

<template>
  <svg viewBox="0 0 360 110" class="chain">
    <!-- main chain links -->
    <g v-for="(x, i) in units" :key="i">
      <line v-if="i < units.length - 1" :x1="x + 13" y1="60" :x2="x + 42" y2="60"
        :stroke="color" stroke-width="2.5" />
      <polygon :points="hex(x, 60)" :fill="color" fill-opacity="0.16" :stroke="color" stroke-width="2.5" />
    </g>
    <!-- branch off the 3rd unit -->
    <template v-if="branch">
      <line :x1="150" y1="47" :x2="150" y2="22" :stroke="color" stroke-width="2.5" />
      <polygon :points="hex(150, 18, 11)" :fill="color" fill-opacity="0.16" :stroke="color" stroke-width="2.5" />
      <line :x1="260" y1="47" :x2="260" y2="22" :stroke="color" stroke-width="2.5" />
      <polygon :points="hex(260, 18, 11)" :fill="color" fill-opacity="0.16" :stroke="color" stroke-width="2.5" />
    </template>
  </svg>
</template>

<style scoped>
.chain { width: 100%; max-width: 360px; height: auto; }
</style>
