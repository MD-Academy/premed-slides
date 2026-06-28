<script setup lang="ts">
// Two amino acids join by a peptide bond (condensation), releasing water.
</script>

<template>
  <svg viewBox="0 0 380 170" class="pb">
    <!-- amino acid 1 -->
    <rect x="14" y="40" width="120" height="60" rx="14" fill="#E8F1F8" stroke="#1E6FB8" stroke-width="2.5" />
    <text x="74" y="66" class="t" fill="#1E6FB8">Amino Acid 1</text>
    <text x="74" y="86" class="s" fill="#5B6B7B">—COOH</text>

    <!-- amino acid 2 -->
    <rect x="246" y="40" width="120" height="60" rx="14" fill="#E8F1F8" stroke="#1E6FB8" stroke-width="2.5" />
    <text x="306" y="66" class="t" fill="#1E6FB8">Amino Acid 2</text>
    <text x="306" y="86" class="s" fill="#5B6B7B">H₂N—</text>

    <!-- peptide bond link -->
    <line x1="134" y1="70" x2="170" y2="70" stroke="#9FB3C4" stroke-width="2.5" />
    <line x1="210" y1="70" x2="246" y2="70" stroke="#9FB3C4" stroke-width="2.5" />
    <rect x="166" y="54" width="48" height="32" rx="10" fill="#D9F2E4" stroke="#0E8A57" stroke-width="2.5" />
    <text x="190" y="74" class="t" fill="#0E8A57">C–N</text>
    <text x="190" y="30" class="cap" fill="#0E8A57">Peptide Bond</text>

    <!-- released water -->
    <path d="M190 110 q-10 14 0 22 q10 -8 0 -22 z" fill="#7DD3F0" stroke="#2BA8E0" stroke-width="1.5" />
    <text x="222" y="130" class="s" fill="#2BA8E0">+ H₂O</text>
    <text x="190" y="158" class="cap" fill="#5B6B7B">Condensation reaction</text>
  </svg>
</template>

<style scoped>
.pb { width: 100%; max-width: 380px; height: auto; }
.t { font: 700 13px 'Lexend', sans-serif; text-anchor: middle; }
.s { font: 600 11px 'Inter', sans-serif; text-anchor: middle; }
.cap { font: 600 10px 'Inter', sans-serif; text-anchor: middle; }
</style>
