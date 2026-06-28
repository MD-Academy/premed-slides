<script setup lang="ts">
import { computed } from 'vue'

const props = withDefaults(defineProps<{
  height?: number
  turns?: number
  glow?: boolean
}>(), { height: 460, turns: 3, glow: false })

const W = 220
const H = computed(() => props.height)
const cx = W / 2
const amp = 66
const pad = 26
const palette = ['#E0556B', '#F2A93B', '#2BA8E0', '#16A36F', '#8E5BD0']

function strandPath(phase: number) {
  const pts: string[] = []
  const steps = 140
  for (let i = 0; i <= steps; i++) {
    const t = i / steps
    const y = pad + t * (H.value - 2 * pad)
    const x = cx + amp * Math.sin(t * Math.PI * 2 * props.turns + phase)
    pts.push(`${x.toFixed(1)},${y.toFixed(1)}`)
  }
  return 'M' + pts.join(' L')
}

const rungs = computed(() => {
  const n = props.turns * 6
  return Array.from({ length: n }, (_, i) => {
    const t = (i + 0.5) / n
    const ang = t * Math.PI * 2 * props.turns
    const y = pad + t * (H.value - 2 * pad)
    const x1 = cx + amp * Math.sin(ang)
    const x2 = cx + amp * Math.sin(ang + Math.PI)
    const front = Math.cos(ang) >= 0
    return { y, x1, x2, color: palette[i % palette.length], front }
  })
})

const strandA = computed(() => strandPath(0))
const strandB = computed(() => strandPath(Math.PI))
</script>

<template>
  <svg :viewBox="`0 0 ${W} ${H}`" :style="{ height: H + 'px' }" class="dna-helix">
    <defs>
      <linearGradient id="strandA" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stop-color="#3CB4E8" /><stop offset="100%" stop-color="#1E6FB8" />
      </linearGradient>
      <linearGradient id="strandB" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stop-color="#7FCDEB" /><stop offset="100%" stop-color="#2BA8E0" />
      </linearGradient>
      <filter v-if="glow" id="dnaGlow" x="-40%" y="-40%" width="180%" height="180%">
        <feGaussianBlur stdDeviation="3.5" result="b" />
        <feMerge><feMergeNode in="b" /><feMergeNode in="SourceGraphic" /></feMerge>
      </filter>
    </defs>
    <g :filter="glow ? 'url(#dnaGlow)' : undefined">
      <!-- backbone strands -->
      <path :d="strandB" fill="none" stroke="url(#strandB)" stroke-width="7" stroke-linecap="round" opacity="0.8" />
      <path :d="strandA" fill="none" stroke="url(#strandA)" stroke-width="7" stroke-linecap="round" />
      <!-- base-pair rungs on top, connecting the backbones -->
      <line v-for="(r, i) in rungs" :key="i"
        :x1="r.x1" :y1="r.y" :x2="r.x2" :y2="r.y"
        :stroke="r.color" stroke-width="7" stroke-linecap="round" />
    </g>
  </svg>
</template>

<style scoped>
.dna-helix { display: block; }
</style>
