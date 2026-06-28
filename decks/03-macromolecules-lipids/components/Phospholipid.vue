<script setup lang="ts">
// Phospholipid: polar phosphate "head" + 2 hydrophobic fatty-acid "tails".
// mode="single" shows one molecule with labels; mode="bilayer" shows the membrane.
withDefaults(defineProps<{ mode?: 'single' | 'bilayer' }>(), { mode: 'single' })
const cols = Array.from({ length: 12 }, (_, i) => 24 + i * 26)
</script>

<template>
  <svg v-if="mode === 'single'" viewBox="0 0 200 220" class="pl">
    <!-- head -->
    <circle cx="100" cy="40" r="26" fill="#E8F1F8" stroke="#2BA8E0" stroke-width="3" />
    <text x="100" y="38" class="lbl" fill="#1E6FB8">PO₄</text>
    <text x="100" y="52" class="sub" fill="#5B6B7B">head</text>
    <!-- two tails -->
    <polyline points="88,64 84,90 90,116 84,142 90,168 84,190" fill="none" stroke="#D9A23B" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round" />
    <polyline points="112,64 116,90 110,116 116,142 110,168 116,190" fill="none" stroke="#D9A23B" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round" />
    <text x="100" y="210" class="sub" fill="#5B6B7B">2 hydrophobic tails</text>
  </svg>

  <svg v-else viewBox="0 0 340 170" class="pl-bi">
    <!-- top layer: heads up, tails down -->
    <g v-for="(x, i) in cols" :key="'t'+i">
      <circle :cx="x" cy="26" r="9" fill="#E8F1F8" stroke="#2BA8E0" stroke-width="2" />
      <line :x1="x-3" y1="35" :x2="x-3" y2="75" stroke="#D9A23B" stroke-width="2.4" />
      <line :x1="x+3" y1="35" :x2="x+3" y2="75" stroke="#D9A23B" stroke-width="2.4" />
    </g>
    <!-- bottom layer: heads down, tails up -->
    <g v-for="(x, i) in cols" :key="'b'+i">
      <line :x1="x-3" y1="95" :x2="x-3" y2="135" stroke="#D9A23B" stroke-width="2.4" />
      <line :x1="x+3" y1="95" :x2="x+3" y2="135" stroke="#D9A23B" stroke-width="2.4" />
      <circle :cx="x" cy="144" r="9" fill="#E8F1F8" stroke="#2BA8E0" stroke-width="2" />
    </g>
  </svg>
</template>

<style scoped>
.pl { width: 150px; height: auto; }
.pl-bi { width: 100%; max-width: 340px; height: auto; }
.lbl { font: 700 13px 'Lexend', sans-serif; text-anchor: middle; }
.sub { font: 600 10px 'Inter', sans-serif; text-anchor: middle; }
</style>
