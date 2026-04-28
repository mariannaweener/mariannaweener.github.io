<a href="#about">
  <img 
    src="https://media.licdn.com/dms/image/v2/D4D03AQGS8gdiTZT8Fw/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1682457911773?e=1778716800&v=beta&t=-ZpMYreuOoUxH_OPjjRZPZVoz1VQlweP9112AZDPs_w" 
    alt="About Me" 
    width="250" 
    align="right"
  />
</a>

<table>
<tr>
<td valign="top" width="210">

### Navigation
- [About](#about)
- [Projects](#projects)
- [AlphaGenome](#alphagenome)
- [SpliceAI](#spliceai)
- [Experimental Validation](#experimental-validation)
- [Discussions](#discussions)
- [Methods](#methods)

</td>
<td valign="top">

# Ocular Genomics | Harvard Medical School

**Physician-Scientist · Inherited Retinal Degenerations · Functional Genomics · Artificial Intelligence-Driven Variant Interpretation**

[![Mass Eye and Ear](https://img.shields.io/badge/Institution-Mass%20Eye%20%26%20Ear-blue)](https://www.masseyeandear.org)
[![Harvard Medical School](https://img.shields.io/badge/Affiliation-Harvard%20Medical%20School-crimson)](https://hms.harvard.edu)
[![Broad Institute](https://img.shields.io/badge/Collaborator-Broad%20Institute-green)](https://www.broadinstitute.org)

</td>
</tr>
</table>

---

## About

I am a physician-scientist at the Ocular Genomics Institute, Harvard Medical School and Mass Eye and Ear, specializing in inherited retinal degenerations. I maintain a registry of over 10,000 patients and bridge high-resolution clinical phenotyping with computational and experimental genomics approaches.

My work sits at the intersection of functional splicing biology, machine learning-based variant interpretation, and translational medicine. I have over 15 years of clinical experience and collaborate closely with the Medical Population Genetics group at the Broad Institute.

I also consult for leading gene therapy biotechnology and pharmaceutical companies, advising on computational pipeline design, data strategy, and translational decision-making.

---

## Projects

### Cryptic Exon Activation in Inherited Retinal Degenerations

My primary research investigates how deep intronic variants — sequence changes located far from exon boundaries — trigger inappropriate inclusion of cryptic exons into messenger RNA transcripts of known inherited retinal degeneration disease genes.

Non-coding variants that alter messenger RNA splicing are increasingly recognized as important contributors to the genetic causality of Mendelian disorders, accounting for an estimated 30% of inherited retinal degeneration cases. Despite their significance, predicting intronic variant pathogenicity accurately remains a major challenge.

**Key questions driving this work:**
- Which deep intronic variants activate cryptic exons in inherited retinal degeneration genes?
- How can we improve computational prediction of intronic variant pathogenicity?
- Can high-throughput experimental assays close the gap between prediction and validation?

---

## AlphaGenome

As part of our variant benchmarking effort, we evaluated AlphaGenome alongside the top-performing computational classifiers for variant pathogenicity prediction, using our experimentally validated dataset as ground truth.

**What we found:**

AlphaGenome proved highly informative overall, particularly for periexonic variants. However, we identified meaningful discrepancies in its predictions for deep intronic variants — both false positives and false negatives — that are not captured by existing prediction programs.

**Dataset evaluated:**
- 992 deep intronic variants (more than 50 base pairs from the nearest exon)
- 4,056 periexonic variants (fewer than 50 base pairs from the nearest exon)
- Drawn from unsolved inherited retinal degeneration patients and families

**Our perspective:**

While many newly developed algorithms present promising results, there remains a clear lack of robust experimental validation — particularly for deep intronic and non-coding variant classes. Our goal is to help bridge that gap by contributing experimentally validated datasets and ocular tissue RNA sequencing data to improve model training in a biologically accurate, tissue-specific manner.

We are actively interested in collaborations aimed at integrating retinal genomics expertise into next-generation variant effect prediction tools, and welcome discussion on how best to complement existing training datasets with our cases.

---

## SpliceAI

We benchmarked SpliceAI as part of our evaluation of the top four best-performing classifiers for deep intronic variant pathogenicity prediction, using an autosomal recessive inheritance pattern.

SpliceAI was evaluated head-to-head against AlphaGenome and other leading tools using our high-throughput splicing assay experimental results as ground truth. While SpliceAI performs well for variants near splice sites, its sensitivity for deep intronic variants — those more than 50 base pairs from the nearest exon — remains limited.

Our experimental dataset provides a unique opportunity to benchmark and improve tools like SpliceAI using real patient-derived variant data with functional read-outs.

---

## Experimental Validation

### High-Throughput Splicing Assay Platform

To systematically evaluate intronic variant pathogenicity, we co-developed a high-throughput splicing assay platform in collaboration with the Medical Population Genetics group at the Broad Institute.

**How it works:**

A variant library of approximately 5,000 variants covering a 300 base pair intronic window was generated and cloned into the high-throughput splicing assay plasmid. This plasmid contains a minigene composed of an intron flanked by 5-prime and 3-prime split green fluorescent protein exons.

The plasmid variant library was transfected into HEK293 cells. Forty-eight hours later, total RNA was extracted from the transfected cells. RNA transcripts produced by the high-throughput splicing assay minigene were amplified by reverse transcription polymerase chain reaction and sequenced. Intronic sequences spliced between the two green fluorescent protein exons were identified and quantified.

**Scale of validation to date:**

| Variant class | Count | Distance from exon |
|---|---|---|
| Deep intronic variants | 992 | More than 50 base pairs |
| Periexonic variants (controls) | 4,056 | Fewer than 50 base pairs |
| **Total** | **~5,000** | |

Periexonic variant results served as experimental controls for deep intronic variant evaluation.

**Workflow:**
1. Variant library cloning into minigene construct
2. Stable transfection into HEK293 cells
3. Fluorescence-activated cell sorting at the flow cytometry facility
4. RNA extraction and reverse transcription polymerase chain reaction amplification
5. Sequencing and quantification of splicing outcomes

---

## Discussions

We welcome collaboration and scientific exchange on the following topics:

**Variant pathogenicity prediction**
We are interested in discussing discrepancies we have observed in AlphaGenome and SpliceAI predictions for deep intronic variants, and how experimental datasets can complement computational model development.

**Ocular tissue RNA sequencing data contribution**
We can contribute RNA sequencing data from ocular tissues to efforts aimed at improving variant effect prediction models. We are interested in ensuring this data is used in a biologically accurate, tissue-specific way, and believe that retinal domain expertise should guide how such datasets are integrated into model training.

**Collaborative validation**
As we identify interesting and validated results from our high-throughput splicing assay platform, we aim to share findings that could serve as a starting point for collaboration — now or in the future.

**Open questions we are exploring:**
- How can ocular tissue RNA sequencing data best complement existing variant effect predictor training sets?
- What is the most effective framework for integrating retinal expert knowledge into computational pipelines?
- How do we define a robust ground-truth benchmark for deep intronic variant pathogenicity?

Feel free to open an issue or reach out directly to start a conversation.

---

## Methods

### Summary of Key Methods Used

**High-Throughput Splicing Assay**
Minigene-based functional assay using a plasmid containing an intron flanked by split green fluorescent protein exons. Variant libraries are cloned, transfected into HEK293 cells, and splicing outcomes are quantified by sequencing.

**Fluorescence-Activated Cell Sorting**
Performed regularly at the flow cytometry facility to separate cell populations based on green fluorescent protein expression levels following stable transfection.

**Variant Library Construction**
A variant library of approximately 5,000 variants spanning a 300 base pair intronic region was generated from unsolved inherited retinal degeneration patient cohorts and cloned into the high-throughput splicing assay plasmid.

**Computational Benchmarking**
The top four best-performing variant pathogenicity classifiers — including AlphaGenome and SpliceAI — were evaluated against experimental ground truth, stratified by autosomal recessive inheritance pattern and variant distance from exon boundaries.

**Sequencing and Quantification**
RNA transcripts from the high-throughput splicing assay minigene were amplified by reverse transcription polymerase chain reaction and sequenced. Intronic sequences retained between green fluorescent protein exons were identified and quantified to assess cryptic exon inclusion rates.

**Patient Registry**
A curated registry of over 10,000 inherited retinal degeneration patients supports variant identification, phenotype-genotype correlation, and prioritization of unsolved cases for functional study.

---

*Ocular Genomics Institute · Harvard Medical School · Mass Eye and Ear · Broad Institute Medical Population Genetics Group*
