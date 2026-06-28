<script setup lang="ts">
// Intercellular junctions — original schematic SVG.
// variant 'between-cells' = two adjacent cells with all three junctions.
// variant 'panels'       = side-by-side tight / anchoring / gap detail.
withDefaults(defineProps<{ variant?: 'between-cells' | 'panels' }>(), { variant: 'between-cells' })
</script>

<template>
  <!-- TWO ADJACENT CELLS -->
  <svg v-if="variant === 'between-cells'" viewBox="0 0 420 260" class="jx">
    <rect x="40" y="24" width="150" height="212" rx="20" fill="#E8F1F8" stroke="#1E6FB8" stroke-width="3"/>
    <rect x="230" y="24" width="150" height="212" rx="20" fill="#E8F1F8" stroke="#1E6FB8" stroke-width="3"/>

    <!-- tight junction (apex) -->
    <path d="M190 50 q20 8 40 0" fill="none" stroke="#E0556B" stroke-width="3"/>
    <path d="M190 58 q20 8 40 0" fill="none" stroke="#E0556B" stroke-width="3"/>
    <text x="210" y="40" class="cap" fill="#C0392B">Tight junction</text>

    <!-- desmosome (anchoring, middle) -->
    <rect x="196" y="118" width="10" height="28" rx="3" fill="#8E5BD0"/>
    <rect x="214" y="118" width="10" height="28" rx="3" fill="#8E5BD0"/>
    <g stroke="#8E5BD0" stroke-width="1.6">
      <line x1="196" y1="132" x2="170" y2="118"/><line x1="196" y1="132" x2="170" y2="146"/>
      <line x1="224" y1="132" x2="250" y2="118"/><line x1="224" y1="132" x2="250" y2="146"/>
    </g>
    <text x="210" y="166" class="cap" fill="#8E5BD0">Desmosome</text>

    <!-- gap junction (lower) -->
    <g fill="#16A36F">
      <rect x="196" y="196" width="10" height="9" rx="2"/><rect x="214" y="196" width="10" height="9" rx="2"/>
      <rect x="196" y="208" width="10" height="9" rx="2"/><rect x="214" y="208" width="10" height="9" rx="2"/>
    </g>
    <text x="210" y="232" class="cap" fill="#16A36F">Gap junction</text>
  </svg>

  <!-- THREE DETAIL PANELS -->
  <svg v-else viewBox="0 0 460 200" class="jx">
    <g v-for="(p, i) in [{x:10,t:'Tight Junction',c:'#E0556B'},{x:160,t:'Anchoring (Desmosome)',c:'#8E5BD0'},{x:310,t:'Gap Junction',c:'#16A36F'}]" :key="i">
      <rect :x="p.x" y="20" width="140" height="150" rx="14" fill="#F2F7FB" stroke="#E4EAF0" stroke-width="1.5"/>
      <text :x="p.x+70" y="44" class="ttl" :fill="p.c">{{ p.t }}</text>
      <!-- two membranes -->
      <line :x1="p.x+52" y1="60" :x2="p.x+52" y2="160" stroke="#2BA8E0" stroke-width="3"/>
      <line :x1="p.x+88" y1="60" :x2="p.x+88" y2="160" stroke="#2BA8E0" stroke-width="3"/>
    </g>
    <!-- tight: stitches -->
    <g stroke="#E0556B" stroke-width="2.2">
      <line v-for="y in [78,98,118,138]" :key="y" :x1="62" :y1="y" :x2="98" :y2="y"/>
    </g>
    <!-- desmosome: plaques + filaments -->
    <rect x="206" y="86" width="8" height="48" rx="2" fill="#8E5BD0"/>
    <rect x="246" y="86" width="8" height="48" rx="2" fill="#8E5BD0"/>
    <g stroke="#8E5BD0" stroke-width="1.5">
      <line x1="206" y1="110" x2="182" y2="92"/><line x1="206" y1="110" x2="182" y2="128"/>
      <line x1="254" y1="110" x2="278" y2="92"/><line x1="254" y1="110" x2="278" y2="128"/>
    </g>
    <!-- gap: connexons -->
    <g fill="#16A36F">
      <rect v-for="y in [80,104,128]" :key="'l'+y" x="354" :y="y" width="8" height="14" rx="2"/>
      <rect v-for="y in [80,104,128]" :key="'r'+y" x="398" :y="y" width="8" height="14" rx="2"/>
    </g>
  </svg>
</template>

<style scoped>
.jx { width: 100%; height: auto; }
.cap { font: 600 11px 'Inter', sans-serif; text-anchor: middle; }
.ttl { font: 700 11px 'Lexend', sans-serif; text-anchor: middle; }
</style>
