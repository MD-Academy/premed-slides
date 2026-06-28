---
theme: default
title: 'Cell Membrane Transportation'
info: MDA Premedical Biology — Cell Membrane Transportation
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

<div class="grid grid-cols-[1.05fr_0.95fr] items-center h-full gap-6">
  <div>
    <div class="eyebrow">Biology</div>
    <h1 class="cover-title">Cell Membrane<br>Transportation</h1>
    <p class="mt-6 text-lg leading-relaxed max-w-md">
      How the selectively permeable membrane moves substances in and out —
      passive &amp; active transport, carrier proteins, vesicles, and cell junctions.
    </p>
  </div>
  <div class="card-soft flex justify-center py-6">
    <Membrane type="active" />
  </div>
</div>

<!--
Membrane transport: the mechanisms that move solutes across the selectively
permeable membrane, plus how cells connect through junctions.
-->

---

# Overview

<div class="grid-3 mt-8 gap-x-8 gap-y-7">
  <div class="ov-item"><div class="ov-num">01</div><div class="ov-title">Membrane Transport</div><p>Selective permeability &amp; transport types.</p></div>
  <div class="ov-item"><div class="ov-num">02</div><div class="ov-title">Passive Transport</div><p>Diffusion &amp; facilitated diffusion.</p></div>
  <div class="ov-item"><div class="ov-num">03</div><div class="ov-title">Active Transport</div><p>Primary &amp; secondary (ATP-driven).</p></div>
  <div class="ov-item"><div class="ov-num">04</div><div class="ov-title">Carrier Proteins</div><p>Uniport, symport &amp; antiport.</p></div>
  <div class="ov-item"><div class="ov-num">05</div><div class="ov-title">Exo- &amp; Endocytosis</div><p>Vesicle-based transport.</p></div>
  <div class="ov-item"><div class="ov-num">06</div><div class="ov-title">Intercellular Junctions</div><p>How cells connect &amp; communicate.</p></div>
</div>

---

# Membrane Transport

<div class="grid grid-cols-[1.1fr_0.9fr] gap-6 items-center">
  <div>
    <p class="text-sm"><strong>Membrane transport</strong> is the collection of mechanisms that regulate
    the passage of solutes — ions &amp; small molecules — through the cell membrane.</p>
    <div class="card-soft mt-3 text-sm">The membrane is <strong>selectively permeable</strong>
    (semi-permeable) — permeable to certain substances but not others.</div>
    <div class="grid-2 gap-3 mt-3">
      <div class="card"><h3 class="!text-base">Passive</h3><p class="text-xs mt-1">Diffusion &amp; facilitated diffusion — <strong>no energy</strong>.</p></div>
      <div class="card"><h3 class="!text-base">Active</h3><p class="text-xs mt-1">Primary &amp; secondary — <strong>requires ATP</strong>.</p></div>
    </div>
  </div>
  <div class="card-soft flex justify-center py-4"><Membrane type="passive" /></div>
</div>

---

# Passive Transport

<div class="grid grid-cols-[1.1fr_0.9fr] gap-6 items-center">
  <div>
    <p class="text-sm"><strong>Passive transport</strong> moves substances across the membrane with
    <strong>no energy</strong> required.</p>
    <div class="grid gap-3 mt-3">
      <div class="card"><h3 class="!text-base">Diffusion</h3><p class="text-xs mt-1">Passage of <strong>small, non-polar</strong> (lipid-soluble) molecules <strong>down the concentration gradient</strong> — high → low. E.g. O₂ &amp; CO₂ exchange in lung alveoli.</p></div>
      <div class="card"><h3 class="!text-base">Facilitated Diffusion</h3><p class="text-xs mt-1">Large, polar, or charged molecules cross via <strong>carrier/channel proteins</strong>, avoiding the hydrophobic core.</p></div>
    </div>
  </div>
  <div class="card-soft flex justify-center py-4"><Membrane type="passive" /></div>
</div>

---

# Active Transport

<div class="grid grid-cols-[1.1fr_0.9fr] gap-6 items-center">
  <div>
    <p class="text-sm"><strong>Active transport</strong> moves molecules <strong>against</strong> their
    concentration gradient — this <strong>requires energy (ATP)</strong>.</p>
    <div class="grid gap-3 mt-3">
      <div class="card"><h3 class="!text-base">Primary</h3><p class="text-xs mt-1">Membrane proteins pump molecules using ATP <strong>directly</strong>. E.g. the <strong>Sodium–Potassium pump</strong> (Na⁺/K⁺).</p></div>
      <div class="card"><h3 class="!text-base">Secondary</h3><p class="text-xs mt-1">Uses ATP <strong>indirectly</strong> — the gradient set up by the primary pump drives it. E.g. <strong>Na⁺–glucose</strong> transport.</p></div>
    </div>
    <div class="card-soft mt-3 text-xs" style="color:var(--mda-blue)">The Na⁺/K⁺ pump moves <strong>3 Na⁺ out</strong> for <strong>2 K⁺ in</strong> — making Na⁺ the main extracellular and K⁺ the main intracellular cation.</div>
  </div>
  <div class="card-soft flex justify-center py-4"><Membrane type="active" /></div>
</div>

---

# Carrier Proteins

<div class="grid grid-cols-[1fr_1fr] gap-6 items-center">
  <div>
    <p class="text-sm"><strong>Carrier proteins</strong> are integral membrane proteins that move molecules
    across the membrane — used in passive <em>or</em> active transport. Classified by the number and
    direction of molecules moved.</p>
    <div class="grid gap-2 mt-3 text-sm">
      <div class="card"><h3 class="!text-base">Uniport</h3><p class="text-xs mt-1">1 molecule, one direction. E.g. Ca²⁺ entry in muscle contraction.</p></div>
      <div class="card"><h3 class="!text-base">Symport</h3><p class="text-xs mt-1">2 molecules, <strong>same</strong> direction. E.g. glucose + Na⁺ into the cell.</p></div>
      <div class="card"><h3 class="!text-base">Antiport</h3><p class="text-xs mt-1">2 molecules, <strong>opposite</strong> directions. E.g. the Na⁺/K⁺ pump.</p></div>
    </div>
  </div>
  <div class="card-soft flex justify-center py-4"><Membrane type="carriers" /></div>
</div>

---

# Exocytosis &amp; Endocytosis

<div class="grid grid-cols-[1.05fr_0.95fr] gap-6 items-center">
  <div>
    <p class="text-sm">Both require <strong>energy (ATP)</strong> but use <strong>vesicles</strong> instead of carrier proteins.</p>
    <div class="grid gap-3 mt-3">
      <div class="card"><h3 class="!text-base">Exocytosis</h3><p class="text-xs mt-1">The cell <strong>releases</strong> materials outward — vesicles fuse with the membrane and discharge their contents.</p></div>
      <div class="card"><h3 class="!text-base">Endocytosis</h3><p class="text-xs mt-1">The cell <strong>takes in</strong> materials by engulfing them into vesicles:</p>
        <ul class="tight list-disc pl-5 text-xs mt-1">
          <li><strong>Phagocytosis</strong> — large solids (e.g. bacteria)</li>
          <li><strong>Pinocytosis</strong> — fluids ("cell drinking")</li>
          <li><strong>Receptor-mediated</strong> — specific molecules bind receptors (e.g. LDL)</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="card-soft flex justify-center py-4"><Membrane type="exo-endo" /></div>
</div>

---

# Intercellular Junctions

<p class="-mt-2 mb-3 text-sm">Cells in close contact form <strong>cell junctions</strong> — multi-protein
complexes that connect cells, enable communication, and control passage of materials. They are vital to
tissue function and integrity.</p>

<div class="grid-3 gap-4 text-sm">
  <div class="card"><h3 class="!text-base">Anchoring Junctions</h3><p class="text-xs mt-1">Made of <strong>cadherin</strong> proteins; strong bonds that don't affect passage.</p>
    <ul class="tight list-disc pl-5 text-xs mt-1"><li><strong>Desmosomes</strong> — anchored by intermediate filaments</li><li><strong>Adherens</strong> — cement cells to the cytoskeleton</li></ul>
  </div>
  <div class="card"><h3 class="!text-base">Tight Junctions</h3><p class="text-xs mt-1">Made of <strong>occludin</strong>; seal membranes of adjacent cells &amp; act as a barrier. E.g. the <strong>blood–brain barrier</strong> &amp; intestinal epithelium.</p></div>
  <div class="card"><h3 class="!text-base">Gap Junctions</h3><p class="text-xs mt-1">Made of <strong>connexin</strong> (6 form a channel); allow substances &amp; rapid signals to pass. E.g. synchronizing <strong>cardiac muscle</strong> contraction.</p></div>
</div>

---

# Junctions — Between Cells

<div class="flex justify-center mt-2">
  <Junctions variant="between-cells" class="max-w-2xl" />
</div>

<p class="text-center text-sm text-[var(--mda-muted)] mt-2">Adjacent epithelial cells held together by
<strong style="color:#C0392B">tight junctions</strong> (apex),
<strong style="color:#8E5BD0">desmosomes</strong> (anchoring), and
<strong style="color:#16A36F">gap junctions</strong> (communication).</p>

---

# Junctions — Compared

<div class="flex justify-center mt-2">
  <Junctions variant="panels" class="max-w-3xl" />
</div>

<div class="grid-3 gap-4 mt-3 text-xs">
  <div class="card-soft"><strong style="color:#C0392B">Tight</strong> — impermeable seal; blocks passage through the intercellular space.</div>
  <div class="card-soft"><strong style="color:#8E5BD0">Anchoring</strong> — "velcro" that binds cells &amp; forms a tension-resisting network.</div>
  <div class="card-soft"><strong style="color:#16A36F">Gap</strong> — channels (connexons) let ions &amp; small molecules pass for communication.</div>
</div>

---

<div class="eyebrow">Summary</div>

# Transport at a Glance

<div class="grid-2 gap-4 mt-3">
  <div class="card"><h3>Membrane Transport</h3><p class="text-sm mt-1">Regulates passage of solutes through the <strong>selectively permeable</strong> membrane.</p></div>
  <div class="card"><h3>Passive (no energy)</h3><p class="text-sm mt-1"><strong>Diffusion</strong> — small/non-polar down the gradient; <strong>facilitated diffusion</strong> — via proteins.</p></div>
  <div class="card"><h3>Active (ATP)</h3><p class="text-sm mt-1"><strong>Primary</strong> (direct, Na⁺/K⁺ pump) &amp; <strong>secondary</strong> (indirect, Na⁺–glucose).</p></div>
  <div class="card"><h3>Carrier Proteins</h3><p class="text-sm mt-1"><strong>Uniport</strong> (1, one way), <strong>symport</strong> (2, same way), <strong>antiport</strong> (2, opposite ways).</p></div>
</div>

---

<div class="eyebrow">Summary</div>

# Vesicles &amp; Junctions

<div class="grid-2 gap-4 mt-3">
  <div class="card"><h3>Exocytosis</h3><p class="text-sm mt-1">ATP-driven release of materials outward via vesicles fusing with the membrane.</p></div>
  <div class="card"><h3>Endocytosis</h3><p class="text-sm mt-1">ATP-driven uptake via vesicles — <strong>phagocytosis</strong>, <strong>pinocytosis</strong> &amp; <strong>receptor-mediated</strong>.</p></div>
  <div class="card"><h3>Cell Junctions</h3><p class="text-sm mt-1">Multi-protein complexes connecting cells: <strong>anchoring</strong> (cadherin), <strong>tight</strong> (occludin), <strong>gap</strong> (connexin).</p></div>
  <div class="card"><h3>Why It Matters</h3><p class="text-sm mt-1">Junctions maintain tissue integrity, barriers (BBB), and rapid signaling (cardiac muscle).</p></div>
</div>

---

# Review Questions

<div class="grid-2 gap-x-6 gap-y-2.5 mt-3 text-sm">
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">1</div><p>Name the 2 types of membrane transport.</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">2</div><p>What is passive transport?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">3</div><p>Difference between diffusion &amp; facilitated diffusion?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">4</div><p>What is active transport?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">5</div><p>Difference between primary &amp; secondary active transport?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">6</div><p>Describe the mechanism of the Sodium–Potassium pump.</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">7</div><p>What are carrier proteins?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">8</div><p>Difference between uniport &amp; antiport?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">9</div><p>What are exocytosis &amp; endocytosis?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] font-bold">10</div><p>Difference between phagocytosis &amp; pinocytosis? Name the 3 types of cell junctions.</p></div>
</div>

---
layout: default
class: cover-bg
title: Thank You
---

<div class="grid grid-cols-[1.1fr_0.9fr] items-center h-full gap-6">
  <div>
    <h1 class="cover-title">Thank You</h1>
    <p class="mt-4 text-[var(--mda-blue)] font-medium tracking-wide">Membrane Transport · Carrier Proteins · Vesicles · Junctions</p>
    <p class="mt-5 text-lg max-w-md">The selectively permeable membrane is the gatekeeper of the cell —
    controlling what enters, what leaves, and how cells connect.</p>
  </div>
  <div class="card-soft flex justify-center py-6"><Membrane type="carriers" /></div>
</div>
