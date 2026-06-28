<script setup lang="ts">
// Fatty acid schematic: carboxyl "head" + hydrocarbon "tail".
// saturated = straight zig-zag (packs tightly); unsaturated = kinked (double bond).
withDefaults(defineProps<{ saturated?: boolean; color?: string; label?: string }>(), {
  saturated: true, color: '#1E6FB8', label: '',
})
const sat = '70,70 92,58 114,70 136,58 158,70 180,58 202,70 224,58 246,70 268,58 290,70 312,58 334,70'
const unsatA = '70,70 92,58 114,70 136,58 158,70 180,58'
const unsatB = '180,58 202,44 222,32 242,22 262,15 282,11 302,9'
</script>

<template>
  <div class="fa-wrap">
    <svg viewBox="0 0 360 100" class="fa">
      <!-- carboxyl head -->
      <text x="20" y="60" class="head" fill="#C0392B">HO</text>
      <line x1="42" y1="64" x2="58" y2="70" :stroke="color" stroke-width="3" />
      <line x1="58" y1="70" x2="58" y2="48" stroke="#C0392B" stroke-width="3" />
      <line x1="62" y1="70" x2="62" y2="48" stroke="#C0392B" stroke-width="3" />
      <text x="60" y="44" class="head" fill="#C0392B">O</text>
      <!-- tail -->
      <template v-if="saturated">
        <polyline :points="sat" fill="none" :stroke="color" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round" />
      </template>
      <template v-else>
        <polyline :points="unsatA" fill="none" :stroke="color" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round" />
        <!-- double bond (kink) marked in red -->
        <line x1="180" y1="54" x2="202" y2="40" stroke="#C0392B" stroke-width="3.5" stroke-linecap="round" />
        <line x1="183" y1="61" x2="205" y2="47" stroke="#C0392B" stroke-width="3.5" stroke-linecap="round" />
        <polyline :points="unsatB" fill="none" :stroke="color" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round" />
      </template>
    </svg>
    <div v-if="label" class="fa-label">{{ label }}</div>
  </div>
</template>

<style scoped>
.fa-wrap { display: inline-flex; flex-direction: column; align-items: center; width: 100%; }
.fa { width: 100%; max-width: 340px; height: auto; }
.head { font: 700 14px 'Lexend', sans-serif; text-anchor: middle; }
.fa-label { font: 600 12px 'Lexend', sans-serif; color: var(--mda-navy); margin-top: 2px; }
</style>
