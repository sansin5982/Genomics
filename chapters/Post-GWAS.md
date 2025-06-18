# 🧬 What is Post-GWAS?

Genome-Wide Association Studies (GWAS) help identify genetic variants
(mostly SNPs) associated with traits or diseases. However, GWAS alone
doesn’t explain how or why these variants impact biology. **Post-GWAS**
refers to all the downstream analyses that help interpret, validate, and
apply GWAS findings.

------------------------------------------------------------------------

# 🔧 Categories of Post-GWAS Tools

<table>
<colgroup>
<col style="width: 37%" />
<col style="width: 62%" />
</colgroup>
<thead>
<tr>
<th>Category</th>
<th>Goal</th>
</tr>
</thead>
<tbody>
<tr>
<td>Gene Mapping &amp; Annotation</td>
<td>Map SNPs to nearby or regulatory genes</td>
</tr>
<tr>
<td>Tissue/Cell-Type Specificity</td>
<td>Identify tissues or cells where SNPs are active</td>
</tr>
<tr>
<td>Pathway Enrichment</td>
<td>Understand affected biological functions/pathways</td>
</tr>
<tr>
<td>Genetic Correlation/Heritability</td>
<td>Estimate trait heritability &amp; shared genetics</td>
</tr>
<tr>
<td>Fine-Mapping</td>
<td>Pinpoint causal variants among significant loci</td>
</tr>
<tr>
<td>Colocalization</td>
<td>Check if two traits share causal variants</td>
</tr>
<tr>
<td>Polygenic Risk Scores (PRS)</td>
<td>Summarize genetic risk across many SNPs</td>
</tr>
<tr>
<td>Causal Inference (MR)</td>
<td>Use genetics to infer causality</td>
</tr>
<tr>
<td>Advanced: Multi-omics &amp; ML</td>
<td>Use single-cell, Hi-C, ML for deeper interpretation</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🛠 1. Gene Mapping & Annotation Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>FUMA</td>
<td>Functional mapping and annotation pipeline</td>
</tr>
<tr>
<td>ANNOVAR</td>
<td>Annotates SNPs with gene function, region</td>
</tr>
<tr>
<td>VEP</td>
<td>Predicts effects of variants on genes</td>
</tr>
<tr>
<td>HaploReg</td>
<td>Annotates regulatory motifs, LD info</td>
</tr>
<tr>
<td>SNiPA</td>
<td>Functional annotation browser with LD info</td>
</tr>
<tr>
<td>LocusZoom</td>
<td>Regional association visualization</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🌿 2. Tissue/Cell-Type Specificity Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>What it does</th>
</tr>
</thead>
<tbody>
<tr>
<td>MAGMA</td>
<td>Tests for gene expression enrichment in tissues</td>
</tr>
<tr>
<td>DEPICT</td>
<td>Predicts relevant tissues and cell types</td>
</tr>
<tr>
<td>CELLECT</td>
<td>Prioritizes cell types using single-cell RNA-seq</td>
</tr>
<tr>
<td>LDSC-SEG</td>
<td>Partitions heritability by epigenetic annotations</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🎯 3. Pathway and Functional Enrichment

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>GSEA</td>
<td>Gene Set Enrichment Analysis</td>
</tr>
<tr>
<td>MAGMA</td>
<td>Also performs gene-set enrichment</td>
</tr>
<tr>
<td>DEPICT</td>
<td>Data-driven pathway and function prediction</td>
</tr>
<tr>
<td>FUMA GENE2FUNC</td>
<td>Functional enrichment in GO, KEGG, etc.</td>
</tr>
<tr>
<td>DAVID, PANTHER</td>
<td>Older tools for pathway analysis</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🧠 4. Genetic Correlation & Heritability Estimation

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>LDSC</td>
<td>LD Score Regression for heritability, correlation</td>
</tr>
<tr>
<td>LDAK</td>
<td>Alternative heritability method</td>
</tr>
<tr>
<td>MiXeR</td>
<td>Polygenicity and overlap quantification</td>
</tr>
<tr>
<td>GCTA-GREML</td>
<td>Individual-level data heritability analysis</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🧬 5. Fine-Mapping Tools

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 87%" />
</colgroup>
<thead>
<tr>
<th>Tool</th>
<th>Purpose</th>
</tr>
</thead>
<tbody>
<tr>
<td>FINEMAP</td>
<td>Bayesian fine-mapping using summary stats</td>
</tr>
<tr>
<td>PAINTOR</td>
<td>Combines annotations with fine-mapping</td>
</tr>
<tr>
<td>SuSiE</td>
<td>Sum of Single Effects model-based fine-mapping</td>
</tr>
<tr>
<td>CAVIAR</td>
<td>Identifies causal variants and their probabilities</td>
</tr>
<tr>
<td>PolyFun</td>
<td>Functional annotation informed fine-mapping</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🧪 6. Colocalization Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>COLOC</td>
<td>Bayesian colocalization of GWAS and eQTL</td>
</tr>
<tr>
<td>eCAVIAR</td>
<td>Joint analysis of GWAS and functional data</td>
</tr>
<tr>
<td>SMR</td>
<td>Summary-data-based Mendelian Randomization</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 📊 7. Polygenic Risk Score Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>PRSice-2</td>
<td>Efficient PRS calculation with tuning</td>
</tr>
<tr>
<td>LDpred</td>
<td>Bayesian PRS with LD adjustments</td>
</tr>
<tr>
<td>PLINK</td>
<td>Basic PRS and score calculation</td>
</tr>
<tr>
<td>PRS-CS</td>
<td>Bayesian continuous shrinkage method</td>
</tr>
<tr>
<td>REGENIE</td>
<td>Efficient PRS + mixed model GWAS</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🧬 8. Causal Inference / Mendelian Randomization

<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 81%" />
</colgroup>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>TwoSampleMR</td>
<td>MR using summary stats (R package)</td>
</tr>
<tr>
<td>MR-PRESSO</td>
<td>Corrects for horizontal pleiotropy</td>
</tr>
<tr>
<td>GSMR</td>
<td>MR with outlier removal using GCTA</td>
</tr>
<tr>
<td>CAUSE</td>
<td>Accounts for correlated and uncorrelated pleiotropy</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 🌍 9. Advanced Tools: Single-cell, 3D Genome, ML

## 🔎 A. scGWAS

-   Integrates GWAS with single-cell RNA-seq data.
-   Identifies disease-relevant **cell subtypes**.
-   GitHub: <https://github.com/li-lab/scGWAS>

## 🧬 B. H-MAGMA

-   Extends MAGMA by integrating **Hi-C chromatin interaction** data.
-   Useful for brain and regulatory disorders.

## 💡 C. PoPs (Polygenic Priority Score)

-   Ranks genes based on network, expression, and pathway features.

## 🎓 D. TWAS (Transcriptome-Wide Association Study)

-   Tests association of **predicted gene expression** with traits.
-   Tools: PrediXcan, FUSION, MetaXcan.

## 🧪 E. Chromatin/eQTL-aware Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Open Targets</td>
<td>Multi-omic GWAS portal</td>
</tr>
<tr>
<td>CHiCAGO</td>
<td>Chromatin interaction analysis</td>
</tr>
<tr>
<td>FOCUS</td>
<td>TWAS fine-mapping and gene prioritization</td>
</tr>
</tbody>
</table>

## 🧠 F. ML & Deep Learning

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>DeepSEA</td>
<td>Predicts regulatory effects using deep learning</td>
</tr>
<tr>
<td>Varmole</td>
<td>Neural network modeling of SNP → gene → trait</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 📌 Summary Table

<table>
<thead>
<tr>
<th>Category</th>
<th>Tool Examples</th>
</tr>
</thead>
<tbody>
<tr>
<td>Mapping</td>
<td>FUMA, ANNOVAR, VEP</td>
</tr>
<tr>
<td>Tissues</td>
<td>MAGMA, DEPICT, CELLECT</td>
</tr>
<tr>
<td>Pathways</td>
<td>GSEA, DEPICT, FUMA</td>
</tr>
<tr>
<td>Heritability</td>
<td>LDSC, MiXeR, LDAK</td>
</tr>
<tr>
<td>Fine-mapping</td>
<td>FINEMAP, PAINTOR, SuSiE</td>
</tr>
<tr>
<td>Colocalize</td>
<td>COLOC, eCAVIAR, SMR</td>
</tr>
<tr>
<td>PRS</td>
<td>PRSice-2, LDpred, PRS-CS</td>
</tr>
<tr>
<td>MR</td>
<td>TwoSampleMR, MR-PRESSO, GSMR</td>
</tr>
<tr>
<td>Advanced</td>
<td>scGWAS, H-MAGMA, PoPs, DeepSEA</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

# 📝 Final Tips for Students

-   Choose tools based on **your biological question**.
-   Most tools work with **summary statistics**, but others require
    functional or expression data.
-   Visual tools like LocusZoom, GeneMANIA, and STRING are useful for
    interpretation.
-   Always try to **replicate and validate** your findings when
    possible.
