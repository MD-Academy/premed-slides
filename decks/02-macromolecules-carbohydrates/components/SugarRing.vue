<script setup lang="ts">
// Clean Haworth-style pyranose ring (hexose). Optional anomer shows the C1
// hydroxyl pointing down (alpha) or up (beta). Fully original SVG.
withDefaults(defineProps<{
  color?: string
  label?: string
  anomer?: 'alpha' | 'beta' | 'none'
  showCarbons?: boolean
}>(), { color: '#1E6FB8', label: '', anomer: 'none', showCarbons: false })
</script>

<template>
  <div class="ring-wrap">
    <svg viewBox="0 0 220 180" class="ring">
      <!-- ring body (Haworth: thicker front edge) -->
      <polygon points="55,70 110,55 165,70 165,110 110,125 55,110"
        :fill="color" fill-opacity="0.10" :stroke="color" stroke-width="2.5" stroke-linejoin="round" />
      <!-- bold front edge -->
      <polyline points="55,110 110,125 165,110" fill="none" :stroke="color" stroke-width="5" stroke-linecap="round" />
      <!-- ring oxygen -->
      <circle cx="110" cy="55" r="13" fill="#fff" :stroke="color" stroke-width="2.5" />
      <text x="110" y="60" class="atom" :fill="color">O</text>
      <!-- CH2OH off C5 (top-left) -->
      <line x1="55" y1="70" x2="40" y2="44" :stroke="color" stroke-width="2.5" />
      <text x="34" y="38" class="grp" :fill="color">CH₂OH</text>
      <!-- C1 anomeric carbon (right) -->
      <template v-if="anomer === 'alpha'">
        <line x1="165" y1="110" x2="180" y2="138" stroke="#C0392B" stroke-width="2.5" />
        <text x="184" y="150" class="oh" fill="#C0392B">OH</text>
      </template>
      <template v-else-if="anomer === 'beta'">
        <line x1="165" y1="70" x2="180" y2="44" stroke="#0E8A57" stroke-width="2.5" />
        <text x="184" y="40" class="oh" fill="#0E8A57">OH</text>
      </template>
      <!-- a couple of schematic OH groups for realism -->
      <line x1="110" y1="125" x2="110" y2="150" :stroke="color" stroke-width="2" opacity=".6" />
      <text x="110" y="164" class="oh" :fill="color" opacity=".7">OH</text>
      <line x1="55" y1="110" x2="36" y2="126" :stroke="color" stroke-width="2" opacity=".6" />
      <text x="22" y="138" class="oh" :fill="color" opacity=".7">OH</text>
      <!-- carbon numbers -->
      <template v-if="showCarbons">
        <text x="168" y="66" class="cn" :fill="color">1</text>
        <text x="168" y="124" class="cn" :fill="color">2</text>
        <text x="110" y="140" class="cn" :fill="color">3</text>
        <text x="46" y="124" class="cn" :fill="color">4</text>
        <text x="44" y="66" class="cn" :fill="color">5</text>
      </template>
    </svg>
    <div v-if="label" class="ring-label">{{ label }}</div>
  </div>
</template>

<style scoped>
.ring-wrap { display: inline-flex; flex-direction: column; align-items: center; }
.ring { width: 150px; height: 122px; }
.atom { font: 700 14px 'Lexend', sans-serif; text-anchor: middle; }
.grp { font: 600 11px 'Inter', sans-serif; }
.oh { font: 600 11px 'Inter', sans-serif; text-anchor: middle; }
.cn { font: 700 9px 'Lexend', sans-serif; text-anchor: middle; }
.ring-label { font: 600 13px 'Lexend', sans-serif; color: var(--mda-navy); margin-top: 2px; }
</style>
