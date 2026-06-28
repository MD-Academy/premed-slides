<script setup lang="ts">
// Modern flat, labelled eukaryotic (animal) cell — original SVG illustration.
import { computed } from 'vue'
const props = withDefaults(defineProps<{ labels?: boolean }>(), { labels: true })
const viewBox = computed(() => (props.labels ? '0 0 680 380' : '0 0 392 380'))
</script>

<template>
  <svg :viewBox="viewBox" class="cell">
    <!-- cytoplasm / cell membrane -->
    <ellipse cx="195" cy="190" rx="180" ry="152" fill="#FBFAF6" stroke="#0B2540" stroke-width="4" />
    <ellipse cx="195" cy="190" rx="180" ry="152" fill="#E8F1F8" fill-opacity="0.5" />

    <!-- nucleus -->
    <circle cx="180" cy="175" r="66" fill="#8E5BD0" fill-opacity="0.14" stroke="#8E5BD0" stroke-width="3.5" />
    <circle cx="180" cy="175" r="58" fill="none" stroke="#8E5BD0" stroke-width="1.6" opacity="0.6" />
    <circle cx="196" cy="188" r="22" fill="#8E5BD0" fill-opacity="0.45" />

    <!-- rough ER (around nucleus) -->
    <g fill="none" stroke="#1E6FB8" stroke-width="2.6" opacity="0.85">
      <path d="M150 250 q40 -14 78 2" />
      <path d="M150 264 q44 -14 86 4" />
    </g>
    <g fill="#D9A23B"><circle cx="160" cy="248" r="2.4"/><circle cx="190" cy="250" r="2.4"/><circle cx="220" cy="256" r="2.4"/></g>

    <!-- mitochondria -->
    <g>
      <ellipse cx="100" cy="120" rx="40" ry="20" fill="#E0556B" fill-opacity="0.14" stroke="#E0556B" stroke-width="3"/>
      <path d="M66 120 q9 -14 18 0 q9 14 18 0 q9 -14 18 0" fill="none" stroke="#E0556B" stroke-width="2"/>
      <ellipse cx="250" cy="270" rx="36" ry="18" fill="#E0556B" fill-opacity="0.14" stroke="#E0556B" stroke-width="3"/>
      <path d="M220 270 q8 -12 16 0 q8 12 16 0 q8 -12 16 0" fill="none" stroke="#E0556B" stroke-width="2"/>
    </g>

    <!-- golgi -->
    <g fill="#14B8A6" fill-opacity="0.16" stroke="#14B8A6" stroke-width="2.6">
      <path d="M250 110 q34 -14 68 0 q-34 9 -68 0 z"/>
      <path d="M256 124 q30 -12 60 0 q-30 9 -60 0 z"/>
      <path d="M262 138 q24 -10 48 0 q-24 8 -48 0 z"/>
    </g>

    <!-- lysosome -->
    <circle cx="120" cy="250" r="18" fill="#2BA8E0" fill-opacity="0.18" stroke="#2BA8E0" stroke-width="3"/>
    <g fill="#2BA8E0" fill-opacity="0.6"><circle cx="114" cy="246" r="2.6"/><circle cx="126" cy="252" r="2.6"/><circle cx="118" cy="256" r="2.6"/></g>

    <!-- free ribosomes -->
    <g fill="#D9A23B"><circle cx="150" cy="110" r="3"/><circle cx="220" cy="150" r="3"/><circle cx="150" cy="300" r="3"/><circle cx="300" cy="220" r="3"/></g>

    <!-- labels + leader lines -->
    <g v-if="labels" class="lead" stroke="#9FB3C4" stroke-width="1.4" fill="none">
      <path d="M360 60 H470" /><path d="M246 175 L470 92" />
      <path d="M212 196 L470 124" /><path d="M236 258 L470 156" />
      <path d="M300 220 L470 188" /><path d="M140 120 L470 220" />
      <path d="M318 120 L470 252" /><path d="M138 250 L470 284" />
      <path d="M320 300 L470 316" />
    </g>
    <g v-if="labels" class="lbl" fill="#1A2B3C">
      <text x="474" y="64">Cell membrane</text>
      <text x="474" y="96">Nucleus</text>
      <text x="474" y="128">Nucleolus</text>
      <text x="474" y="160">Rough ER</text>
      <text x="474" y="192">Ribosomes</text>
      <text x="474" y="224">Mitochondria</text>
      <text x="474" y="256">Golgi apparatus</text>
      <text x="474" y="288">Lysosome</text>
      <text x="474" y="320">Cytoplasm</text>
    </g>
  </svg>
</template>

<style scoped>
.cell { width: 100%; height: auto; }
.lbl text { font: 600 13px 'Lexend', sans-serif; }
</style>
