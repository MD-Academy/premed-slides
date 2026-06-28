<script setup lang="ts">
withDefaults(defineProps<{ type?: 'purine' | 'pyrimidine'; color?: string }>(), {
  type: 'purine', color: '#E0556B',
})
</script>

<template>
  <svg viewBox="0 0 160 120" class="ring">
    <!-- Purine: fused six- + five-membered ring -->
    <template v-if="type === 'purine'">
      <polygon points="60,30 92,30 108,60 92,90 60,90 44,60"
        :fill="color" fill-opacity="0.18" :stroke="color" stroke-width="3" stroke-linejoin="round" />
      <polygon points="92,30 130,40 130,80 92,90 108,60"
        :fill="color" fill-opacity="0.30" :stroke="color" stroke-width="3" stroke-linejoin="round" />
      <text x="44" y="64" class="n">N</text>
      <text x="60" y="28" class="n">N</text>
      <text x="92" y="94" class="n">N</text>
      <text x="128" y="84" class="n">N</text>
    </template>
    <!-- Pyrimidine: single six-membered ring -->
    <template v-else>
      <polygon points="64,28 100,28 118,60 100,92 64,92 46,60"
        :fill="color" fill-opacity="0.22" :stroke="color" stroke-width="3" stroke-linejoin="round" />
      <text x="62" y="26" class="n">N</text>
      <text x="100" y="98" class="n">N</text>
    </template>
  </svg>
</template>

<style scoped>
.ring { width: 130px; height: 100px; }
.n { font: 700 13px 'Lexend', sans-serif; fill: #0B2540; text-anchor: middle; }
</style>
