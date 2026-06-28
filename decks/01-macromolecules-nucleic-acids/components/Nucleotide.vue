<script setup lang="ts">
// Schematic nucleotide: phosphate (circle) – sugar (pentagon) – base (hexagon)
</script>

<template>
  <svg viewBox="0 0 460 220" class="nucleotide">
    <!-- bonds -->
    <line x1="92" y1="110" x2="158" y2="110" stroke="#9FB3C4" stroke-width="3" />
    <line x1="250" y1="100" x2="312" y2="80" stroke="#9FB3C4" stroke-width="3" />

    <!-- Phosphate -->
    <circle cx="60" cy="110" r="34" fill="#FDE4E1" stroke="#E0556B" stroke-width="2.5" />
    <text x="60" y="116" text-anchor="middle" class="lbl-in" fill="#C0392B">P</text>
    <text x="60" y="172" text-anchor="middle" class="cap" fill="#5B6B7B">Phosphate</text>
    <text x="92" y="100" text-anchor="middle" class="prime" fill="#1E6FB8">5′</text>

    <!-- Sugar pentagon -->
    <polygon points="204,72 248,100 232,150 176,150 160,100"
      fill="#FFF3D6" stroke="#D9A23B" stroke-width="2.5" stroke-linejoin="round" />
    <text x="204" y="118" text-anchor="middle" class="lbl-in" fill="#9A7D0A">Sugar</text>
    <text x="204" y="178" text-anchor="middle" class="cap" fill="#5B6B7B">5-Carbon Sugar</text>
    <text x="232" y="160" text-anchor="middle" class="prime" fill="#1E6FB8">3′</text>
    <text x="166" y="92" text-anchor="middle" class="prime" fill="#1E6FB8">1′</text>

    <!-- Base hexagon -->
    <polygon points="360,48 404,48 426,86 404,124 360,124 338,86"
      fill="#E8F1F8" stroke="#2BA8E0" stroke-width="2.5" stroke-linejoin="round" />
    <text x="382" y="92" text-anchor="middle" class="lbl-in" fill="#1E6FB8">Base</text>
    <text x="382" y="146" text-anchor="middle" class="cap" fill="#5B6B7B">Nitrogenous Base</text>
  </svg>
</template>

<style scoped>
.nucleotide { width: 100%; max-width: 460px; }
.lbl-in { font: 700 16px 'Lexend', sans-serif; }
.cap { font: 600 12px 'Inter', sans-serif; }
.prime { font: 700 11px 'Lexend', sans-serif; }
</style>
