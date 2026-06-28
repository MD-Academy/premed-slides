---
theme: default
title: 'Macromolecules: Nucleic Acids'
info: MDA Premedical Biology — Macromolecules & Nucleic Acids
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

<div class="grid grid-cols-[1.1fr_0.9fr] items-center h-full gap-6">
  <div>
    <div class="eyebrow">Biology</div>
    <h1 class="cover-title">Macromolecules:<br>Nucleic Acids</h1>
    <p class="mt-6 text-lg leading-relaxed max-w-md">
      An exploration of the building blocks of life — from macromolecules to the
      genetic code written in <strong>DNA</strong> and <strong>RNA</strong>.
    </p>
  </div>
  <div class="flex justify-center">
    <DnaHelix :height="440" :turns="3" glow />
  </div>
</div>

<!--
Welcome. This lesson builds from the four classes of macromolecules down to the
genetic code stored in DNA and RNA.
-->

---

# Course Overview

<div class="grid-2 mt-8 gap-x-10 gap-y-7">
  <div class="ov-item">
    <div class="ov-num">01</div>
    <div class="ov-title">Macromolecules</div>
    <p>The 4 major types and how they are built from monomers.</p>
  </div>
  <div class="ov-item">
    <div class="ov-num">02</div>
    <div class="ov-title">Nucleic Acids &amp; Building Blocks</div>
    <p>Nucleotides — the monomers of DNA and RNA.</p>
  </div>
  <div class="ov-item">
    <div class="ov-num">03</div>
    <div class="ov-title">Nitrogenous Bases</div>
    <p>Purines &amp; Pyrimidines and their roles.</p>
  </div>
  <div class="ov-item">
    <div class="ov-num">04</div>
    <div class="ov-title">DNA &amp; RNA</div>
    <p>Structure, function, and key differences.</p>
  </div>
</div>

---

# What Are Macromolecules?

<p class="max-w-4xl -mt-2">
  <strong>Macromolecules</strong> are large, biologically important molecules involved in all
  structures and processes of cells and organisms. They are <strong>polymers</strong> — many
  monomers strung together — built through <strong>Condensation</strong> (removal of H₂O) or
  <strong>Hydrolysis</strong> (addition of H₂O) reactions.
</p>

<div class="flex items-center gap-2 text-xs text-[var(--mda-muted)] my-4 font-medium">
  <span>Atom</span><Ic name="chevron-right" />
  <span>Molecule</span><Ic name="chevron-right" />
  <span>Macromolecule</span><Ic name="chevron-right" />
  <span>Cell</span><Ic name="chevron-right" />
  <span>Tissue</span><Ic name="chevron-right" />
  <span>Organ</span><Ic name="chevron-right" />
  <span>Organism</span>
</div>

<div class="grid-4 mt-3">
  <div class="card-soft">
    <div class="chip-icon mb-2"><Ic name="bread-slice" /></div>
    <h3>Carbohydrates</h3>
    <p class="text-sm">Monomer: <strong>Monosaccharide</strong></p>
  </div>
  <div class="card-soft">
    <div class="chip-icon mb-2"><Ic name="food-steak" /></div>
    <h3>Proteins</h3>
    <p class="text-sm">Monomer: <strong>Amino Acid</strong></p>
  </div>
  <div class="card-soft">
    <div class="chip-icon mb-2"><Ic name="oil" /></div>
    <h3>Lipids</h3>
    <p class="text-sm">Monomer: <strong>Fatty Acid</strong></p>
  </div>
  <div class="card-soft">
    <div class="chip-icon mb-2"><Ic name="dna" /></div>
    <h3>Nucleic Acids</h3>
    <p class="text-sm">Monomer: <strong>Nucleotide</strong></p>
  </div>
</div>

---

# Macromolecules: Polymers &amp; Monomers

<p class="-mt-2 mb-4 max-w-4xl">
  Each macromolecule class has distinct polymers and monomers. Nucleic acids form
  <strong>DNA and RNA</strong> from nucleotide monomers containing Adenine, Guanine,
  Thymine/Uracil, and Cytosine.
</p>

<div class="grid-4 text-sm">
  <div>
    <div class="text-center font-bold text-[var(--mda-navy)] mb-2 flex items-center justify-center gap-2"><Ic name="bread-slice" class="text-[var(--mda-blue)]" /> Carbohydrates</div>
    <div class="card mb-2"><div class="lead">POLYMER</div><strong>Polysaccharides</strong><p class="text-xs mt-1">Starch, Glycogen, Cellulose</p></div>
    <div class="card-soft"><div class="lead">MONOMER</div><strong>Monosaccharides</strong><p class="text-xs mt-1">Glucose, Fructose, Galactose</p></div>
  </div>
  <div>
    <div class="text-center font-bold text-[var(--mda-navy)] mb-2 flex items-center justify-center gap-2"><Ic name="food-steak" class="text-[var(--mda-blue)]" /> Proteins</div>
    <div class="card mb-2"><div class="lead">POLYMER</div><strong>Polypeptides</strong><p class="text-xs mt-1">Hemoglobin, Collagen, Enzymes</p></div>
    <div class="card-soft"><div class="lead">MONOMER</div><strong>Amino Acids</strong><p class="text-xs mt-1">Glycine, Alanine, Lysine</p></div>
  </div>
  <div>
    <div class="text-center font-bold text-[var(--mda-navy)] mb-2 flex items-center justify-center gap-2"><Ic name="oil" class="text-[var(--mda-blue)]" /> Lipids</div>
    <div class="card mb-2"><div class="lead">POLYMER</div><strong>Fats (Triglycerides)</strong><p class="text-xs mt-1">Triglycerides, Oils, Waxes</p></div>
    <div class="card-soft"><div class="lead">MONOMER</div><strong>Fatty Acids &amp; Glycerol</strong><p class="text-xs mt-1">Fatty Acids, Glycerol</p></div>
  </div>
  <div>
    <div class="text-center font-bold text-[var(--mda-navy)] mb-2 flex items-center justify-center gap-2"><Ic name="dna" class="text-[var(--mda-blue)]" /> Nucleic Acids</div>
    <div class="card mb-2"><div class="lead">POLYMER</div><strong>DNA / RNA</strong><p class="text-xs mt-1">Long chains of nucleotides</p></div>
    <div class="card-soft"><div class="lead">MONOMER</div><strong>Nucleotides</strong><p class="text-xs mt-1">A, T/U, C, G</p></div>
  </div>
</div>

---

<div class="eyebrow">Nucleic Acids</div>

# Nucleic Acids &amp; the Nucleotide

<div class="grid grid-cols-[1.05fr_0.95fr] gap-6 mt-2 items-center">
  <div>
    <div class="card-dark mb-3">
      <h3>What Are Nucleic Acids?</h3>
      <p class="mt-2"><strong>DNA</strong> (deoxyribonucleic acid) and <strong>RNA</strong> (ribonucleic acid)
      store and transmit the genetic material of all organisms. Their monomer is the
      <strong>Nucleotide</strong>; a <strong>Nucleoside</strong> = Sugar + Base (no phosphate).</p>
    </div>
    <h3 class="!text-[1.05rem] mb-1">Nucleotide Structure</h3>
    <ul class="tight text-sm list-disc pl-5">
      <li><strong>5-Carbon Sugar</strong> — ribose or deoxyribose</li>
      <li><strong>Nitrogenous Base</strong> — attached to carbon 1′</li>
      <li><strong>Phosphate Group</strong> — attached to carbon 5′</li>
    </ul>
    <p class="text-sm mt-2">Nucleotides link via <strong>Phosphodiester Bonds</strong> — phosphate
    connects the 5′ carbon of one sugar to the 3′ carbon of the next.</p>
  </div>
  <div class="card-soft flex justify-center items-center py-6">
    <Nucleotide />
  </div>
</div>

---

<div class="eyebrow">Nitrogenous Bases</div>

# Purines &amp; Pyrimidines

<p class="-mt-2">Nitrogenous bases are divided into two groups based on their ring structure.
<strong class="text-[var(--mda-blue)]">Remember: Pur As Gold &amp; CUT the Py</strong></p>

<div class="grid-2 mt-5">
  <div class="card">
    <h3>Purines — Double Ring, 4 Nitrogens</h3>
    <div class="flex items-center gap-6 mt-2">
      <div class="text-center">
        <RingStructure type="purine" color="#E0556B" />
        <div class="text-sm font-semibold">Adenine (A)</div>
      </div>
      <div class="text-center">
        <RingStructure type="purine" color="#5B7BD0" />
        <div class="text-sm font-semibold">Guanine (G)</div>
      </div>
    </div>
  </div>
  <div class="card">
    <h3>Pyrimidines — Single Ring, 2 Nitrogens</h3>
    <div class="flex items-center justify-around gap-2 mt-2">
      <div class="text-center">
        <RingStructure type="pyrimidine" color="#D9A23B" />
        <div class="text-xs font-semibold">Cytosine (C)</div>
      </div>
      <div class="text-center">
        <RingStructure type="pyrimidine" color="#E0556B" />
        <div class="text-xs font-semibold">Thymine (T)<br><span class="text-[var(--mda-muted)] font-normal">DNA only</span></div>
      </div>
      <div class="text-center">
        <RingStructure type="pyrimidine" color="#16A36F" />
        <div class="text-xs font-semibold">Uracil (U)<br><span class="text-[var(--mda-muted)] font-normal">RNA only</span></div>
      </div>
    </div>
  </div>
</div>

---

<div class="eyebrow">DNA</div>

# DNA Structure

<div class="grid grid-cols-[0.85fr_1.15fr] gap-6 items-center">
  <div class="flex justify-center">
    <DnaHelix :height="300" :turns="3" />
  </div>
  <div>
    <p class="mb-4"><strong>DNA</strong> (deoxyribonucleic acid) composes the hereditary material
    (genes) of an organism and contains instructions for making proteins and RNA.</p>
    <div class="grid grid-3 gap-3">
      <div class="card"><h3 class="!text-base">Double Helix</h3><p class="text-xs mt-1">Two strands of deoxynucleotides twisted together with a sugar-phosphate backbone; bases face inward.</p></div>
      <div class="card"><h3 class="!text-base">Hydrogen Bonds</h3><p class="text-xs mt-1"><span class="pill pill-a">A</span>=<span class="pill pill-t">T</span> (2 bonds) and <span class="pill pill-g">G</span>≡<span class="pill pill-c">C</span> (3 bonds) hold the strands together.</p></div>
      <div class="card"><h3 class="!text-base">Anti-Parallel</h3><p class="text-xs mt-1">The two strands run in opposite directions (3′→5′ and 5′→3′).</p></div>
    </div>
  </div>
</div>

---

<div class="eyebrow">RNA</div>

# RNA Structure &amp; Function

<p class="-mt-2 max-w-4xl"><strong>RNA</strong> (ribonucleic acid) carries out DNA's instructions by transferring
genetic information to the sites of protein synthesis (ribosomes) and translating it into proteins.
RNA is usually a <strong>single strand</strong> of ribonucleotides. Base pairs:
<span class="pill pill-a">A</span>=<span class="pill pill-u">U</span> (2 bonds) and <span class="pill pill-g">G</span>≡<span class="pill pill-c">C</span> (3 bonds).</p>

<div class="grid-2 mt-5 gap-4">
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="message-text" /></div><div><h3>mRNA</h3><p class="text-sm">Transports genetic information from the nucleus to the cytoplasm.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="factory" /></div><div><h3>rRNA</h3><p class="text-sm">Composes ribosomes — the site of protein synthesis.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="translate" /></div><div><h3>tRNA</h3><p class="text-sm">Translates nucleic acid "language" into amino acid "language."</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="content-cut" /></div><div><h3>snRNA</h3><p class="text-sm">Found in the nucleus; plays a role in DNA transcription and RNA splicing.</p></div></div>
</div>

---

# DNA vs. RNA: Side-by-Side

<table class="mda-table mt-6">
  <thead>
    <tr><th>Feature</th><th class="col-dna">DNA</th><th>RNA</th></tr>
  </thead>
  <tbody>
    <tr><td>Location</td><td>Nucleus</td><td>Nucleus, nucleolus, cytoplasm</td></tr>
    <tr><td>Nitrogenous Bases</td><td>A, G, T, C</td><td>A, G, U, C</td></tr>
    <tr><td>Sugar</td><td>Deoxyribose</td><td>Ribose</td></tr>
    <tr><td>Structure</td><td>Double strand</td><td>Single strand</td></tr>
  </tbody>
</table>

---

# DNA vs. RNA: Chemical Comparison

<div class="grid-2 mt-6 gap-6">
  <div class="card-dark">
    <h3>DNA — Deoxyribonucleic Acid</h3>
    <ul class="tight mt-2 list-disc pl-5">
      <li>Bases: <strong>A, T, C, G</strong></li>
      <li>Base pairs: <strong>A–T</strong> and <strong>G–C</strong></li>
      <li>Backbone sugar: <strong>Deoxyribose</strong></li>
    </ul>
  </div>
  <div class="card">
    <h3>RNA — Ribonucleic Acid</h3>
    <ul class="tight mt-2 list-disc pl-5 text-sm">
      <li>Bases: <strong>A, U, C, G</strong></li>
      <li>Base pairs: <strong>A–U</strong> and <strong>G–C</strong></li>
      <li>Backbone sugar: <strong>Ribose</strong></li>
      <li><strong>Uracil replaces Thymine</strong></li>
    </ul>
  </div>
</div>

---

<div class="eyebrow">Summary</div>

# Key Takeaways

<div class="flex gap-2 mt-1 mb-5 flex-wrap">
  <span class="pill" style="background:var(--mda-navy);color:#fff">Macromolecules</span>
  <span class="pill" style="background:var(--mda-blue);color:#fff">Nucleotide</span>
  <span class="pill" style="background:var(--mda-cyan);color:#fff">Nitrogenous Bases</span>
  <span class="pill" style="background:var(--mda-sky);color:var(--mda-navy)">DNA vs RNA</span>
</div>

<div class="grid-3 gap-4">
  <div class="card"><h3>Nucleic Acids</h3><p class="text-sm mt-1">DNA &amp; RNA store and transmit genetic information; their monomer is the <strong>nucleotide</strong> (5-carbon sugar + nitrogenous base + phosphate), linked by <strong>phosphodiester bonds</strong>.</p></div>
  <div class="card"><h3>Nitrogenous Bases</h3><p class="text-sm mt-1"><strong>Purines</strong> (Adenine, Guanine) — double ring; <strong>Pyrimidines</strong> (Cytosine, Thymine, Uracil) — single ring. Thymine = DNA only; Uracil = RNA only.</p></div>
  <div class="card"><h3>DNA &amp; RNA</h3><p class="text-sm mt-1"><strong>DNA</strong>: double-stranded helix, anti-parallel, A=T &amp; G≡C. <strong>RNA</strong>: single-stranded, A=U &amp; G≡C; types include mRNA, rRNA, tRNA, snRNA.</p></div>
</div>

---

# Review Questions

<div class="grid-2 gap-x-6 gap-y-3 mt-5 text-sm">
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">1</div><p>What are macromolecules and what are the 4 major ones in the body?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">2</div><p>What are monomers and what is the monomer of nucleic acids?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">3</div><p>What is the structure of the nucleotide?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">4</div><p>Name the nitrogenous bases — which are purines and which are pyrimidines?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">5</div><p>Describe the structure of DNA and RNA. What are their base pairs?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">6</div><p>3-Hydrogen bonds are found between which base pairs? Which nucleic acid is found in the cytoplasm?</p></div>
</div>

---
layout: default
class: cover-bg
---

<div class="grid grid-cols-[1.1fr_0.9fr] items-center h-full gap-6">
  <div>
    <h1 class="cover-title">Thank You</h1>
    <p class="mt-4 text-[var(--mda-blue)] font-medium tracking-wide">Macromolecules · Nucleic Acids · DNA · RNA</p>
    <p class="mt-5 text-lg max-w-md">Understanding nucleic acids is the foundation for understanding how life
    stores, transmits, and expresses genetic information.</p>
  </div>
  <div class="flex justify-center">
    <DnaHelix :height="430" :turns="3" glow />
  </div>
</div>
