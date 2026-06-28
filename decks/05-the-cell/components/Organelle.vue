<script setup lang="ts">
// Clean, original schematic diagrams of eukaryotic organelles + cytoskeleton
// filaments. One component, selectable via `type`. All SVG is fully ours.
import { computed } from 'vue'
const props = withDefaults(defineProps<{ type:
  'nucleus' | 'mitochondrion' | 'er' | 'golgi' | 'ribosome' | 'vesicle' |
  'chloroplast' | 'microtubule' | 'intermediate' | 'microfilament'
}>(), { type: 'nucleus' })

// helpers
const tubeBeads = computed(() => Array.from({ length: 9 }, (_, i) => 22 + i * 18))
const grana = computed(() => [
  { x: 55, y: 70 }, { x: 95, y: 92 }, { x: 132, y: 64 },
])
function disc(n: number) { return Array.from({ length: n }, (_, i) => i) }
</script>

<template>
  <svg viewBox="0 0 200 160" class="org">
    <!-- NUCLEUS -->
    <template v-if="type === 'nucleus'">
      <circle cx="100" cy="80" r="62" fill="#8E5BD0" fill-opacity="0.10" stroke="#8E5BD0" stroke-width="3" />
      <circle cx="100" cy="80" r="55" fill="none" stroke="#8E5BD0" stroke-width="2" opacity="0.6" />
      <!-- pores -->
      <g fill="#fff" stroke="#8E5BD0" stroke-width="2">
        <circle cx="100" cy="18" r="4" /><circle cx="155" cy="50" r="4" />
        <circle cx="158" cy="108" r="4" /><circle cx="100" cy="142" r="4" />
        <circle cx="42" cy="108" r="4" /><circle cx="42" cy="50" r="4" />
      </g>
      <!-- nucleolus -->
      <circle cx="112" cy="90" r="20" fill="#8E5BD0" fill-opacity="0.45" stroke="#8E5BD0" stroke-width="2" />
      <!-- chromatin squiggles -->
      <path d="M60 70 q14 -10 26 2 t26 -2" fill="none" stroke="#8E5BD0" stroke-width="2" opacity="0.55" />
      <path d="M58 96 q12 12 26 2" fill="none" stroke="#8E5BD0" stroke-width="2" opacity="0.45" />
    </template>

    <!-- MITOCHONDRION -->
    <template v-else-if="type === 'mitochondrion'">
      <ellipse cx="100" cy="80" rx="84" ry="44" fill="#E0556B" fill-opacity="0.10" stroke="#E0556B" stroke-width="3" />
      <ellipse cx="100" cy="80" rx="74" ry="34" fill="none" stroke="#E0556B" stroke-width="2" opacity="0.7" />
      <!-- cristae folds -->
      <g fill="none" stroke="#E0556B" stroke-width="2.4" opacity="0.8">
        <path d="M40 80 q12 -22 24 0 q12 22 24 0 q12 -22 24 0 q12 22 24 0 q12 -22 24 0" />
      </g>
    </template>

    <!-- ENDOPLASMIC RETICULUM -->
    <template v-else-if="type === 'er'">
      <g fill="none" stroke="#1E6FB8" stroke-width="3" stroke-linecap="round">
        <path d="M24 44 q40 -20 80 0 t72 0" />
        <path d="M24 74 q40 -20 80 0 t72 0" />
        <path d="M24 104 q40 -20 80 0 t72 0" />
      </g>
      <!-- ribosome dots (rough ER) -->
      <g fill="#D9A23B">
        <circle cx="46" cy="40" r="3" /><circle cx="86" cy="36" r="3" /><circle cx="126" cy="40" r="3" /><circle cx="166" cy="44" r="3" />
        <circle cx="46" cy="70" r="3" /><circle cx="106" cy="64" r="3" /><circle cx="156" cy="70" r="3" />
        <circle cx="66" cy="100" r="3" /><circle cx="126" cy="98" r="3" />
      </g>
    </template>

    <!-- GOLGI APPARATUS -->
    <template v-else-if="type === 'golgi'">
      <g fill="#14B8A6" fill-opacity="0.14" stroke="#14B8A6" stroke-width="3">
        <path d="M50 44 q50 -22 100 0 q-50 12 -100 0 z" />
        <path d="M44 66 q56 -22 112 0 q-56 12 -112 0 z" />
        <path d="M50 88 q50 -22 100 0 q-50 12 -100 0 z" />
        <path d="M58 110 q42 -20 84 0 q-42 12 -84 0 z" />
      </g>
      <!-- vesicles -->
      <g fill="#14B8A6" fill-opacity="0.5">
        <circle cx="36" cy="120" r="6" /><circle cx="160" cy="124" r="7" /><circle cx="150" cy="36" r="6" />
      </g>
    </template>

    <!-- RIBOSOME -->
    <template v-else-if="type === 'ribosome'">
      <!-- large subunit -->
      <path d="M52 50 q48 -20 96 0 q14 26 0 44 q-48 16 -96 0 q-14 -22 0 -44 z"
        fill="#D9A23B" fill-opacity="0.22" stroke="#D9A23B" stroke-width="3" />
      <text x="100" y="86" class="cap" fill="#9A7D0A">Large subunit</text>
      <!-- small subunit -->
      <path d="M60 104 q40 -14 80 0 q8 16 0 26 q-40 12 -80 0 q-8 -12 0 -26 z"
        fill="#D9A23B" fill-opacity="0.35" stroke="#D9A23B" stroke-width="3" />
      <text x="100" y="126" class="cap" fill="#9A7D0A">Small subunit</text>
      <!-- mRNA -->
      <path d="M30 100 h140" stroke="#1E6FB8" stroke-width="2.5" stroke-dasharray="5 4" />
      <text x="178" y="103" class="cap" fill="#1E6FB8" text-anchor="start">mRNA</text>
    </template>

    <!-- VESICLE / LYSOSOME / PEROXISOME -->
    <template v-else-if="type === 'vesicle'">
      <circle cx="100" cy="80" r="58" fill="#2BA8E0" fill-opacity="0.10" stroke="#2BA8E0" stroke-width="3" />
      <circle cx="100" cy="80" r="50" fill="none" stroke="#2BA8E0" stroke-width="2" opacity="0.6" />
      <g fill="#2BA8E0" fill-opacity="0.55">
        <circle cx="86" cy="66" r="6" /><circle cx="116" cy="74" r="7" /><circle cx="92" cy="98" r="6" />
        <circle cx="118" cy="100" r="5" /><circle cx="100" cy="80" r="5" />
      </g>
    </template>

    <!-- CHLOROPLAST -->
    <template v-else-if="type === 'chloroplast'">
      <ellipse cx="100" cy="80" rx="86" ry="42" fill="#16A36F" fill-opacity="0.12" stroke="#16A36F" stroke-width="3" />
      <ellipse cx="100" cy="80" rx="76" ry="32" fill="none" stroke="#16A36F" stroke-width="2" opacity="0.6" />
      <!-- grana (thylakoid stacks) -->
      <g>
        <g v-for="(g, i) in grana" :key="i">
          <rect v-for="d in disc(5)" :key="d" :x="g.x - 12" :y="g.y - 18 + d * 8"
            width="24" height="6" rx="2" fill="#16A36F" fill-opacity="0.5" />
        </g>
        <!-- lamellae connecting -->
        <path d="M55 70 L95 92 M95 92 L132 64" stroke="#16A36F" stroke-width="2" opacity="0.5" />
      </g>
    </template>

    <!-- MICROTUBULE -->
    <template v-else-if="type === 'microtubule'">
      <g fill="#1E6FB8" fill-opacity="0.25" stroke="#1E6FB8" stroke-width="1.5">
        <circle v-for="x in tubeBeads" :key="'a'+x" :cx="x" cy="58" r="8" />
        <circle v-for="x in tubeBeads" :key="'b'+x" :cx="x" cy="74" r="8" />
      </g>
      <!-- cross-section ring -->
      <g fill="#1E6FB8" fill-opacity="0.4">
        <circle v-for="i in 13" :key="i" :cx="100 + 30 * Math.cos((i-1)/13*6.283)"
          :cy="120 + 22 * Math.sin((i-1)/13*6.283)" r="4.5" />
      </g>
      <text x="150" y="124" class="cap" fill="#1E6FB8" text-anchor="start">cross-section</text>
    </template>

    <!-- INTERMEDIATE FILAMENT -->
    <template v-else-if="type === 'intermediate'">
      <g fill="none" stroke="#8E5BD0" stroke-width="3" stroke-linecap="round">
        <path d="M20 80 q20 -22 40 0 t40 0 t40 0 t40 0" />
        <path d="M20 80 q20 22 40 0 t40 0 t40 0 t40 0" />
        <path d="M20 64 q20 -16 40 0 t40 0 t40 0 t40 0" opacity="0.5" />
        <path d="M20 96 q20 16 40 0 t40 0 t40 0 t40 0" opacity="0.5" />
      </g>
    </template>

    <!-- MICROFILAMENT (actin) -->
    <template v-else-if="type === 'microfilament'">
      <g fill="#16A36F" fill-opacity="0.5">
        <circle v-for="i in 11" :key="'x'+i" :cx="18 + (i-1)*17" :cy="70 + 14 * Math.sin((i-1)*0.9)" r="7" />
        <circle v-for="i in 11" :key="'y'+i" :cx="18 + (i-1)*17" :cy="90 - 14 * Math.sin((i-1)*0.9)" r="7" />
      </g>
    </template>
  </svg>
</template>

<style scoped>
.org { width: 100%; max-width: 200px; height: auto; }
.cap { font: 600 9px 'Inter', sans-serif; text-anchor: middle; }
</style>
