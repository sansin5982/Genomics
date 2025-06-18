# 🧬 What is Post-GWAS?

Genome-Wide Association Studies (GWAS) help identify genetic variants
(mostly SNPs) associated with traits or diseases. However, GWAS alone
doesn’t explain how or why these variants impact biology. **Post-GWAS**
refers to all the downstream analyses that help interpret, validate, and
apply GWAS findings.

### 🔍 Post-GWAS refers to the analysis steps taken after identifying GWAS hits to:

Understand biological meaning

Find causal genes or pathways

Discover shared genetics across traits

------------------------------------------------------------------------

# 🔧 Categories of Post-GWAS Tools

-   We organize the tools into functional categories:

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

-   These tools help connect SNPs to genes or functional annotations.

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

> If GWAS gives you dots on a map, these tools help label cities,
> rivers, or forests near those dots.

------------------------------------------------------------------------

# 🌿 2. Tissue/Cell-Type Specificity Tools

-   We want to know: In which tissue or cell type is the signal coming
    from?

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

-   Used to understand which biological pathways or gene sets are
    involved.

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

> Think of this as grouping your top SNPs into “teams” and finding out
> which team (e.g., immune system, brain function) is winning.

------------------------------------------------------------------------

# 🧠 4. Genetic Correlation & Heritability Estimation

-   Understand how much of a trait is genetic and whether two traits
    share genetics.

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

-   Helps pinpoint the most likely causal variants among many.

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

> GWAS gives you a neighborhood; fine-mapping tries to find the actual
> house (causal variant).

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

> Think of MR like a genetic clinical trial — using nature’s random
> assignment of alleles to test if high BMI causes diabetes, for
> example.

------------------------------------------------------------------------

# 🌍 9. Advanced Tools: Single-cell, 3D Genome, ML

## 🔎 A. scGWAS

Integrates GWAS with single-cell transcriptomic data to identify cell
types or subtypes where disease-associated variants are most active. \*
Traditional GWAS + bulk RNA may miss fine-scale signals. \* GitHub:
<https://github.com/li-lab/scGWAS>

> If a disease is like a fire in a building, scGWAS helps you locate the
> exact room (cell type) where the fire started — not just the building.

## 🧠 B. S-LDSC (Stratified LD Score Regression)

-   Extension of LDSC that **partitions heritability** based on
    functional categories.
-   Which annotation (e.g. promoter, enhancer) contributes most to
    heritability?

## 🧬 C. H-MAGMA

-   Enhances MAGMA by integrating **Hi-C** data (3D chromatin structure)
    to assign distal SNPs to genes.
-   Especially useful for **brain disorders** and regulatory SNPs.

> Example: An intergenic SNP may loop to a gene promoter 1Mb away —
> H-MAGMA captures this.

## 💡 D. PoPs (Polygenic Priority Score)

-   Uses gene features (expression, pathways, networks) to **prioritize
    genes** near GWAS loci.
-   Trained on large GWAS + functional databases.
-   Especially useful when multiple genes are in LD with a lead SNP.

## 🎓 E. TWAS (Transcriptome-Wide Association Study)

-   Tests association of **predicted gene expression** with traits.
-   **Tools: PrediXcan// S-PrediXcan, FUSION, MetaXcan.**

## 🧪 F. Chromatin/eQTL-aware Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Open Targets</strong></td>
<td>Multi-omic GWAS portal</td>
</tr>
<tr>
<td><strong>CHiCAGO</strong></td>
<td>Chromatin interaction analysis</td>
</tr>
<tr>
<td><strong>FOCUS</strong></td>
<td>TWAS fine-mapping and gene prioritization</td>
</tr>
</tbody>
</table>

## 🧠 G. Machine Learning Tools for Gene Prioritization

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 87%" />
</colgroup>
<thead>
<tr>
<th>Tool</th>
<th>Method</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>DeepSEA</strong></td>
<td>Deep learning model to predict regulatory effects</td>
</tr>
<tr>
<td><strong>BIRD</strong></td>
<td>Bayesian integration of regulatory data</td>
</tr>
<tr>
<td><strong>Varmole</strong></td>
<td>Deep neural network with interpretable layers for regulatory SNP
effect modeling</td>
</tr>
</tbody>
</table>

## 🧬 H. Pathway-aware Polygenic Tools

<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 72%" />
</colgroup>
<thead>
<tr>
<th>Tool</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>AnnoPred</strong></td>
<td>Functionally informed PRS</td>
</tr>
<tr>
<td><strong>PRSet</strong> (in PRSice)</td>
<td>Pathway-level risk scoring</td>
</tr>
<tr>
<td><strong>TIGAR</strong></td>
<td>TWAS + network analysis for pathway-level prioritization</td>
</tr>
</tbody>
</table>

## 🧪 I. Functional Validation Resources

<table>
<colgroup>
<col style="width: 51%" />
<col style="width: 48%" />
</colgroup>
<thead>
<tr>
<th>Tool</th>
<th>Use</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>GTEx Portal</strong></td>
<td>eQTL tissue atlas</td>
</tr>
<tr>
<td><strong>ENCODE</strong> / <strong>Roadmap Epigenomics</strong></td>
<td>Regulatory annotation</td>
</tr>
<tr>
<td><strong>PsychENCODE</strong></td>
<td>Brain-specific functional genomics</td>
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
