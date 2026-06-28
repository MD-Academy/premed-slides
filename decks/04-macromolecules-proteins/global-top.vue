<script setup lang="ts">
import { ref, computed } from 'vue'

const nav = $slidev.nav
const open = ref(false)
const current = computed(() => nav.currentPage.value)

const toc = [
  'Macromolecules: Proteins',
  'Course Overview',
  'What Are Macromolecules?',
  'The 4 Types of Macromolecules',
  'Protein Structure: The Basics',
  'The Four Levels of Structure',
  'Structure: Visual Summary',
  'Protein Function',
  'Amino Acids: Building Blocks',
  'R-Group Classifications',
  'Practice: Identify the Amino Acid',
  'Review Questions',
  'More Review Questions',
  'Summary',
]

function go(n: number) {
  nav.go(n)
  open.value = false
}
</script>

<template>
  <div class="slidenav">
    <button class="slidenav-toggle" :class="{ open }" @click="open = !open"
      :title="open ? 'Hide menu' : 'Show slide menu'">
      <svg viewBox="0 0 24 24" width="20" height="20">
        <path fill="currentColor" d="M8.59 16.58L13.17 12L8.59 7.41L10 6l6 6l-6 6z" />
      </svg>
    </button>

    <transition name="slide">
      <nav v-if="open" class="slidenav-panel">
        <div class="slidenav-head">Slides</div>
        <ul>
          <li v-for="(t, i) in toc" :key="i"
            :class="{ active: current === i + 1 }" @click="go(i + 1)">
            <span class="n">{{ i + 1 }}</span><span class="t">{{ t }}</span>
          </li>
        </ul>
      </nav>
    </transition>
  </div>
</template>

<style scoped>
.slidenav { position: fixed; top: 0; right: 0; z-index: 200; }

.slidenav-toggle {
  position: fixed; top: 12px; right: 12px;
  width: 34px; height: 34px; border-radius: 9px;
  display: flex; align-items: center; justify-content: center;
  background: rgba(11, 37, 64, 0.85); color: #fff; border: none;
  cursor: pointer; backdrop-filter: blur(4px);
  box-shadow: 0 4px 14px -4px rgba(0,0,0,.4); transition: transform .2s, background .2s;
}
.slidenav-toggle:hover { background: #0B2540; }
.slidenav-toggle.open { transform: rotate(180deg); }

.slidenav-panel {
  position: fixed; top: 0; right: 0; height: 100%;
  width: 270px; padding: 56px 12px 16px;
  background: linear-gradient(180deg, #0B2540, #123A5E);
  color: #DCE9F4; overflow-y: auto;
  box-shadow: -10px 0 30px -12px rgba(0,0,0,.5);
}
.slidenav-head {
  font: 600 .7rem 'Lexend', sans-serif; letter-spacing: .14em;
  text-transform: uppercase; color: #7DD3F0; padding: 0 8px 8px;
}
.slidenav-panel ul { list-style: none; margin: 0; padding: 0; }
.slidenav-panel li {
  display: flex; align-items: center; gap: 10px;
  padding: 8px 10px; border-radius: 8px; cursor: pointer;
  font-size: .82rem; line-height: 1.2; transition: background .15s;
}
.slidenav-panel li:hover { background: rgba(125, 211, 240, .12); }
.slidenav-panel li.active { background: rgba(43, 168, 224, .25); color: #fff; }
.slidenav-panel li .n {
  flex: none; width: 22px; text-align: center;
  font: 600 .72rem 'Lexend', sans-serif; color: #7DD3F0;
}
.slidenav-panel li.active .n { color: #fff; }

.slide-enter-active, .slide-leave-active { transition: transform .25s ease; }
.slide-enter-from, .slide-leave-to { transform: translateX(100%); }

@media print { .slidenav { display: none !important; } }
</style>
