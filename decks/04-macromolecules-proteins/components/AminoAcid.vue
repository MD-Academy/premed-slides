<script setup lang="ts">
// Amino acid: central α-carbon bonded to amino group, carboxyl group,
// a hydrogen, and the variable R-group. Clean original recreation.
</script>

<template>
  <svg viewBox="0 0 280 210" class="aa">
    <!-- bonds -->
    <line x1="140" y1="92" x2="140" y2="58" stroke="#5B6B7B" stroke-width="2.5" />
    <line x1="124" y1="105" x2="78" y2="105" stroke="#5B6B7B" stroke-width="2.5" />
    <line x1="156" y1="105" x2="202" y2="105" stroke="#5B6B7B" stroke-width="2.5" />
    <line x1="140" y1="118" x2="140" y2="152" stroke="#5B6B7B" stroke-width="2.5" />

    <!-- central carbon -->
    <circle cx="140" cy="105" r="17" fill="#fff" stroke="#0B2540" stroke-width="2.5" />
    <text x="140" y="110" class="c">Cα</text>

    <!-- Hydrogen (top) -->
    <rect x="120" y="22" width="40" height="34" rx="9" fill="#FCE4EC" stroke="#E0556B" stroke-width="2" />
    <text x="140" y="44" class="grp" fill="#C0392B">H</text>

    <!-- Amino group (left) -->
    <rect x="6" y="86" width="72" height="38" rx="9" fill="#D6F0F2" stroke="#14B8A6" stroke-width="2" />
    <text x="42" y="110" class="grp" fill="#0E8A57">NH₃⁺</text>
    <text x="42" y="138" class="cap" fill="#5B6B7B">Amino</text>

    <!-- Carboxyl group (right) -->
    <rect x="202" y="86" width="72" height="38" rx="9" fill="#D9F2E4" stroke="#0E8A57" stroke-width="2" />
    <text x="238" y="110" class="grp" fill="#0E8A57">COO⁻</text>
    <text x="238" y="138" class="cap" fill="#5B6B7B">Carboxyl</text>

    <!-- R group (bottom) -->
    <rect x="116" y="152" width="48" height="40" rx="9" fill="#FFF3D6" stroke="#D9A23B" stroke-width="2" />
    <text x="140" y="178" class="grp" fill="#9A7D0A">R</text>
    <text x="140" y="205" class="cap" fill="#5B6B7B">Side chain</text>
  </svg>
</template>

<style scoped>
.aa { width: 100%; max-width: 280px; height: auto; }
.c { font: 700 13px 'Lexend', sans-serif; text-anchor: middle; }
.grp { font: 700 15px 'Lexend', sans-serif; text-anchor: middle; }
.cap { font: 600 10px 'Inter', sans-serif; text-anchor: middle; }
</style>
