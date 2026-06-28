<script setup lang="ts">
// Modern flat, labelled prokaryotic (bacterial) cell — original SVG.
</script>

<template>
  <svg viewBox="0 0 680 320" class="cell">
    <!-- flagellum -->
    <path d="M40 160 q-20 -16 -34 -2 q14 16 34 2" fill="none" stroke="#14B8A6" stroke-width="3" />
    <!-- capsule -->
    <rect x="60" y="70" width="320" height="180" rx="90" fill="#16A36F" fill-opacity="0.10" stroke="#16A36F" stroke-width="3" stroke-dasharray="2 4" />
    <!-- cell wall -->
    <rect x="72" y="82" width="296" height="156" rx="78" fill="#16A36F" fill-opacity="0.14" stroke="#16A36F" stroke-width="3.5" />
    <!-- plasma membrane -->
    <rect x="84" y="94" width="272" height="132" rx="66" fill="#FBFAF6" stroke="#2BA8E0" stroke-width="3" />
    <!-- nucleoid (circular DNA) -->
    <path d="M170 160 q-26 -34 14 -46 q40 -10 40 24 q0 36 -38 34 q-28 -2 -16 -12"
      fill="none" stroke="#8E5BD0" stroke-width="3.5" />
    <!-- ribosomes -->
    <g fill="#D9A23B">
      <circle cx="120" cy="120" r="3.2"/><circle cx="140" cy="200" r="3.2"/><circle cx="250" cy="110" r="3.2"/>
      <circle cx="300" cy="180" r="3.2"/><circle cx="280" cy="210" r="3.2"/><circle cx="110" cy="170" r="3.2"/>
    </g>
    <!-- pili -->
    <g stroke="#16A36F" stroke-width="2" fill="none" opacity="0.8">
      <path d="M380 110 l24 -10"/><path d="M384 150 l26 0"/><path d="M380 196 l24 12"/>
    </g>

    <!-- labels -->
    <g class="lead" stroke="#9FB3C4" stroke-width="1.4" fill="none">
      <path d="M210 84 L470 60" /><path d="M236 96 L470 96" />
      <path d="M250 130 L470 132" /><path d="M300 180 L470 168" />
      <path d="M404 100 L470 204" /><path d="M10 158 L470 240" />
    </g>
    <g class="lbl" fill="#1A2B3C">
      <text x="474" y="64">Capsule &amp; cell wall</text>
      <text x="474" y="100">Plasma membrane</text>
      <text x="474" y="136">Nucleoid (DNA)</text>
      <text x="474" y="172">Ribosomes</text>
      <text x="474" y="208">Pili</text>
      <text x="474" y="244">Flagellum</text>
    </g>
  </svg>
</template>

<style scoped>
.cell { width: 100%; height: auto; }
.lbl text { font: 600 13px 'Lexend', sans-serif; }
</style>
