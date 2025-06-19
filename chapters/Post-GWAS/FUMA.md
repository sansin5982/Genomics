# Functional Mapping and Annotation of GWAS

## 🧪 What is FUMA?

**FUMA** stands for **Functional Mapping and Annotation**. It is a
web-based platform designed to annotate, prioritize, and interpret GWAS
results.

**Website**: <https://fuma.ctglab.nl>

FUMA connects GWAS findings to biological mechanisms using gene mapping,
tissue-specific expression, and functional enrichment analyses.

> **Explanation**: GWAS gives you a list of “hotspots” in the genome.
> FUMA helps you figure out which genes those hotspots affect, what
> tissues they work in, and what biological functions they might
> influence.

### 🔧 Input File Requirements

FUMA requires **GWAS summary statistics** as input.

#### 🔢 Accepted File Format

-   Plain text format (.txt or .tsv)
-   One line per SNP
-   No header or whitespace lines

#### 🔍 Essential Columns Required:

<table>
<thead>
<tr>
<th style="text-align: left;">Column</th>
<th style="text-align: left;">Meaning</th>
<th style="text-align: left;">Notes</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">SNP</td>
<td style="text-align: left;">rsid</td>
<td style="text-align: left;">Required</td>
</tr>
<tr>
<td style="text-align: left;">CHR</td>
<td style="text-align: left;">Chromosome Number</td>
<td style="text-align: left;">Required</td>
</tr>
<tr>
<td style="text-align: left;">BP</td>
<td style="text-align: left;">Base pair position</td>
<td style="text-align: left;">GRCh37/hg19 coordinates</td>
</tr>
<tr>
<td style="text-align: left;">P</td>
<td style="text-align: left;">p-value of association</td>
<td style="text-align: left;">eg. 2.3e-08</td>
</tr>
<tr>
<td style="text-align: left;">A1</td>
<td style="text-align: left;">Effect Allele</td>
<td style="text-align: left;">Optional, used in PRS</td>
</tr>
<tr>
<td style="text-align: left;">A2</td>
<td style="text-align: left;">Reference Allele</td>
<td style="text-align: left;">Optional</td>
</tr>
<tr>
<td style="text-align: left;">OR/Beta</td>
<td style="text-align: left;">Effect size or Odds ratio</td>
<td style="text-align: left;">Required if using Magam</td>
</tr>
<tr>
<td style="text-align: left;">N</td>
<td style="text-align: left;">Sample size (optional)</td>
<td style="text-align: left;">Improves power</td>
</tr>
</tbody>
</table>

> FUMA also allows VCF and PLINK formats in some contexts, but **summary
> statistics** are the primary input.

## 🔮 Key Modules & Tests in FUMA

FUMA consists of **two main pipelines**:

#### 1. SNP2GENE

#### 2. GENE2FUNC

### 🔹 1. SNP2GENE Module

This module performs the **core mapping and annotation** of GWAS SNPs.

#### ✅ A. Independent Significant SNP Identification

-   Select SNPs with **p &lt; 5e-8** (default)
-   Use **LD (r²) thresholds** to find independent signals (e.g., r²
    &lt; 0.6)
-   Identifies lead SNPs and tagged SNPs

> “Which SNPs are truly independent, and which ones are just tagging
> others?”

#### ✅ B. Functional Annotation of SNPs

FUMA uses multiple databases:

-   **ANNOVAR** for gene function (intronic, exonic, etc.)
-   **CADD score** (pathogenic potential)
-   **RegulomeDB score** (regulatory evidence)
-   **Chromatin states** from Roadmap Epigenomics
-   **eQTLs (expression QTLs)** from GTEx and other dataset

#### ✅ C. SNP-to-Gene Mapping Methods

FUMA uses 3 strategies:

<table>
<thead>
<tr>
<th style="text-align: left;">Mapping type</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">Positional</td>
<td style="text-align: left;">Based on physical distance to genes</td>
</tr>
<tr>
<td style="text-align: left;">Based on physical distance to genes</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: left;">eQTL Mapping</td>
<td style="text-align: left;">Links SNPs to genes whose expression they
regulate</td>
</tr>
<tr>
<td style="text-align: left;">Chromatin Mapping</td>
<td style="text-align: left;">Chromatin Mapping</td>
</tr>
</tbody>
</table>

> Think of it as “Which gene is closest?”, “Which gene is turned on by
> this SNP?”, and “Which gene does this SNP touch in 3D space?”

#### ✅ D. MAGMA Gene-Based Analysis

-   Aggregates SNPs into gene-level p-values
-   Tests **each gene’s association** with the phenotype

#### ✅ E. Tissue Expression Analysis

-   Tests if associated genes are enriched in specific tissues
-   Uses GTEx, BrainSpan, and other transcriptomic resources

#### ✅ F. Cell-Type Specificity (optional)

-   For neuro/immune traits, can check enrichment in single-cell types

### 🔹 2. GENE2FUNC Module

This module helps understand what the mapped genes do biologically.

#### ✅ A. Tissue Expression Heatmap

-   Shows expression levels across GTEx tissues for mapped genes
-   Highlights tissue-specific expression

#### ✅ B. Gene Set Enrichment

-   Uses MsigDB, GO, KEGG, Reactome databases
-   Enriches mapped genes into pathways/functions

#### ✅ C. Differentially Expressed Genes (DEG) Analysis

-   Identifies genes that are over- or under-expressed in specific
    tissues

#### ✅ D. Interaction Networks (GeneMANIA)

-   Visualizes how genes interact with each other (optional integration)

### Summary

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Step</th>
<th style="text-align: left;">What it does</th>
<th style="text-align: left;">Analogy</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><strong>SNP2GENE</strong></td>
<td style="text-align: left;">Connect SNPs to genes and tissues</td>
<td style="text-align: left;">“Where is the signal coming from and which
switch is it flipping?”</td>
</tr>
<tr>
<td style="text-align: left;"><strong>GENE2FUNC</strong></td>
<td style="text-align: left;">Discover what those genes actually do</td>
<td style="text-align: left;">“What job does this gene do in the
body?”</td>
</tr>
</tbody>
</table>

#### 📆 Final Notes

-   FUMA supports **summary-statistic-level** input, not
    individual-level genotype data.
-   Output includes **interactive plots, tables, and downloadable
    files**.
-   FUMA is widely used in publications and supports **multi-ancestry
    GWAS** if LD reference is appropriate

#### 🔗 References

-   Watanabe et al. (2017), “Functional mapping and annotation of
    genetic associations with FUMA.” Nature Communications.
    <https://www.nature.com/articles/s41467-017-01261-5>
-   FUMA official site: <https://fuma.ctglab.nl>
-   FUMA tutorials: <https://fuma.ctglab.nl/tutorial>
