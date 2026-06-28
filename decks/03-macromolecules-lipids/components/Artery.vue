<script setup lang="ts">
// Artery cross-section: healthy (open lumen) vs atherosclerotic (plaque-narrowed).
withDefaults(defineProps<{ blocked?: boolean }>(), { blocked: false })
</script>

<template>
  <svg viewBox="0 0 220 120" class="artery">
    <!-- vessel wall -->
    <rect x="6" y="20" width="208" height="80" rx="40" fill="#FBE9E7" stroke="#E0556B" stroke-width="3" />
    <!-- lumen -->
    <rect x="18" y="32" width="184" height="56" rx="28" fill="#fff" />
    <!-- plaque -->
    <template v-if="blocked">
      <path d="M18 60 Q70 18 140 44 Q175 56 184 60 Q175 64 140 76 Q70 102 18 60 Z"
        fill="#F2C14E" stroke="#D9A23B" stroke-width="2" opacity="0.95" />
      <circle v-for="(x, i) in [40,70,150,175]" :key="i" :cx="x" :cy="60" r="4.5" fill="#E0556B" />
    </template>
    <!-- flowing blood cells -->
    <template v-else>
      <circle v-for="(x, i) in [40,70,100,130,160,190]" :key="i" :cx="x" :cy="60" r="6.5" fill="#E0556B" opacity="0.85" />
      <path d="M150 60 h34 M178 54 l8 6 l-8 6" fill="none" stroke="#1E6FB8" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" />
    </template>
  </svg>
</template>

<style scoped>
.artery { width: 100%; max-width: 220px; height: auto; }
</style>
