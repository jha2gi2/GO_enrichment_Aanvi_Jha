# GO_enrichment_Aanvi_Jha
Question 4- GO enrichment, by Aanvi Jha (24114002)

# Genomic BED Files Documentation

## Overview
This project contains BED-format genomic annotation files commonly used in computational biology and genome analysis workflows.

The files describe transcription start sites (TSS) and promoter regions associated with genes. These datasets can be used for:
- Gene regulation studies
- Promoter analysis
- Genomic interval overlap analysis
- Epigenetic and transcription-factor binding studies
- Genome browser visualization

---

# Files Included

## 1. `genes_tss.bed`
This file contains genomic coordinates corresponding to transcription start sites (TSS) of genes.

### Typical Columns
| Column | Description |
|--------|-------------|
| Chromosome | Chromosome identifier |
| Start | Start coordinate |
| End | End coordinate |
| Gene Name | Associated gene identifier |
| Score | Optional annotation score |
| Strand | DNA strand orientation (+/-) |

### Applications
- Mapping transcription initiation sites
- Associating regulatory regions with genes
- RNA-seq and ChIP-seq analysis pipelines

---

## 2. `promoter.bed`
This file contains promoter-region coordinates for genes.

Promoter regions are regulatory DNA segments located upstream of transcription start sites and play an important role in controlling gene expression.

### Applications
- Motif discovery
- TF binding-site analysis
- Chromatin accessibility studies
- Regulatory genomics

---

# BED File Format

BED (Browser Extensible Data) is a standard tab-delimited format used to store genomic intervals.

General structure:

```text
chromosome    start    end    annotation
```

Example:

```text
chr1    12000    12500    GeneA
```

Coordinates follow zero-based indexing conventions used in most genome browsers.

---

# Tools Commonly Used with BED Files

These files are compatible with:
- BEDTools
- UCSC Genome Browser
- IGV (Integrative Genomics Viewer)
- SAMtools
- Bioconductor packages
- Python genomic libraries such as pybedtools and pyranges

---

# Example Usage

## Intersect promoter regions with genomic peaks
```bash
bedtools intersect -a promoter.bed -b peaks.bed
```

## Find overlaps between TSS and promoters
```bash
bedtools intersect -a genes_tss.bed -b promoter.bed
```

---

# Biological Significance

Studying promoter regions and transcription start sites helps researchers:
- Understand gene regulation mechanisms
- Identify active regulatory elements
- Analyze transcription-factor binding patterns
- Investigate epigenetic modifications
- Interpret functional genomics datasets

---



