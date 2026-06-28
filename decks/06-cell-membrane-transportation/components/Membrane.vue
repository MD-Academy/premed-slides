<script setup lang="ts">
// Phospholipid-bilayer transport diagrams. One component, selectable by `type`.
// All original SVG: heads = cyan circles, tails = gold lines, proteins = purple.
import { computed } from 'vue'
const props = withDefaults(defineProps<{ type:
  'passive' | 'active' | 'carriers' | 'exo-endo' }>(), { type: 'passive' })
const heads = computed(() => Array.from({ length: 22 }, (_, i) => 14 + i * 15))
</script>

<template>
  <svg viewBox="0 0 340 220" class="mem">
    <!-- region labels -->
    <text x="6" y="20" class="reg">Extracellular</text>
    <text x="6" y="212" class="reg">Cytoplasm</text>

    <!-- bilayer -->
    <g>
      <g stroke="#D9A23B" stroke-width="2">
        <line v-for="x in heads" :key="'tt'+x" :x1="x" y1="100" :x2="x" y2="118" />
        <line v-for="x in heads" :key="'bt'+x" :x1="x" y1="120" :x2="x" y2="102" />
      </g>
      <g fill="#2BA8E0">
        <circle v-for="x in heads" :key="'th'+x" :cx="x" cy="96" r="6" />
        <circle v-for="x in heads" :key="'bh'+x" :cx="x" cy="124" r="6" />
      </g>
    </g>

    <!-- PASSIVE: diffusion (left) + facilitated via channel (right) -->
    <template v-if="type === 'passive'">
      <g fill="#14B8A6"><circle cx="70" cy="50" r="5"/><circle cx="78" cy="70" r="5"/><circle cx="70" cy="150" r="5"/><circle cx="84" cy="170" r="5"/></g>
      <path d="M74 58 V150" stroke="#0B2540" stroke-width="2" marker-end="url(#ar)"/>
      <text x="74" y="40" class="cap">Diffusion</text>
      <!-- channel protein -->
      <rect x="232" y="84" width="30" height="52" rx="10" fill="#8E5BD0" fill-opacity="0.7"/>
      <rect x="244" y="84" width="6" height="52" fill="#fff" fill-opacity="0.7"/>
      <g fill="#E0556B"><circle cx="247" cy="50" r="5"/><circle cx="247" cy="70" r="5"/><circle cx="247" cy="160" r="5"/></g>
      <path d="M247 58 V162" stroke="#0B2540" stroke-width="2" marker-end="url(#ar)"/>
      <text x="247" y="40" class="cap">Facilitated</text>
    </template>

    <!-- ACTIVE: Na/K pump with ATP -->
    <template v-else-if="type === 'active'">
      <rect x="150" y="80" width="44" height="60" rx="14" fill="#8E5BD0" fill-opacity="0.75"/>
      <text x="172" y="160" class="cap" fill="#C0392B">ATP → ADP + Pi</text>
      <circle cx="172" cy="150" r="6" fill="#E0556B"/>
      <!-- 3 Na out -->
      <g fill="#1E6FB8"><circle cx="120" cy="150" r="5"/><circle cx="134" cy="158" r="5"/><circle cx="120" cy="166" r="5"/></g>
      <path d="M150 150 q-20 -60 -20 -110" stroke="#1E6FB8" stroke-width="2" fill="none" marker-end="url(#ar)"/>
      <text x="96" y="44" class="cap" fill="#1E6FB8">3 Na⁺ out</text>
      <!-- 2 K in -->
      <g fill="#16A36F"><circle cx="220" cy="54" r="5"/><circle cx="234" cy="62" r="5"/></g>
      <path d="M196 60 q24 50 0 96" stroke="#16A36F" stroke-width="2" fill="none" marker-end="url(#ar)"/>
      <text x="250" y="172" class="cap" fill="#16A36F">2 K⁺ in</text>
    </template>

    <!-- CARRIERS: uniport / symport / antiport -->
    <template v-else-if="type === 'carriers'">
      <g v-for="(c, i) in [{x:60,l:'Uniport'},{x:170,l:'Symport'},{x:280,l:'Antiport'}]" :key="i">
        <rect :x="c.x-15" y="84" width="30" height="52" rx="10" fill="#8E5BD0" fill-opacity="0.7"/>
        <text :x="c.x" y="206" class="cap">{{ c.l }}</text>
      </g>
      <!-- uniport: 1 down -->
      <path d="M60 60 V160" stroke="#1E6FB8" stroke-width="2" marker-end="url(#ar)"/>
      <circle cx="60" cy="52" r="5" fill="#1E6FB8"/>
      <!-- symport: 2 down -->
      <path d="M163 60 V160" stroke="#1E6FB8" stroke-width="2" marker-end="url(#ar)"/>
      <path d="M177 60 V160" stroke="#16A36F" stroke-width="2" marker-end="url(#ar)"/>
      <circle cx="163" cy="52" r="5" fill="#1E6FB8"/><circle cx="177" cy="52" r="5" fill="#16A36F"/>
      <!-- antiport: opposite -->
      <path d="M273 60 V160" stroke="#1E6FB8" stroke-width="2" marker-end="url(#ar)"/>
      <path d="M287 160 V60" stroke="#16A36F" stroke-width="2" marker-end="url(#ar)"/>
      <circle cx="273" cy="52" r="5" fill="#1E6FB8"/><circle cx="287" cy="168" r="5" fill="#16A36F"/>
    </template>

    <!-- EXO / ENDO -->
    <template v-else-if="type === 'exo-endo'">
      <!-- endocytosis (left): membrane invaginates inward -->
      <path d="M60 96 q14 50 0 70" fill="none" stroke="#2BA8E0" stroke-width="3"/>
      <circle cx="58" cy="170" r="14" fill="#E8F1F8" stroke="#2BA8E0" stroke-width="2.5"/>
      <g fill="#14B8A6"><circle cx="58" cy="50" r="4"/><circle cx="66" cy="64" r="4"/></g>
      <path d="M60 70 V150" stroke="#0B2540" stroke-width="2" marker-end="url(#ar)"/>
      <text x="58" y="200" class="cap">Endocytosis</text>
      <!-- exocytosis (right): vesicle fuses & releases out -->
      <circle cx="282" cy="170" r="14" fill="#E8F1F8" stroke="#2BA8E0" stroke-width="2.5"/>
      <g fill="#E0556B"><circle cx="282" cy="60" r="4"/><circle cx="274" cy="48" r="4"/></g>
      <path d="M282 150 V60" stroke="#0B2540" stroke-width="2" marker-end="url(#ar)"/>
      <text x="282" y="200" class="cap">Exocytosis</text>
    </template>

    <defs>
      <marker id="ar" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto">
        <path d="M0 0 L6 3 L0 6 z" fill="#0B2540"/>
      </marker>
    </defs>
  </svg>
</template>

<style scoped>
.mem { width: 100%; max-width: 340px; height: auto; }
.reg { font: 600 10px 'Inter', sans-serif; fill: #5B6B7B; }
.cap { font: 600 10px 'Inter', sans-serif; fill: #1A2B3C; text-anchor: middle; }
</style>
