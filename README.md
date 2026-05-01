#### QTL-seq Analysis Identifies Cy-2 Locus Conferring Resistance to ToLCNDV in Cucumber
## Project Overview

This repository contains a comprehensive QTL-seq analysis pipeline used to identify genomic regions associated with resistance to Tomato leaf curl New Delhi virus (ToLCNDV) in cucumber (Cucumis sativus L.).
The study integrates bulked segregant analysis (BSA), whole-genome resequencing, linkage mapping, and gene expression profiling to uncover the genetic architecture of viral resistance.

## Objectives
To identify genomic loci associated with ToLCNDV resistance using QTL-seq
To calculate SNP-index and Δ(SNP-index) for contrasting bulks
To map major QTL regions controlling resistance
To identify candidate genes within QTL intervals
To validate findings using molecular markers and qRT-PCR
## Biological Context
Species: Cucumis sativus (cucumber)
Pathogen: Tomato leaf curl New Delhi virus (ToLCNDV)
Trait: Viral disease resistance
Population: F₂ segregating population
Parents:
DC 91 → Resistant
DC 773 → Susceptible
## Experimental Design
160 F₂ individuals phenotyped using disease severity scale (0–4)
Two DNA bulks constructed:
Resistant bulk (15 individuals)
Susceptible bulk (15 individuals)
Whole-genome resequencing performed using Illumina HiSeq
## Bioinformatics Workflow
1. Quality Control
Tool: FastQC
Filtering: Phred score ≥ 30
2. Read Trimming
Tool: Trimmomatic
3. Alignment
Tool: BWA-MEM
Reference genome: C. sativus cv. Gy14_genome_v2
4. Variant Calling
Tool: BCFtools (mpileup)
Filters:
Depth ≥ 10
Quality ≥ 30
MAF ≥ 0.05
5. SNP-index Calculation
SNP-index computed for each bulk
Δ(SNP-index) = Resistant bulk − Susceptible bulk
6. QTL Detection
Tool: QTL-seq v2.2.2
Sliding window:
Window size: 2 Mb
Step size: 10 kb
7. Variant Annotation
Tool: SnpEff
Identification of high-impact and missense variants
## Key Findings
A major QTL (Cy-2) identified on chromosome 7
Genomic interval: 4.8 – 6.6 Mb (~1.8 Mb region)
Strong Δ(SNP-index) peak exceeding statistical thresholds
Resistance follows monogenic recessive inheritance (3:1 segregation)
## Candidate Genes
152 genes identified within QTL interval
Key functional categories:
Leucine-rich repeat (LRR) proteins
Serine/threonine kinases
MYB transcription factors
Cytochrome P450 enzymes
Calmodulin-binding proteins

These genes are associated with:

Pathogen recognition
Signal transduction
Hormonal regulation (SA vs JA pathways)
Defense-related metabolic responses
## Marker Development & Validation
SSR marker: SSR00931
InDel marker: AMS12
CAPS marker: AMS13
All markers showed tight linkage to resistance locus
Genetic distances:
SSR00931 → 9.3 cM
AMS12 → 8.5 cM
AMS13 → 13.2 cM
## Expression Analysis
qRT-PCR performed at 7, 14, 21, and 28 dpi
14 candidate genes analyzed
Resistant genotype showed:
Strong activation of defense signaling pathways
Enhanced SA-mediated response
Coordinated PTI and ETI responses

## Outputs
SNP-index and Δ(SNP-index) plots
Identified QTL regions
Variant annotation tables
Candidate gene lists
Expression analysis plots
## Biological Interpretation

The Cy-2 locus represents a major-effect genomic region controlling resistance to ToLCNDV in cucumber. Resistance is associated with coordinated activation of immune signaling pathways, including receptor-mediated recognition, calcium signaling, kinase cascades, and salicylic acid–dependent defense responses.

## Data Availability

NCBI BioProject: PRJNA1366342
Accessions: SAMN53309079–SAMN53309082

## Disclaimer

This repository represents an academic implementation of QTL-seq analysis based on original research data and is intended for reproducible research and educational purposes.

## Author

Chandrika Ghoshal
ICAR–Indian Agricultural Research Institute, New Delhi
