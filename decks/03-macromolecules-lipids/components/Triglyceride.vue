<script setup lang="ts">
// Triglyceride: glycerol backbone (left) + 3 fatty-acid tails via ester bonds.
</script>

<template>
  <svg viewBox="0 0 320 220" class="tag">
    <!-- glycerol backbone -->
    <rect x="26" y="40" width="34" height="140" rx="12" fill="#FDE4E1" stroke="#E0556B" stroke-width="2.5" />
    <text x="43" y="116" class="bb" fill="#C0392B" transform="rotate(-90 43 110)">Glycerol</text>

    <!-- 3 ester linkages + fatty acid tails -->
    <g v-for="(y, i) in [70, 110, 150]" :key="i">
      <!-- ester bond marker -->
      <circle :cx="70" :cy="y" r="9" fill="#FFF3D6" stroke="#D9A23B" stroke-width="2" />
      <text x="70" :y="y + 4" class="ester">e</text>
      <line :x1="79" :y1="y" :x2="96" :y2="y" stroke="#9FB3C4" stroke-width="2.5" />
      <!-- zig-zag fatty acid tail -->
      <polyline
        :points="`96,${y} 116,${y-9} 136,${y} 156,${y-9} 176,${y} 196,${y-9} 216,${y} 236,${y-9} 256,${y} 276,${y-9} 296,${y}`"
        fill="none" stroke="#1E6FB8" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" />
    </g>
    <text x="196" y="200" class="cap">3 Fatty Acids — ester bonds</text>
  </svg>
</template>

<style scoped>
.tag { width: 100%; max-width: 320px; height: auto; }
.bb { font: 700 13px 'Lexend', sans-serif; text-anchor: middle; }
.ester { font: 700 10px 'Lexend', sans-serif; fill: #9A7D0A; text-anchor: middle; }
.cap { font: 600 11px 'Inter', sans-serif; fill: #5B6B7B; text-anchor: middle; }
</style>
