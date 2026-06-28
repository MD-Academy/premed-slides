<script setup lang="ts">
// Aldehyde (terminal C=O, R-C-H) vs Ketone (internal C=O, R-C-R). Original SVG.
withDefaults(defineProps<{ type?: 'aldehyde' | 'ketone'; color?: string }>(), {
  type: 'aldehyde', color: '#1E6FB8',
})
</script>

<template>
  <svg viewBox="0 0 200 150" class="carbonyl">
    <!-- carbonyl oxygen (double bond up) -->
    <text x="100" y="34" class="atom" fill="#C0392B">O</text>
    <line x1="96" y1="44" x2="96" y2="78" :stroke="color" stroke-width="2.5" />
    <line x1="104" y1="44" x2="104" y2="78" :stroke="color" stroke-width="2.5" />
    <!-- central carbon -->
    <text x="100" y="100" class="atom" :fill="color">C</text>
    <!-- left R group -->
    <line x1="88" y1="96" x2="52" y2="114" :stroke="color" stroke-width="2.5" />
    <text x="38" y="124" class="grp" :fill="color">R</text>
    <!-- right group: H for aldehyde, R for ketone -->
    <line x1="112" y1="96" x2="148" y2="114" :stroke="color" stroke-width="2.5" />
    <text x="152" y="124" class="grp" :fill="type === 'aldehyde' ? '#C0392B' : color">
      {{ type === 'aldehyde' ? 'H' : 'R' }}
    </text>
  </svg>
</template>

<style scoped>
.carbonyl { width: 150px; height: 112px; }
.atom { font: 700 22px 'Lexend', sans-serif; text-anchor: middle; }
.grp { font: 700 18px 'Lexend', sans-serif; text-anchor: middle; }
</style>
