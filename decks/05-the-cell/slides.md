---
theme: default
title: 'The Cell'
info: MDA Premedical Biology — The Cell
class: cover-bg
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
fonts:
  provider: google
  sans: Inter
  serif: Lexend
  weights: '300,400,500,600,700'
---

<div class="grid grid-cols-[1fr_1fr] items-center h-full gap-6">
  <div>
    <div class="eyebrow">Biology</div>
    <h1 class="cover-title">The Cell</h1>
    <p class="mt-6 text-lg leading-relaxed max-w-md">
      The smallest structural and functional unit of life — its types, its
      organelles, and the cytoskeleton that holds it together.
    </p>
  </div>
  <div class="flex justify-center">
    <AnimalCell :labels="false" class="w-full max-w-sm" />
  </div>
</div>

<!--
The cell as the basic unit of life: homeostasis, prokaryotes vs eukaryotes,
the organelles, and the cytoskeleton.
-->

---

# Overview

<div class="grid-3 mt-8 gap-x-8 gap-y-7">
  <div class="ov-item"><div class="ov-num">01</div><div class="ov-title">The Cell</div><p>The basic unit of life &amp; homeostasis.</p></div>
  <div class="ov-item"><div class="ov-num">02</div><div class="ov-title">Types of Cells</div><p>Prokaryote vs. Eukaryote.</p></div>
  <div class="ov-item"><div class="ov-num">03</div><div class="ov-title">Eukaryotic Organelles</div><p>The cell's subunits and their functions.</p></div>
  <div class="ov-item"><div class="ov-num">04</div><div class="ov-title">The Cytoskeleton</div><p>The cell's framework &amp; "highway."</p></div>
  <div class="ov-item"><div class="ov-num">05</div><div class="ov-title">Summary</div><p>Key takeaways &amp; review.</p></div>
</div>

---

# The Cell &amp; Homeostasis

<div class="grid grid-cols-[1.1fr_0.9fr] gap-6 items-center">
  <div>
    <ul class="tight list-disc pl-5 text-sm space-y-1">
      <li>The <strong>Cell</strong> is the smallest structural &amp; functional unit of living organisms.</li>
      <li>It is capable of maintaining <strong>Homeostasis</strong> — keeping a constant internal environment regardless of external changes (pH, temperature, salt concentration).</li>
      <li>Think of the cell as a <strong>city</strong> — its job is to keep everything inside working all the time.</li>
    </ul>
  </div>
  <div class="card-soft">
    <div class="lead mb-2">Levels of organization</div>
    <div class="flex flex-wrap items-center gap-1.5 text-xs font-medium text-[var(--mda-muted)]">
      <span>Atom</span><Ic name="chevron-right" />
      <span>Molecule</span><Ic name="chevron-right" />
      <span>Macromolecule</span><Ic name="chevron-right" />
      <span class="text-[var(--mda-blue)] font-bold">Cell</span><Ic name="chevron-right" />
      <span>Tissue</span><Ic name="chevron-right" />
      <span>Organ</span><Ic name="chevron-right" />
      <span>Organ system</span><Ic name="chevron-right" />
      <span>Organism</span>
    </div>
  </div>
</div>

---

# Types of Cells

<div class="grid grid-cols-[1.05fr_0.95fr] gap-6 items-center">
  <div>
    <div class="grid-2 gap-3 mb-3">
      <div class="card"><h3 class="!text-base">1. Prokaryotic</h3><p class="text-xs mt-1">"Before nucleus" — e.g. Bacteria.</p></div>
      <div class="card"><h3 class="!text-base">2. Eukaryotic</h3><p class="text-xs mt-1">"True nucleus" — Protista, Fungi, Plants &amp; Animals.</p></div>
    </div>
    <ul class="tight list-disc pl-5 text-sm space-y-1">
      <li><strong>Unicellular</strong> (e.g. bacteria) vs. <strong>Multicellular</strong> (e.g. humans — ~10 trillion cells).</li>
      <li>Average eukaryote cell: <strong>10–100 μm</strong>; prokaryotes ~1/10 that diameter.</li>
    </ul>
    <div class="card-soft mt-3 text-xs" style="color:var(--mda-blue)">Note: all multicellular organisms are made of <strong>eukaryotic</strong> cells.</div>
  </div>
  <div class="card-soft py-3"><ProkaryoteCell /></div>
</div>

---

# Prokaryote vs. Eukaryote

<table class="mda-table mt-4 text-sm">
  <thead><tr><th>Prokaryote</th><th class="col-dna">Eukaryote</th></tr></thead>
  <tbody>
    <tr><td>Unicellular, usually smaller</td><td>Uni- or multicellular, usually larger</td></tr>
    <tr><td>No membrane-bound organelles</td><td>Membrane-bound organelles</td></tr>
    <tr><td>No nucleus — DNA in a circular molecule in the <strong>nucleoid</strong></td><td>Membrane-bound <strong>nucleus</strong>; DNA organized into <strong>chromosomes</strong></td></tr>
    <tr><td>Plasma membrane &amp; ribosomes</td><td>Plasma membrane &amp; ribosomes</td></tr>
    <tr><td>Cell wall surrounds the membrane</td><td>Cell wall in Fungi, Plants &amp; some Protista — not Animals</td></tr>
    <tr><td>Division by fission or budding</td><td>Division by mitosis or meiosis</td></tr>
  </tbody>
</table>

---

# So Far…

<div class="grid-2 gap-5 mt-3">
  <div class="card-dark">
    <h3>Recap</h3>
    <ul class="tight mt-2 list-disc pl-5">
      <li>The cell is the smallest functional unit of life.</li>
      <li>Its job is to maintain <strong>Homeostasis</strong>.</li>
      <li><strong>Prokaryotic</strong> — unicellular.</li>
      <li><strong>Eukaryotic</strong> — unicellular or multicellular.</li>
    </ul>
  </div>
  <div class="card flex flex-col justify-center">
    <div class="lead">Up next</div>
    <p class="text-sm mt-1">Taking a look inside the eukaryotic cell — the different functions within the "city": the <strong>Organelles</strong>.</p>
  </div>
</div>

---

# The Plasma Membrane

<div class="grid grid-cols-[1.05fr_0.95fr] gap-6 items-center">
  <div>
    <ul class="tight list-disc pl-5 text-sm space-y-1">
      <li>The <strong>Plasma Membrane</strong> is the border — the "city wall" — that surrounds all cells.</li>
      <li>It encloses the cell and lets its internal chemistry differ from the outside.</li>
      <li><strong>Selectively permeable</strong> — it controls what goes in and out ("picky").</li>
    </ul>
  </div>
  <div class="card-soft py-5 flex justify-center">
    <svg viewBox="0 0 300 120" class="w-full max-w-xs">
      <g fill="#2BA8E0"><circle v-for="i in 14" :key="'t'+i" :cx="14 + (i-1)*21" cy="30" r="8" /></g>
      <g stroke="#D9A23B" stroke-width="2.4"><line v-for="i in 14" :key="'tt'+i" :x1="14 + (i-1)*21" y1="38" :x2="14 + (i-1)*21" y2="62" /></g>
      <g stroke="#D9A23B" stroke-width="2.4"><line v-for="i in 14" :key="'bt'+i" :x1="14 + (i-1)*21" y1="58" :x2="14 + (i-1)*21" y2="82" /></g>
      <g fill="#2BA8E0"><circle v-for="i in 14" :key="'b'+i" :cx="14 + (i-1)*21" cy="90" r="8" /></g>
    </svg>
  </div>
</div>

---

# Eukaryotic Organelles

<div class="grid grid-cols-[1fr_1fr] gap-6 items-center">
  <div>
    <p class="text-sm"><strong>Organelles</strong> are subunits within a cell with specific functions — the city's districts. In eukaryotes they are <strong>membrane-bound</strong> and sit in the <strong>cytoplasm</strong>, suspended in the fluid <strong>cytosol</strong>.</p>
    <div class="grid-2 gap-x-5 gap-y-1 mt-3 text-sm">
      <ul class="tight list-decimal pl-5"><li>Nucleus</li><li>Ribosomes</li><li>Endoplasmic Reticulum</li><li>Golgi Apparatus</li></ul>
      <ul class="tight list-decimal pl-5" start="5"><li>Lysosomes</li><li>Mitochondria</li><li>Chloroplasts <span class="text-xs">(plants)</span></li><li>Cell Wall <span class="text-xs">(not animals)</span></li></ul>
    </div>
  </div>
  <div class="flex justify-center"><AnimalCell class="w-full max-w-md" /></div>
</div>

---

# Nucleus

<div class="grid grid-cols-[0.8fr_1.2fr] gap-6 items-center">
  <div class="card-soft py-3 flex justify-center"><Organelle type="nucleus" /></div>
  <div>
    <p class="text-sm">The <strong>"Control Center"</strong> — contains the genetic material (DNA) organized into <strong>chromosomes</strong>. Surrounded by a highly selective <strong>double membrane</strong>.</p>
    <ul class="tight list-disc pl-5 text-sm mt-2 space-y-1">
      <li><strong>Nuclear pores</strong> — channels regulating passage between nucleus &amp; cytoplasm.</li>
      <li><strong>Nucleolus</strong> — darker area; site of rRNA synthesis.</li>
    </ul>
    <div class="card mt-3"><div class="lead">Functions</div><p class="text-sm mt-1">Protects DNA · DNA synthesis (replication) · all RNA synthesis.</p></div>
  </div>
</div>

---

# Ribosomes

<div class="grid grid-cols-[1.2fr_0.8fr] gap-6 items-center">
  <div>
    <p class="text-sm">The <strong>"Protein Factories"</strong> — take orders from the nucleus and produce proteins. Made of a <strong>large &amp; small subunit</strong> of rRNA + proteins.</p>
    <div class="grid-2 gap-3 mt-3">
      <div class="card"><h3 class="!text-base">Free</h3><p class="text-xs mt-1">Floating in the cytoplasm.</p></div>
      <div class="card"><h3 class="!text-base">Bound</h3><p class="text-xs mt-1">Attached to the rough ER.</p></div>
    </div>
    <p class="text-xs mt-3 text-[var(--mda-muted)]"><strong>Function:</strong> protein synthesis. Note: ribosomes are <em>not</em> true organelles (not membrane-bound). Eukaryote size 60S + 40S; prokaryote 50S + 30S.</p>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="ribosome" /></div>
</div>

---

# Endoplasmic Reticulum (ER)

<div class="grid grid-cols-[1.15fr_0.85fr] gap-6 items-center">
  <div>
    <p class="text-sm">A series of membrane-bound sacs continuous with the nuclear membrane; the internal space is the <strong>ER lumen</strong>.</p>
    <div class="grid gap-3 mt-3">
      <div class="card"><h3 class="!text-base">Rough ER (rER)</h3><p class="text-xs mt-1">Has bound <strong>ribosomes</strong>; site of <strong>protein synthesis</strong> &amp; sugar addition. Proteins are aimed for the membrane or export.</p></div>
      <div class="card"><h3 class="!text-base">Smooth ER (sER)</h3><p class="text-xs mt-1">No ribosomes. <strong>Lipid synthesis</strong>, <strong>detoxification</strong> (liver), and <strong>Ca²⁺ storage</strong>.</p></div>
    </div>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="er" /></div>
</div>

---

# Golgi Apparatus

<div class="grid grid-cols-[1.15fr_0.85fr] gap-6 items-center">
  <div>
    <p class="text-sm">The <strong>"Shipping Center"</strong> — a stack of membrane sacs called <strong>cisternae</strong>. Receives proteins from the rough ER and repackages them for delivery.</p>
    <div class="grid-3 gap-2 mt-3 text-xs">
      <div class="card-soft"><strong>Cis</strong><p class="mt-1">Receives vesicles from the ER.</p></div>
      <div class="card-soft"><strong>Medial</strong><p class="mt-1">Middle region.</p></div>
      <div class="card-soft"><strong>Trans</strong><p class="mt-1">Packages &amp; ships vesicles out.</p></div>
    </div>
    <p class="text-xs mt-3 text-[var(--mda-muted)]"><strong>Function:</strong> modifies, packages &amp; sorts proteins. All rER proteins continue to the Golgi.</p>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="golgi" /></div>
</div>

---

# Vesicles

<p class="-mt-2 mb-3 text-sm">Small sacs enclosed by a phospholipid membrane, with different contents and functions.</p>

<div class="grid grid-cols-[1.3fr_0.7fr] gap-6 items-center">
  <div class="grid gap-3">
    <div class="card"><h3 class="!text-base">Lysosomes</h3><p class="text-xs mt-1">The "digestive system" — contain digestive enzymes at acidic pH (~5) to break down molecules. The <strong>proteasome</strong> degrades proteins marked for destruction.</p></div>
    <div class="card"><h3 class="!text-base">Vesicle</h3><p class="text-xs mt-1">Transports molecules — e.g. from the Golgi toward the cell membrane.</p></div>
    <div class="card"><h3 class="!text-base">Peroxisome</h3><p class="text-xs mt-1">Contains hydrogen peroxide for metabolic functions; helps destroy bacteria.</p></div>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="vesicle" /></div>
</div>

---

# Mitochondria

<div class="grid grid-cols-[1.15fr_0.85fr] gap-6 items-center">
  <div>
    <p class="text-sm">The <strong>"Power Plants"</strong> — convert energy from food into usable cell energy (<strong>ATP</strong>). They grow &amp; reproduce on their own, have their own circular DNA, and contain prokaryote-like ribosomes.</p>
    <div class="grid-2 gap-2 mt-3 text-xs">
      <div class="card-soft"><strong>Outer membrane</strong><p class="mt-1">Permeable.</p></div>
      <div class="card-soft"><strong>Inner membrane</strong><p class="mt-1">Folded into <strong>cristae</strong> — more surface area.</p></div>
      <div class="card-soft"><strong>Intermembrane space</strong><p class="mt-1">Between the membranes.</p></div>
      <div class="card-soft"><strong>Matrix</strong><p class="mt-1">Space within the inner membrane.</p></div>
    </div>
    <p class="text-xs mt-3 text-[var(--mda-muted)]"><strong>Functions:</strong> aerobic respiration (glucose → ATP) &amp; apoptosis (programmed cell death via Cytochrome C).</p>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="mitochondrion" /></div>
</div>

---

# Chloroplasts &amp; Cell Wall

<div class="grid grid-cols-[1.1fr_0.9fr] gap-6 items-center">
  <div class="grid gap-3">
    <div class="card"><h3 class="!text-base">Chloroplasts</h3><p class="text-xs mt-1">"Solar Power Plants" — found only in photosynthetic organisms (plants); contain <strong>chlorophyll</strong>. Generate energy from water, CO₂ &amp; sunlight. Like mitochondria, they have their own DNA.</p></div>
    <div class="card"><h3 class="!text-base">Cell Wall</h3><p class="text-xs mt-1">A fairly rigid structure surrounding the plasma membrane — found in Protista, Fungi &amp; Plants. Provides extra structural support &amp; protection.</p></div>
    <div class="card-soft text-xs" style="color:var(--mda-blue)">Note: plant-cell structure is revisited in <strong>Botany &amp; Photosynthesis</strong>.</div>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="chloroplast" /></div>
</div>

---

<div class="eyebrow">Recap</div>

# Organelles at a Glance

<div class="grid-4 gap-3 mt-2 text-sm">
  <div class="card"><h3 class="!text-base">Nucleus</h3><p class="text-xs mt-1">Control center; DNA &amp; RNA synthesis.</p></div>
  <div class="card"><h3 class="!text-base">Ribosomes</h3><p class="text-xs mt-1">Factories; translate mRNA to protein.</p></div>
  <div class="card"><h3 class="!text-base">ER</h3><p class="text-xs mt-1">Rough = protein; smooth = lipid, detox, Ca²⁺.</p></div>
  <div class="card"><h3 class="!text-base">Golgi</h3><p class="text-xs mt-1">Shipping center; transports proteins.</p></div>
  <div class="card"><h3 class="!text-base">Lysosomes</h3><p class="text-xs mt-1">Break down ingested materials.</p></div>
  <div class="card"><h3 class="!text-base">Mitochondria</h3><p class="text-xs mt-1">Power plants; produce ATP.</p></div>
  <div class="card"><h3 class="!text-base">Chloroplasts</h3><p class="text-xs mt-1">Light + H₂O + CO₂ → energy.</p></div>
  <div class="card"><h3 class="!text-base">Cell Wall</h3><p class="text-xs mt-1">Extra protection &amp; rigidity.</p></div>
</div>

<p class="text-xs mt-3 text-[var(--mda-muted)]">Remember: not all cells have the same organelles — <strong>form follows function</strong>. Next up: the Cytoskeleton — the cell "highway."</p>

---

# Cytoskeleton

<div class="grid grid-cols-[1fr_1.2fr] gap-6 items-center">
  <div>
    <p class="text-sm">The cell <strong>"highway" &amp; support system</strong> — a complex network of protein fibers that determine the cell's shape, strength &amp; ability to move.</p>
    <p class="text-sm mt-2 font-semibold text-[var(--mda-navy)]">3 components:</p>
    <ul class="tight list-disc pl-5 text-sm"><li>Microtubules</li><li>Intermediate filaments</li><li>Microfilaments</li></ul>
  </div>
  <div class="grid grid-3 gap-3">
    <div class="card-soft py-3 text-center"><Organelle type="microtubule" /><div class="text-xs font-semibold mt-1">Microtubule</div></div>
    <div class="card-soft py-3 text-center"><Organelle type="intermediate" /><div class="text-xs font-semibold mt-1">Intermediate</div></div>
    <div class="card-soft py-3 text-center"><Organelle type="microfilament" /><div class="text-xs font-semibold mt-1">Microfilament</div></div>
  </div>
</div>

---

# Microtubules

<div class="grid grid-cols-[1.15fr_0.85fr] gap-6 items-center">
  <div>
    <ul class="tight list-disc pl-5 text-sm space-y-1">
      <li>The <strong>thickest</strong> filaments (25 nm) — a hollow tube.</li>
      <li>Made of proteins <strong>α-tubulin &amp; β-tubulin</strong> (forming a dimer).</li>
      <li>Can elongate &amp; disassemble by adding/removing tubulin dimers.</li>
    </ul>
    <div class="card mt-3"><div class="lead">Functions</div>
      <ol class="tight list-decimal pl-5 text-sm mt-1">
        <li>Intracellular transport.</li>
        <li>Structural basis of <strong>cilia</strong> &amp; <strong>flagella</strong>.</li>
        <li>Form the <strong>mitotic spindle</strong> (moves chromosomes in mitosis).</li>
      </ol>
    </div>
  </div>
  <div class="card-soft py-4 flex justify-center"><Organelle type="microtubule" /></div>
</div>

---

# Intermediate Filaments &amp; Microfilaments

<div class="grid-2 gap-6">
  <div class="card">
    <div class="flex justify-center mb-2"><Organelle type="intermediate" /></div>
    <h3>Intermediate Filaments</h3>
    <p class="text-sm mt-1">Medium thickness (10–12 nm); found where there is mechanical stress; prevent excessive stretching. Many proteins qualify — e.g. <strong>Keratin</strong>.</p>
    <p class="text-xs mt-1 text-[var(--mda-muted)]">Functions: structural rigidity &amp; stability; intercellular communication.</p>
  </div>
  <div class="card">
    <div class="flex justify-center mb-2"><Organelle type="microfilament" /></div>
    <h3>Microfilaments</h3>
    <p class="text-sm mt-1">The <strong>thinnest</strong> (7 nm) — two intertwined chains of <strong>Actin</strong>.</p>
    <p class="text-xs mt-1 text-[var(--mda-muted)]">Functions: determine cell shape &amp; support; muscle contraction; form the ring that divides the cytoplasm in mitosis.</p>
  </div>
</div>

---

<div class="eyebrow">Summary</div>

# The Cell at a Glance

<div class="grid-2 gap-4 mt-3">
  <div class="card"><h3>The Cell</h3><p class="text-sm mt-1">The smallest functional unit of life; maintains <strong>homeostasis</strong>.</p></div>
  <div class="card"><h3>Prokaryote vs. Eukaryote</h3><p class="text-sm mt-1">Prokaryotes have no nucleus or membrane-bound organelles; eukaryotes have both.</p></div>
  <div class="card"><h3>Eukaryotic Organelles</h3><p class="text-sm mt-1">Membrane-bound subunits — <strong>form follows function</strong>.</p></div>
  <div class="card"><h3>Cytoskeleton</h3><p class="text-sm mt-1">Highway &amp; structural support: microtubules, intermediate filaments, microfilaments.</p></div>
</div>

---

# Review Questions

<div class="grid-2 gap-x-6 gap-y-2.5 mt-3 text-sm">
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">1</div><p>Name some differences between prokaryote &amp; eukaryote cells.</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">2</div><p>Organelles are found in the ____ floating in a fluid called ____.</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">3</div><p>Where does rRNA synthesis occur?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">4</div><p>Which organelle handles protein synthesis, and where for proteins used by the cell?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">5</div><p>What is the Trans face of the Golgi responsible for?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">6</div><p>Which organelle has the lowest (most acidic) pH?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">7</div><p>A bacterium is most similar to which eukaryotic organelle?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">8</div><p>Sperm cells need more energy — they'd have more of which organelle?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">9</div><p>Which organelle is found only in plant cells?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">10</div><p>Name 2 organelles with a double membrane. And the 3 cytoskeleton components (small → large).</p></div>
</div>

---
layout: default
class: cover-bg
title: Thank You
---

<div class="grid grid-cols-[1.1fr_0.9fr] items-center h-full gap-6">
  <div>
    <h1 class="cover-title">Thank You</h1>
    <p class="mt-4 text-[var(--mda-blue)] font-medium tracking-wide">The Cell · Homeostasis · Organelles · Cytoskeleton</p>
    <p class="mt-5 text-lg max-w-md">The cell is life's basic unit — understanding its parts is the foundation for
    everything that follows in biology.</p>
  </div>
  <div class="flex justify-center"><AnimalCell :labels="false" class="w-full max-w-xs" /></div>
</div>
