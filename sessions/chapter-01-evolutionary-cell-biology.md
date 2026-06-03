---
title: Chapter 1 — Evolutionary Cell Biology
layout: default
parent: Sessions
nav_order: 1
---

# Chapter 1 — Evolutionary Cell Biology

## Book chapter

Michael Lynch, *Evolutionary Cell Biology*, Chapter 1.

## Main question

**Historical perspectives and problems with biological fields:**
- Evolutionary biology and its traditional aliance with ecology. Ecological interactions determine the major drivers of evolution. Molecular and cellular features determines what is possible at all for the evolution to modify from a common ancestor.
- Natural selection is not the sole responsible for biological diversity.
- Lack of integration of genetics, what is actually transmitted during evolution, in optimization theory and evo-devo.
- Most of the research focuses on multicellular species but most of the biological diversity resides in unicellular species.
- A framework for the evolution of cell biological features and structures is lacking.
- For evolutionary cell biology, we need comparative studies in a wide range of cells. Our information is limited to a few model organisms and human cell cultures.
- 
**What is evolutionary cell biology?**
Evolutionary cell biology is the fusion of cell biology with evolutionary thinking, informed by the integration of the great engines of theoretical and quantitative biology – biochemistry, biophysics, and population genetics (Lynch et al. 2014).

**To understand evolution of cells:**
1. The classical intellectual domain of evolutionary biology is ecology, where the usual focus is on challenges imposed by factors outside of the organism. 
2. We must consider the cellular environment, which imposes historical contingencies, biophysical constraints, and molecular stochasticity. 
3. There is the population-genetic environment.
The joint operation of these three environments dictates what natural selection can and cannot accomplish in different phylogenetic lineages, thereby dictating the mechanisms by which cellular features evolve.

Conclusion: Cell biology offers powerful opportunities for identifying the explicit biological connections between genotypes, phenotypes, and fitness, essential to the development of a mature field of evolutionary biology. The focus of this book is on the degree to which selection, effectively neutral processes, historical contingencies, and/or constraints at the biochemical and biophysical levels jointly influence patterns of evolutionary diversification. This way of thinking may ultimately find use in the applied fields of agriculture, medicine, environmental science, and synthetic biology.

**Extended Eevolutionary Synthesis and what it offers:**
Although a persistent claim of the EESers is that the environmental induction of a trait in a novel situation can enhance the exposure of the trait to selection, thereby magnifying the response to selection, this is by no means a novel insight. Such effects are central to the concept of genotype × environment interaction, the theory of which dates back decades (Lynch and Walsh 1998). Indeed, breeders have long exploited this concept to determine the optimum environmental setting in which to select for particular phenotypes (Walsh and Lynch 2018). Thus, the idea that evolutionary theory needs to be remodelled to account for phenotypic plasticity is without merit.

**Balance between evolutionary forces**
What selection can achieve is modulated by the relative power of nonadaptive forces.
- Selection-drift balance
- Selection-mutation balance
- The importance of neutral models and the challenge for defining them

**Grand challenges ahead**
- The origin of life: More than three billion years ago, cellular biochemistry became established in such a way as to provide all of the necessities for evolution: metabolism, growth, replication, and variation. 
- The roots of organismal complexity: Although it is commonly asserted that added layers of cellular complexity make for more robust and evolutionary successful organisms, evidence for this is entirely lacking.
- **Molecular stochasticity**:  Collectively, these features and more (including asymmetries in cell division) lead to substantial stochasticity in cellular composition, even among cells with identical genotypes inhabiting homogenous environments. Natural selection operates on phenotypic variance, and is more efficient when most of the variance is due to genetic differences.
- Molecular complexes: The number of subunits underlying the same protein can vary across species, but not always in ways that reflect organismal complexity. This weak connection is very unlike the situation in genome evolution, where genome architecture becomes enormously complex in large multicellular species

## Possible discussion questions
Take from summary:
1. In which types of evolutionary biology questions would we need an understanding of cell and molecular biology?
2. In what aspects of your work, understanding cell biology can contribute to the evolutionary question you address?
3. How can cell biology be integrated with population genetics?
4. Neutral models in population genetics and molecular evolution are prevalent. Do such models exist for evolution of traits?

## Cell or molecular biology method theme: Single cell image analysis
Main conceptual problem: Averaging cells destroys information. A population of genetically identical cells can contain subpopulations with radically different fates — some dividing, some dying, some committing to differentiation — and bulk assays like western blots or bulk RNA-seq report only the mean, flattening all of that variation into a single number. The methods in this paper are all answers to the same question: how do we measure what individual cells are actually doing, and at what scale?
Challenge: Finding methods that are non-destructive and dynamic so we can watch the same cell change state in real time rather than inferring state from a snapshot of a killed population.
The starting point is **fluorescent reporters**. 
The authors showcase a toolkit of **genetically encoded sensors** that convert invisible intracellular states into light signals:the FUCCI system reports cell-cycle position by expressing two differently colored proteins that appear and disappear in opposite phases; kinase translocation reporters (KTRs) convert signaling activity into a nuclear-to-cytoplasmic shift you can see under the microscope; FRET-based probes report ATP levels or redox state in specific organelles.

1. Time-lapse microscopy with live reporters — revealing that gene regulation is all-or-none, not graded: Used fluorescent reporters to follow gene expression in individual cells over time. Population averages suggested gradual repression, but single-cell tracking showed all-or-none switching.
2. Single-cell analysis of stress response — overturning a 30-year-old model of HSF1: Used single-cell imaging to measure HSF1 nuclear foci and chaperone protein levels in individual tumor cells. Contrary to the old model, persistent HSF1 foci marked stressed, vulnerable cells. The active stress-response state correlated with foci dissolution, not foci formation.
3. Microfluidics + aging tracking — discovering two distinct aging trajectories in yeast: Used microfluidic chambers to keep aging yeast mother cells in place while daughters washed away. Long-term imaging revealed two distinct aging trajectories. The output was lifespan path, daughter morphology, mitochondrial aggregation, and early irreversible aging fate.
4. Six-color live imaging of cell fate decisions — showing that fate is determined earlier than anyone thought: Used six fluorescent reporters to track cell cycle, sporulation, metabolism, storage molecules, and mitochondria during starvation. Fate choice between meiosis and quiescence was predictable before the final cell division. Vacuole size and metabolic state were key predictors.
5. High-content screening (HCS) with deep learning — systematic genome-wide phenotyping: Used automated microscopy to image millions of cells across many genetic perturbations. Segmentation, feature extraction, and deep learning classified phenotypes at scale. The output was genome-wide genotype-to-phenotype maps and detection of abnormal or rare cell states.

That real-time observation is only possible with **time-lapse microscopy and lineage tracking**, which the paper treats as the method that most fundamentally changes what you can ask. The clearest demonstration is a yeast experiment tracking six reporters simultaneously through starvation-induced fate decisions: cells either entered meiosis or quiescence, and single-cell analysis revealed that fate was determined before the last cell division, far earlier than anyone had suspected. That result was not accessible to any population-level readout. Lineage tracking also enables microfluidics as a companion technique — chambers that physically retain mother cells while daughters wash away, making it possible to follow rare aging cells through their entire lifespan without losing them in the crowd of young cells.

When the question shifts from hypothesis-driven to discovery-driven — what does every gene in the genome do to cell morphology? — the answer is high-content screening (HCS). Automated microscopes image thousands of genetic perturbation conditions; computational pipelines then segment each cell, extract hundreds of quantitative features per cell (shape, texture, intensity distributions, subcellular localization), and use machine learning to classify cells or detect outlier phenotypes. Deep learning is increasingly used at the classification step because it learns relevant image features automatically rather than requiring researchers to pre-specify them.

Finally, when you want to connect the live-imaging dynamics to gene expression state, spatial RNA FISH methods (smFISH, MERFISH, seqFISH+) let you fix cells after a time-lapse run and measure transcriptomes in place, preserving the spatial relationships between neighboring cells. This hybrid live-then-fix strategy is currently the most practical bridge between dynamic cell behavior and molecular cell state.

## Evolutionary or comparative method theme: Single-cell analysis reveals contextdependent, cell-level selection of mtDNA

This is a 2024 Nature paper from the Bhatt/Mootha group at MGH. The central question is one the field has long debated: when heteroplasmy levels shift in a dividing cell population, is that driven by selection or random drift, and if selection, does it act at the level of cell fitness (whole-cell proliferation advantage) or intracellularly (preferential replication or degradation of mtDNA molecules within a single cell)?

The technical innovation: SCI-LITE

**What they found**

Using precise mtDNA base editing (DdCBE) to install either a functionally damaging missense mutation (LHON-associated, complex I subunit MT-ND4) or a matched synonymous silent mutation two base pairs away, they tracked heteroplasmy dynamics over 15 days at single-cell resolution.

The key results, in order of logical argument:

Cell populations in standard culture actively purge the nonsynonymous (damaging) variant but not the synonymous one — a direct argument against simple drift.
Cells with high nonsynonymous heteroplasmy grow slower and die more when forced to rely on OXPHOS (galactose medium), confirming the fitness cost is real and mechanistically tied to complex I dysfunction.
Within individual lineages (tracked via unique ancestry barcodes + SCI-LITE), heteroplasmy stays stable even while the population distribution shifts. This is the critical finding: if intracellular selection were happening, every lineage would show a gradual decline; instead, high-heteroplasmy lineages simply drop out of the population. Selection acts at the cell level, not the mtDNA molecule level.
The sign of selection is environment-dependent. The same truncating complex I mutation that is purged in normoxia or galactose is positively selected in hypoxia or when complex V is inhibited by oligomycin — conditions where losing complex I is actually beneficial. In oligomycin-treated cultures, cells that divided the most ended up with the highest heteroplasmy.
Why it matters broadly

The authors suggest this framework reframes how we think about accumulation of mtDNA mutations in ageing and cancer. The standard assumption is that nonsynonymous mtDNA mutations accumulate because selection is weak. This paper argues instead that some of those mutations may accumulate because the metabolic environment of aged or tumour cells makes them selectively advantageous. The Hürthle cell carcinoma experiment — where introducing the truncating complex I mutation accelerated tumour formation in mice — makes this concrete.

The paper rests on two technical pillars working together: a way to write controlled mutations into mitochondrial DNA, and a way to read heteroplasmy in thousands of individual cells at once. Let me walk through both from scratch.

The problem they needed to solve first: writing mutations into mtDNA

Normal gene-editing tools like CRISPR don't work on mitochondrial DNA. Mitochondria have their own small genome (mtDNA), separate from the nuclear genome, and the molecular machinery needed to deliver CRISPR into mitochondria doesn't exist yet. So for years, researchers studying heteroplasmy had to use naturally occurring mutations, which you can't control or pair with a matched silent control.

The authors used a recently developed tool called DdCBE (deaminase-coupled base editor). This is a protein you deliver into the cell (via a plasmid, i.e., a small loop of DNA you transfect into cells). Once inside, DdCBE finds a specific site on the mtDNA and chemically converts one DNA base into another — specifically, it converts a cytosine (C) into a uracil (U), which the cell's own replication machinery then reads as a thymine (T). The result is a point mutation at a precise location, without cutting the DNA. Crucially, this is a base change, not a deletion or insertion, so you can install either a missense mutation (one that changes the amino acid in the resulting protein) or a synonymous/silent mutation (one that changes the DNA sequence but codes for the same amino acid, so the protein is identical).

They used two versions:

LHON DdCBE: installs a missense mutation in the MT-ND4 gene, a subunit of Complex I of the mitochondrial respiratory chain. This specific mutation is associated with Leber's hereditary optic neuropathy (LHON), a real human disease. The mutation breaks Complex I function.
SILENT DdCBE: installs a synonymous mutation two base pairs away in the same gene. Same position, same gene, but the protein is unaffected.
This pair is the experimental heart of the paper. Because the only difference is whether the protein is broken or not, any difference in how the two variants behave in a population must be due to the functional consequence, not some quirk of the DNA sequence itself.

What is heteroplasmy?

Each cell contains hundreds to thousands of mtDNA copies. Heteroplasmy simply means that not all copies are identical \ — some are wild-type and some carry the mutation. The heteroplasmy level of a cell is the fraction of its mtDNA copies that carry the mutant version. A cell at 80% heteroplasmy has 80% mutant and 20% wild-type mtDNA. This matters because mitochondrial function only breaks down above a threshold (roughly 60-90% mutant), so a cell at 50% heteroplasmy might function normally while a cell at 90% is severely impaired.

The reading problem: why bulk measurement is misleading

If you take a million cells and extract all their DNA to measure heteroplasmy, you get one number \ — the average across all cells. That average could mean every cell is at exactly 50%, or it could mean half the cells are at 100% mutant and the other half are at 0%. These are biologically completely different situations, but a bulk assay can't distinguish them. This is the same averaging problem that motivated the Mattiazzi Usaj paper you presented earlier.

The new method: SCI-LITE

SCI-LITE (single-cell combinatorial indexing leveraged to interrogate targeted expression) is the tool they built to measure heteroplasmy in thousands of individual cells cheaply and at scale.

The core challenge in single-cell sequencing is: how do you know which DNA or RNA molecule came from which cell? The dominant solution (used by commercial platforms like 10x Genomics) is to put each cell in its own tiny droplet in a microfluidic device, add a bead with a unique barcode into each droplet, and attach that barcode to every molecule in that cell. This works but requires expensive microfluidic chips and is slow.

SCI-LITE uses a different strategy called split-pool barcoding, which avoids droplets entirely. The logic is clever: instead of putting cells in separate physical containers, you identify cells by giving them a combination of barcodes across multiple rounds. Here's how it works step by step:

Round 1 (Reverse transcription barcoding): All cells are fixed and permeabilized (their membranes are made porous so reagents can get inside, but the cells stay as individual particles). They are distributed into the wells of a multi-well plate. In each well, a barcoded reverse transcription primer is added, which copies the target RNA (in this case mtRNA encoding MT-ND4) into cDNA and attaches a well-specific barcode (Barcode 1) to every cDNA molecule in that well. All cells are then pooled together again.

Round 2 (Ligation barcoding): The pooled cells are redistributed randomly into new wells. In each well, a ligation reaction attaches a second barcode (Barcode 2) plus a unique molecular identifier (UMI — a short random sequence that marks individual molecules so you can count them without double-counting) to all cDNA molecules in that well. Cells are pooled again.

Round 3 (PCR and sequencing barcodes): The pooled cells are redistributed into new wells, lysed (broken open), and the cDNA is amplified by PCR. During PCR, two more Illumina sequencing barcodes (Barcodes 3 and 4, the standard indexes used in all Illumina sequencing) are attached.

After sequencing, every cDNA molecule has four barcodes. The key insight: the probability that two different cells traversed the same path through all three rounds of redistribution by chance is very low (the paper validates a doublet rate of only 0.8%). So the four-barcode combination serves as a near-unique cell identifier, even though the cells were never physically separated.

A UMI (unique molecular identifier) deserves its own brief explanation: before PCR amplification, every molecule gets tagged with a short random sequence. Since PCR copies the same molecule many times, you'd otherwise count the same original molecule dozens of times. The UMI tells you "these 30 reads all came from one original molecule," so you count it as one. This converts raw read counts into true molecule counts.

How the two tools work together to answer the biological question

With DdCBE they could install precisely controlled mutations at known heteroplasmy levels. With SCI-LITE they could then track each cell's heteroplasmy individually over time \ — not as a population average, but as a distribution across thousands of single cells.

The critical experiment combined SCI-LITE with lineage barcoding: cells were transduced with a lentiviral library (a collection of viruses each carrying a different short DNA sequence), so each cell received one unique "ancestry barcode" permanently integrated into its nuclear genome. Every descendant of that cell inherits the same ancestry barcode. Now SCI-LITE was multiplexed to simultaneously read both the mtDNA heteroplasmy (from mtRNA) and the ancestry barcode (from nuclear mRNA) in each cell.

This allowed them to ask, within each lineage: did heteroplasmy change over time? If intracellular selection were happening (mutant mtDNA molecules replicating faster or being degraded less), every lineage's heteroplasmy would drift downward. What they saw instead was that heteroplasmy was stable within lineages, but lineages with high heteroplasmy simply disappeared from the population. That pattern is the fingerprint of cell-level selection: whole cells with too much mutant mtDNA grow slowly and drop out, while their internal heteroplasmy doesn't change before they do.

In short: DdCBE gave them clean experimental control over what mutation was present and at what level; SCI-LITE gave them the resolution to see how that mutation was behaving cell-by-cell and lineage-by-lineage over time. Neither tool alone could have answered the question.

## Optional papers or resources

## Notes from discussion


