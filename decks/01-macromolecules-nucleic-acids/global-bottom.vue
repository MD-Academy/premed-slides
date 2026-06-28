<script setup lang="ts">
import { computed } from 'vue'
const nav = $slidev.nav
const show = computed(() => nav.currentPage.value > 1 && nav.currentPage.value < nav.total.value)
</script>

<template>
  <div v-if="show" class="deck-footer">
    <span class="brand">MDA · Premedical Biology</span>
    <span>Macromolecules: Nucleic Acids &nbsp;·&nbsp; {{ nav.currentPage.value }} / {{ nav.total.value }}</span>
  </div>
</template>
