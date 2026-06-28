---
theme: default
title: 'Macromolecules: Lipids'
info: MDA Premedical Biology — Macromolecules & Lipids
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
    <h1 class="cover-title">Macromolecules:<br>Lipids</h1>
    <p class="mt-6 text-lg leading-relaxed max-w-md">
      A deep dive into the structure, function, and medical significance of lipids —
      one of the four essential macromolecules of life.
    </p>
  </div>
  <div class="flex justify-center">
    <div class="card-soft w-full max-w-sm py-6">
      <Triglyceride />
    </div>
  </div>
</div>

<!--
Lipids: fatty acids, the omega naming system, the three key lipids, and why
saturated vs unsaturated fats matter clinically.
-->

---

# What Are Macromolecules?

<div class="grid grid-cols-[1.1fr_0.9fr] gap-8 items-center">
  <div>
    <p class="-mt-2"><strong>Macromolecules</strong> are large, biologically important molecules
    involved in all structures and processes of cells and organisms. They are <strong>polymers</strong>
    — many monomers strung together — built through <strong>Condensation</strong> (removal of H₂O) or
    <strong>Hydrolysis</strong> (addition of H₂O).</p>
    <div class="flex items-center gap-2 text-xs text-[var(--mda-muted)] my-4 font-medium">
      <span>Atom</span><Ic name="chevron-right" />
      <span>Molecule</span><Ic name="chevron-right" />
      <span>Cell</span><Ic name="chevron-right" />
      <span>Tissue</span><Ic name="chevron-right" />
      <span>Organ</span><Ic name="chevron-right" />
      <span>Organism</span>
    </div>
  </div>
  <div class="grid-2 gap-3">
    <div class="card-soft"><div class="chip-icon mb-2"><Ic name="bread-slice" /></div><h3 class="!text-base">Carbohydrates</h3></div>
    <div class="card-soft"><div class="chip-icon mb-2"><Ic name="food-steak" /></div><h3 class="!text-base">Proteins</h3></div>
    <div class="card-soft" style="outline:2px solid var(--mda-cyan)"><div class="chip-icon mb-2"><Ic name="oil" /></div><h3 class="!text-base">Lipids</h3></div>
    <div class="card-soft"><div class="chip-icon mb-2"><Ic name="dna" /></div><h3 class="!text-base">Nucleic Acids</h3></div>
  </div>
</div>

---

# Macromolecules: Monomers &amp; Polymers

<table class="mda-table mt-6">
  <thead>
    <tr><th>Macromolecule</th><th>Monomer</th><th>Polymers</th><th>Examples</th></tr>
  </thead>
  <tbody>
    <tr><td>Carbohydrates</td><td>Monosaccharide</td><td>Starch, Glycogen, Cellulose</td><td>Glucose, Fructose</td></tr>
    <tr><td>Proteins</td><td>Amino Acid</td><td>Polypeptides</td><td>Enzymes, Hormones</td></tr>
    <tr><td>Lipids</td><td>Fatty Acid</td><td>TAG, Phospholipids, Cholesterol</td><td>Fats, Oils, Waxes</td></tr>
    <tr><td>Nucleic Acids</td><td>Nucleotide</td><td>DNA, RNA</td><td>A, G, T/U, C</td></tr>
  </tbody>
</table>

<div class="card-soft mt-5 text-sm max-w-4xl">
  Macromolecules are built from smaller subunits (<strong>monomers</strong>) linked together to form
  complex structures with vital functions.
</div>

---

# Lipids: Structure &amp; Function

<div class="grid-2 gap-6 mt-2">
  <div class="card-dark">
    <h3>Structure</h3>
    <ul class="tight mt-2 list-disc pl-5">
      <li>Large number of <strong>C–H bonds</strong> → non-polar &amp; hydrophobic</li>
      <li>Contain <strong>carboxyl</strong> and <strong>ester</strong> functional groups</li>
      <li>Monomer: <strong>Fatty Acid</strong> — carboxylic acid + long C–H chain (10–20 carbons)</li>
      <li>Non-polar hydrophobic <strong>"tail"</strong>; slightly polar hydrophilic carboxyl <strong>"head"</strong></li>
    </ul>
  </div>
  <div class="grid gap-3">
    <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="oil" /></div><div><h3 class="!text-base">Energy Storage</h3><p class="text-sm">Highly energy-rich due to many C–H bonds.</p></div></div>
    <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="dna" /></div><div><h3 class="!text-base">Cell Membranes</h3><p class="text-sm">Form the structural basis of all cellular membranes.</p></div></div>
    <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="message-text" /></div><div><h3 class="!text-base">Hormones &amp; Vitamins</h3><p class="text-sm">Precursors to steroid hormones and fat-soluble vitamins.</p></div></div>
  </div>
</div>

---

# Fatty Acid Structure

<div class="grid grid-cols-[1fr_1fr] gap-6 items-center mt-2">
  <div>
    <div class="card-soft py-6"><FattyAcid :saturated="true" color="#1E6FB8" /></div>
  </div>
  <div>
    <p class="text-sm">A fatty acid is a <strong>carboxylic acid</strong> with a long hydrocarbon chain.
    Lauric acid (C₁₂H₂₄O₂) is a 12-carbon <strong>saturated</strong> fatty acid.</p>
    <div class="grid-2 gap-3 mt-3">
      <div class="card"><h3 class="!text-base" style="color:#C0392B">"Head"</h3><p class="text-xs mt-1">Carboxyl group — slightly polar &amp; <strong>hydrophilic</strong>.</p></div>
      <div class="card"><h3 class="!text-base" style="color:#1E6FB8">"Tail"</h3><p class="text-xs mt-1">Long carbon chain — non-polar &amp; <strong>hydrophobic</strong>.</p></div>
    </div>
  </div>
</div>

---

# Naming Fatty Acids: The Omega System

<p class="-mt-2 max-w-4xl text-sm">Carbons in a fatty-acid chain are labeled from each end:
the carbon next to the carboxyl group is <strong>α (alpha)</strong>; the last carbon in the chain is
<strong>ω (omega)</strong>. The <strong>ω-n</strong> notation marks where the <strong>first double bond</strong>
appears, counting from the ω (terminal CH₃) end.</p>

<div class="grid-2 gap-6 mt-5">
  <div class="card">
    <FattyAcid :saturated="false" color="#1E6FB8" />
    <h3 class="!text-base mt-1">Omega-3 (ω-3)</h3>
    <p class="text-sm mt-1">First double bond at the <strong>3rd</strong> carbon–carbon bond from the terminal end.</p>
  </div>
  <div class="card">
    <FattyAcid :saturated="false" color="#14B8A6" />
    <h3 class="!text-base mt-1">Omega-6 (ω-6)</h3>
    <p class="text-sm mt-1">First double bond at the <strong>6th</strong> carbon from the end.</p>
  </div>
</div>

---

# Types of Fatty Acids

<div class="grid-2 gap-4 mt-2">
  <div class="card flex gap-4 items-center">
    <div class="shrink-0 w-40"><FattyAcid :saturated="true" color="#1E6FB8" /></div>
    <div><h3>Saturated</h3><p class="text-sm mt-1">Carbons packed with hydrogens — <strong>no double bonds</strong>. Solid at room temp (e.g. butter). All saturated fatty acids are non-essential.</p></div>
  </div>
  <div class="card flex gap-4 items-center">
    <div class="shrink-0 w-40"><FattyAcid :saturated="false" color="#14B8A6" /></div>
    <div><h3>Unsaturated</h3><p class="text-sm mt-1">One or more <strong>double bonds</strong> — fewer hydrogens. Liquid at room temp (e.g. oil). More polar &amp; soluble.</p></div>
  </div>
  <div class="card-soft"><h3 class="!text-base">Essential</h3><p class="text-sm mt-1">Not made by the body — must come from diet. Includes <strong>Linolenic, Linoleic &amp; Arachidonic</strong> acid (build ω-3 &amp; ω-6).</p></div>
  <div class="card-soft"><h3 class="!text-base">Non-Essential</h3><p class="text-sm mt-1">Made by the body or from diet. The body can only synthesize fatty acids with <strong>ω ≥ 7</strong>.</p></div>
</div>

---

# Saturated vs. Unsaturated Models

<div class="grid-2 gap-6 mt-3">
  <div class="card">
    <h3>Saturated — Straight</h3>
    <div class="my-3"><FattyAcid :saturated="true" color="#0B2540" /></div>
    <p class="text-sm">Arachidic, Stearic &amp; Palmitic acids are straight-chain — they <strong>pack tightly</strong>,
    forming solids at room temperature.</p>
  </div>
  <div class="card">
    <h3>Unsaturated — Kinked</h3>
    <div class="my-3"><FattyAcid :saturated="false" color="#14B8A6" /></div>
    <p class="text-sm">Arachidonic, Linoleic &amp; Linolenic acids <strong>bend</strong> at their double bonds —
    they can't pack tightly, staying liquid at room temperature.</p>
  </div>
</div>

---

# Medical Significance of Fatty Acids

<div class="grid grid-cols-[1fr_1fr] gap-6 mt-2 items-center">
  <div class="grid gap-4">
    <div class="card">
      <h3 style="color:#C0392B">Saturated — Danger</h3>
      <p class="text-sm mt-1">Form solid structures that adhere to blood-vessel walls, leading to
      <strong>Atherosclerosis</strong> (coronary artery blockage) and increasing the risk of
      <strong>myocardial infarction</strong>.</p>
    </div>
    <div class="card">
      <h3 style="color:#0E8A57">Unsaturated — Protective</h3>
      <p class="text-sm mt-1">Flow easily in the blood. Can <strong>prevent</strong> — and may even help
      treat — atherosclerosis. More soluble due to their double bonds.</p>
    </div>
  </div>
  <div class="card-soft py-5 flex flex-col items-center gap-4">
    <div class="text-center"><Artery :blocked="false" /><div class="text-xs font-semibold mt-1" style="color:#0E8A57">Healthy — open lumen</div></div>
    <div class="text-center"><Artery :blocked="true" /><div class="text-xs font-semibold mt-1" style="color:#C0392B">Atherosclerosis — narrowed</div></div>
  </div>
</div>

---

# Lipids in the Human Body

<p class="-mt-2 mb-4 max-w-4xl text-sm">The three major lipid macromolecules each have completely
different characteristics and functions.</p>

<div class="grid-3 gap-4">
  <div class="card">
    <div class="chip-icon mb-2"><Ic name="oil" /></div>
    <h3>Triglycerides (TAG)</h3>
    <p class="text-sm mt-1">Primary energy-storage lipid; found in adipose tissue.</p>
  </div>
  <div class="card">
    <div class="chip-icon mb-2"><Ic name="dna" /></div>
    <h3>Phospholipids</h3>
    <p class="text-sm mt-1">Amphipathic; form the cell-membrane bilayer.</p>
  </div>
  <div class="card">
    <div class="chip-icon mb-2"><Ic name="factory" /></div>
    <h3>Cholesterol</h3>
    <p class="text-sm mt-1">Amphipathic; precursor to hormones, bile, and Vitamin D.</p>
  </div>
</div>

---

# Triglycerides (TAG)

<div class="grid grid-cols-[0.95fr_1.05fr] gap-6 items-center">
  <div class="card-soft flex justify-center py-3"><Triglyceride /></div>
  <div>
    <p class="text-sm">The <strong>most abundant lipid</strong> in living organisms, stored in
    <strong>adipose tissue</strong>. One <strong>Glycerol</strong> (3-carbon, 3 hydroxyl groups) bonds to
    <strong>three Fatty Acids</strong> via <strong>Ester Bonds</strong>, formed by 3 condensation reactions
    (removing H₂O).</p>
    <div class="grid gap-2 mt-3">
      <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="oil" /></div><div><h3 class="!text-base">Energy Storage</h3><p class="text-xs">2× more energy than carbohydrates; sustains 6–10 weeks of starvation.</p></div></div>
      <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="factory" /></div><div><h3 class="!text-base">Temperature Regulation</h3><p class="text-xs">Adipose tissue insulates the body.</p></div></div>
      <div class="card flex gap-3 items-start"><div class="chip-icon shrink-0"><Ic name="message-text" /></div><div><h3 class="!text-base">Protection</h3><p class="text-xs">Cushions internal organs.</p></div></div>
    </div>
  </div>
</div>

---

# Phospholipids

<div class="grid grid-cols-[0.8fr_1.2fr] gap-6 items-center">
  <div class="card-soft flex justify-center py-4"><Phospholipid mode="single" /></div>
  <div>
    <p class="text-sm">An <strong>amphipathic</strong> molecule that forms the bilayer of the
    <strong>Cell Membrane</strong>.</p>
    <h3 class="!text-base mt-3 mb-1">Structure — 4 Components</h3>
    <ol class="tight text-sm list-decimal pl-5">
      <li><strong>Organic Molecule</strong> — choline, serine, or ethanolamine</li>
      <li><strong>Phosphate Group</strong> — polar, hydrophilic "head"</li>
      <li><strong>Glycerol Group</strong></li>
      <li><strong>Fatty Acid Tails</strong> — non-polar, hydrophobic</li>
    </ol>
    <div class="mt-3"><Phospholipid mode="bilayer" /></div>
  </div>
</div>

---

# Cholesterol

<div class="grid grid-cols-[1fr_1fr] gap-6 items-start mt-1">
  <div>
    <p class="text-sm">An <strong>amphipathic</strong> molecule and precursor to many hormones. It does
    not dissolve in blood — it travels inside <strong>Lipoproteins</strong>.</p>
    <div class="grid-2 gap-3 mt-3">
      <div class="card"><h3 class="!text-base" style="color:#C0392B">LDL</h3><p class="text-xs mt-1">Low-Density Lipoprotein — carries cholesterol from liver to tissues. <strong>"Bad cholesterol."</strong></p></div>
      <div class="card"><h3 class="!text-base" style="color:#0E8A57">HDL</h3><p class="text-xs mt-1">High-Density Lipoprotein — collects cholesterol from tissues to liver. <strong>"Good cholesterol."</strong></p></div>
    </div>
  </div>
  <div>
    <div class="card-soft"><h3 class="!text-base">Functions</h3>
      <ul class="tight text-sm list-disc pl-5 mt-1">
        <li>Cell-membrane fluidity &amp; rigidity</li>
        <li>Precursor of steroid hormones, bile &amp; Vitamin D</li>
      </ul>
    </div>
    <div class="mt-3 rounded-2xl px-4 py-3 text-sm" style="background:#FFF3D6;color:#9A7D0A">
      <strong>Hypercholesterolemia</strong> (high blood cholesterol) is a major risk factor for
      coronary heart disease &amp; myocardial infarction. <strong>Physical exercise raises HDL.</strong>
    </div>
  </div>
</div>

---

<div class="eyebrow">Summary</div>

# Lipids at a Glance

<div class="grid-2 gap-4 mt-3">
  <div class="card"><h3>Structure &amp; Function</h3><p class="text-sm mt-1">Fatty-acid monomers (carboxylic acid + hydrocarbon chain); functions: <strong>energy storage, cell membranes, hormones</strong>.</p></div>
  <div class="card"><h3>Fatty Acids</h3><p class="text-sm mt-1"><strong>ω-n</strong> naming; <strong>Saturated</strong> (no double bonds) vs <strong>Unsaturated</strong> (double bonds); Essential vs Non-essential.</p></div>
  <div class="card"><h3>3 Key Lipids</h3><p class="text-sm mt-1"><strong>Triglycerides</strong> → energy/protection; <strong>Phospholipids</strong> → cell membrane; <strong>Cholesterol</strong> → hormones, bile, Vitamin D.</p></div>
  <div class="card"><h3>Clinical Link</h3><p class="text-sm mt-1">Saturated fats → atherosclerosis risk; unsaturated fats are protective. Exercise raises HDL ("good cholesterol").</p></div>
</div>

---

# Review Questions

<div class="grid-2 gap-x-6 gap-y-3 mt-5 text-sm">
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">1</div><p>What are macromolecules &amp; the 4 major ones? What is the monomer of lipids?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">2</div><p>Why are fatty acids amphipathic? Why do unsaturated fatty acids bend — and why does it matter medically?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">3</div><p>What two molecules form a triglyceride? What reaction occurs and what bond forms?</p></div>
  <div class="card flex gap-3 items-start"><div class="ov-num text-[var(--mda-blue)] text-lg font-bold">4</div><p>Name the 4 components of a phospholipid. What is the difference between LDL &amp; HDL?</p></div>
</div>

<div class="mt-4 rounded-2xl px-4 py-3 text-sm" style="background:#D6F5E3;color:#0E8A57">
  Physical exercise elevates HDL ("good cholesterol") — a key takeaway for health and wellness!
</div>
