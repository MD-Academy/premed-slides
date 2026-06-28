---
theme: default
title: 'Macromolecules: Proteins'
info: MDA Premedical Biology — Macromolecules & Proteins
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
    <h1 class="cover-title">Macromolecules:<br>Proteins</h1>
    <p class="mt-6 text-lg leading-relaxed max-w-md">
      Protein structure, function, and the amino acids that build them —
      the molecular machinery behind every living cell.
    </p>
  </div>
  <div class="flex justify-center">
    <div class="card-soft w-full max-w-xs py-6 flex justify-center">
      <AminoAcid />
    </div>
  </div>
</div>

<!--
Proteins: from the amino acid and peptide bond up through the four levels of
structure, their many functions, and how R-groups classify the 20 amino acids.
-->

---

# Course Overview

<div class="grid-2 mt-8 gap-x-10 gap-y-7">
  <div class="ov-item">
    <div class="ov-num">01</div>
    <div class="ov-title">The 4 Macromolecules</div>
    <p>Carbohydrates, Proteins, Lipids, and Nucleic Acids.</p>
  </div>
  <div class="ov-item">
    <div class="ov-num">02</div>
    <div class="ov-title">Protein Structure &amp; Levels</div>
    <p>Primary, Secondary, Tertiary, and Quaternary.</p>
  </div>
  <div class="ov-item">
    <div class="ov-num">03</div>
    <div class="ov-title">Protein Function</div>
    <p>Enzymes, hormones, transport, structural roles, and more.</p>
  </div>
  <div class="ov-item">
    <div class="ov-num">04</div>
    <div class="ov-title">Amino Acids</div>
    <p>The building blocks of proteins — structure and classification.</p>
  </div>
</div>

---

# What Are Macromolecules?

<p class="max-w-4xl -mt-2">
  <strong>Organisms</strong> have <strong>Organs</strong> built from <strong>Tissues</strong>, composed of
  <strong>Cells</strong>, which are made from <strong>Macromolecules</strong> — large molecules involved in
  all structures and processes of cells and organisms. They are <strong>polymers</strong> built by adding
  or removing <strong>monomers</strong> through <strong>Condensation</strong> (removal of H₂O) or
  <strong>Hydrolysis</strong> (addition of H₂O) reactions.
</p>

<div class="grid-4 mt-5">
  <div class="card-soft">
    <div class="chip-icon mb-2"><Ic name="bread-slice" /></div>
    <h3>Carbohydrates</h3>
    <p class="text-sm">Monomer: <strong>Monosaccharide</strong></p>
  </div>
  <div class="card-soft" style="outline:2px solid var(--mda-cyan)">
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

# The 4 Types of Macromolecules

<table class="mda-table mt-6">
  <thead>
    <tr><th>Macromolecule</th><th>Monomer</th><th>Polymers</th></tr>
  </thead>
  <tbody>
    <tr><td>Carbohydrates</td><td>Monosaccharide</td><td>Starch, Glycogen, Cellulose</td></tr>
    <tr><td>Proteins</td><td>Amino Acid</td><td>Polypeptides, Proteins</td></tr>
    <tr><td>Lipids</td><td>Fatty Acid / Glycerol</td><td>Triglycerides, Phospholipids, Cholesterol</td></tr>
    <tr><td>Nucleic Acids</td><td>Nucleotide</td><td>DNA, RNA</td></tr>
  </tbody>
</table>

<div class="card-soft mt-5 text-sm max-w-4xl">
  Each class is built from a specific <strong>monomer</strong>. Proteins are polymers of
  <strong>amino acids</strong> — and the genetic code holds the recipe for every protein.
</div>

---

# Protein Structure: The Basics

<div class="grid grid-cols-[1fr_1.05fr] gap-6 items-center">
  <div class="card-dark">
    <h3>Building Blocks</h3>
    <p class="mt-2"><strong>Amino Acids</strong> are the monomers of proteins. Proteins are
    <strong>Polypeptides</strong> — long chains of amino acids linked by <strong>Peptide Bonds</strong>.</p>
    <p class="mt-2">A <strong>Dipeptide</strong> is two amino acids bonded together. Peptide bonds form
    through <strong>Condensation</strong> (loss of H₂O), joining the carboxyl carbon of one amino acid to
    the amino nitrogen of another.</p>
  </div>
  <div class="card-soft flex justify-center py-5"><PeptideBond /></div>
</div>

---

# The Four Levels of Protein Structure

<div class="grid-4 gap-4 mt-3">
  <div class="card text-center">
    <ProteinLevel :level="1" color="#1E6FB8" />
    <h3 class="!text-base mt-1">Primary</h3>
    <p class="text-xs mt-1">Polypeptide chain; a sequence of amino acids bonded by <strong>Peptide Bonds</strong>.</p>
  </div>
  <div class="card text-center">
    <ProteinLevel :level="2" color="#14B8A6" />
    <h3 class="!text-base mt-1">Secondary</h3>
    <p class="text-xs mt-1"><strong>α-helix</strong> or <strong>β-pleated sheet</strong>, formed through hydrogen bonds.</p>
  </div>
  <div class="card text-center">
    <ProteinLevel :level="3" color="#E0556B" />
    <h3 class="!text-base mt-1">Tertiary</h3>
    <p class="text-xs mt-1">Complete 3-D shape; Van der Waals, hydrophobic, ionic &amp; disulfide bridges. E.g. <strong>Myoglobin</strong>.</p>
  </div>
  <div class="card text-center">
    <ProteinLevel :level="4" color="#1E6FB8" />
    <h3 class="!text-base mt-1">Quaternary</h3>
    <p class="text-xs mt-1">Multiple polypeptide chains together. E.g. <strong>Hemoglobin</strong> — 4 chains, transports O₂.</p>
  </div>
</div>

---

# Protein Structure: Visual Summary

<div class="grid grid-cols-[1fr_1fr] gap-6 items-center">
  <div class="card-soft py-4 flex flex-col items-center gap-3">
    <div class="flex items-end gap-4">
      <div class="text-center"><ProteinLevel :level="1" color="#1E6FB8" /><div class="text-xs font-semibold mt-1">Primary</div></div>
      <div class="text-center"><ProteinLevel :level="2" color="#14B8A6" /><div class="text-xs font-semibold mt-1">Secondary</div></div>
    </div>
    <div class="flex items-end gap-4">
      <div class="text-center"><ProteinLevel :level="3" color="#E0556B" /><div class="text-xs font-semibold mt-1">Tertiary</div></div>
      <div class="text-center"><ProteinLevel :level="4" color="#1E6FB8" /><div class="text-xs font-semibold mt-1">Quaternary</div></div>
    </div>
  </div>
  <div>
    <h3 class="!text-[1.05rem]">Intramolecular Interactions</h3>
    <p class="text-sm mt-1">A chain of amino acids can interact with itself, causing the protein to
    <strong>twist and fold</strong> into a specific shape — critical to its function.</p>
    <div class="mt-3 rounded-2xl px-4 py-3 text-sm" style="background:#FFF3D6;color:#9A7D0A">
      <strong>Denaturation:</strong> high temperature or extreme pH destroys the tertiary structure. A
      denatured protein loses its shape and, most often, its function.
    </div>
    <p class="text-xs mt-2 italic text-[var(--mda-muted)]">Note: Disulfide bridges are covalent bonds between
    two sulfur atoms, formed only between <strong>Cysteine</strong> amino acids.</p>
  </div>
</div>

---

# Protein Function

<p class="-mt-2 mb-3 max-w-4xl text-sm">Proteins are involved in almost every aspect of the body — our
genetic code holds the recipe for all of them.</p>

<div class="grid-3 gap-4 text-sm">
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="factory" /></div><div><h3 class="!text-base">Enzyme</h3><p class="text-xs mt-1">Catalyzes reactions. E.g. <strong>Amylase</strong> breaks down carbohydrates.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="dna" /></div><div><h3 class="!text-base">Protection</h3><p class="text-xs mt-1">Fights infection. E.g. <strong>Antibodies</strong> target pathogens.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="message-text" /></div><div><h3 class="!text-base">Hormone</h3><p class="text-xs mt-1">Regulates metabolism. E.g. <strong>Insulin</strong> regulates blood glucose.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="oil" /></div><div><h3 class="!text-base">Transport</h3><p class="text-xs mt-1">Carries substances. E.g. <strong>Hemoglobin</strong> transports O₂.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="bread-slice" /></div><div><h3 class="!text-base">Structural</h3><p class="text-xs mt-1">Provides structure. E.g. <strong>Cell-wall</strong> proteins, collagen.</p></div></div>
  <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="content-cut" /></div><div><h3 class="!text-base">Contractile</h3><p class="text-xs mt-1">Enables movement. E.g. <strong>Myosin &amp; Actin</strong> contract muscle.</p></div></div>
</div>

---

# Amino Acids: The Building Blocks

<div class="grid grid-cols-[0.9fr_1.1fr] gap-6 items-center">
  <div class="card-soft flex justify-center py-4"><AminoAcid /></div>
  <div>
    <h3 class="!text-[1.05rem]">Amino Acid Structure</h3>
    <p class="text-sm mt-1">Each amino acid has four groups bonded to a central <strong>α-Carbon</strong>:</p>
    <ul class="tight text-sm list-disc pl-5 mt-1">
      <li><strong>Amino group</strong> (NH₃⁺)</li>
      <li><strong>Carboxyl group</strong> (COO⁻)</li>
      <li><strong>Hydrogen</strong> atom</li>
      <li><strong>R-group</strong> — the variable side chain that defines each amino acid</li>
    </ul>
    <div class="mt-3 rounded-2xl px-4 py-3 text-sm" style="background:#E8F1F8;color:#1E6FB8">
      There are <strong>20 kinds</strong> of amino acids, differing only at the R-group.
      <strong>Essential</strong> ones must come from diet; <strong>Non-essential</strong> ones are made in the body.
    </div>
  </div>
</div>

---

# R-Group Classifications

<p class="-mt-2 mb-3 max-w-4xl text-sm">Proteins are built from the same 20 amino acids, classified by
their R-group properties. Students must memorize all structures and classifications.</p>

<div class="grid-3 gap-3 text-sm">
  <div class="card"><h3 class="!text-base">Non-Polar</h3><p class="text-xs mt-1">Hydrophobic; cluster inside proteins. Glycine, Alanine, Valine, Leucine, Isoleucine, Methionine, Phenylalanine, Tryptophan, Proline.</p></div>
  <div class="card"><h3 class="!text-base">Polar</h3><p class="text-xs mt-1">Hydrophilic; interact with water. Serine, Cysteine, Tyrosine, Asparagine, Glutamine.</p></div>
  <div class="card"><h3 class="!text-base">Positive (+) Basic</h3><p class="text-xs mt-1">Positive charge at physiological pH. Lysine, Arginine, Histidine.</p></div>
  <div class="card"><h3 class="!text-base">Negative (−) Acidic</h3><p class="text-xs mt-1">Negative charge at physiological pH. Aspartic Acid, Glutamic Acid.</p></div>
  <div class="card"><h3 class="!text-base">Aromatic</h3><p class="text-xs mt-1">Contain a benzene ring; can be polar or non-polar. Phenylalanine, Tyrosine, Tryptophan.</p></div>
  <div class="card-soft flex items-center justify-center"><AminoAcid /></div>
</div>

---

# Practice: Identify the Amino Acid

<p class="-mt-2 mb-4 max-w-4xl text-sm">For each structure, identify the amino acid, classify its
R-group, and determine whether it is <strong>essential</strong> or <strong>non-essential</strong>.</p>

<div class="grid-4 gap-4">
  <div class="card text-center"><div class="ov-num text-[var(--mda-blue)] font-bold mb-1">A</div><AminoAcid /><p class="text-xs mt-1">Side chain ends in an amide (–CONH₂)</p></div>
  <div class="card text-center"><div class="ov-num text-[var(--mda-blue)] font-bold mb-1">B</div><AminoAcid /><p class="text-xs mt-1">Long chain ending in –NH₂ (basic)</p></div>
  <div class="card text-center"><div class="ov-num text-[var(--mda-blue)] font-bold mb-1">C</div><AminoAcid /><p class="text-xs mt-1">Simplest R-group: a single H</p></div>
  <div class="card text-center"><div class="ov-num text-[var(--mda-blue)] font-bold mb-1">D</div><AminoAcid /><p class="text-xs mt-1">R-group contains a benzene ring (aromatic)</p></div>
</div>

<div class="card-soft mt-4 text-sm flex items-start gap-3">
  <Ic name="translate" class="text-[var(--mda-blue)] text-xl shrink-0 mt-0.5" />
  <span>Hint: focus on the <strong>R-group</strong> only — the amino, carboxyl, and hydrogen groups are
  identical in every amino acid.</span>
</div>

---

# Review Questions

<div class="grid-2 gap-x-6 gap-y-3 mt-5 text-sm">
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">1</div><p>What are macromolecules &amp; what are the 4 major ones in the body?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">2</div><p>What are monomers &amp; what is the monomer of proteins?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">3</div><p>What are the 4 groups of an amino acid?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">4</div><p>What is the bond between amino acids? What reaction forms it?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">5</div><p>α-Helixes &amp; β-pleated sheets are characteristic of which structural level?</p></div>
</div>

---

# More Review Questions

<div class="grid-3 gap-4 mt-5 text-sm">
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">1</div><p>What are some roles of protein in the body?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">2</div><p>What happens to a protein exposed to high heat or extreme pH?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">3</div><p>The R-group of an amino acid can be classified into which 5 groups?</p></div>
</div>

<div class="card-soft mt-5 text-sm flex items-start gap-3">
  <Ic name="message-text" class="text-[var(--mda-blue)] text-xl shrink-0 mt-0.5" />
  <span>Use these questions to self-test before your exam. Refer back to each section of the
  presentation for detailed answers.</span>
</div>

---

<div class="eyebrow">Summary</div>

# Proteins at a Glance

<div class="grid-2 gap-4 mt-3">
  <div class="card"><h3>4 Macromolecules</h3><p class="text-sm mt-1">Carbohydrates, Proteins, Lipids &amp; Nucleic Acids — built from monomers.</p></div>
  <div class="card"><h3>Protein Structure</h3><p class="text-sm mt-1">Polypeptide chains bonded by peptide bonds across <strong>Primary, Secondary, Tertiary &amp; Quaternary</strong> levels.</p></div>
  <div class="card"><h3>Protein Function</h3><p class="text-sm mt-1">Enzymes, protection, hormones, transport, storage, structural &amp; contractile.</p></div>
  <div class="card"><h3>Amino Acids</h3><p class="text-sm mt-1">20 types; differ by R-group: Polar, Non-Polar, Positive, Negative &amp; Aromatic.</p></div>
</div>
