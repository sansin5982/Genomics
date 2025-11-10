# Single Cell RNA-Seq

## 🔬 What is Single-cell RNA-seq (scRNA-seq)?

**Single-cell RNA sequencing (scRNA-seq)** is a powerful technique that
allows researchers to examine the gene expression of individual cells.
It reveals the **transcriptomic diversity** within a tissue by capturing
RNA from **each single cell separately**, enabling the study of:

-   Cellular heterogeneity
-   Cell subtypes or rare cell populations
-   Developmental trajectories
-   Cell-state transitions (e.g., in cancer, differentiation)

## 🧬 What is Bulk RNA-seq?

**Bulk RNA sequencing (Bulk RNA-seq)\* measures the **average gene
expression\*\* from a mixture of thousands or millions of cells. It
provides a **population-level view** of transcriptional activity but
loses information about **individual cell differences**.

### 🧪 Examples

<table>
<colgroup>
<col style="width: 16%" />
<col style="width: 36%" />
<col style="width: 46%" />
</colgroup>
<thead>
<tr>
<th>Scenario</th>
<th>Bulk RNA-seq</th>
<th>scRNA-seq</th>
</tr>
</thead>
<tbody>
<tr>
<td>🧠 <strong>Brain Tissue</strong></td>
<td>Measures average expression across all neurons, glia, etc.</td>
<td>Distinguishes expression patterns of neurons vs astrocytes vs
oligodendrocytes</td>
</tr>
<tr>
<td>🧬 <strong>Cancer Biopsy</strong></td>
<td>Averages gene expression across tumor and immune cells</td>
<td>Identifies different cancer cell clones and immune infiltrates</td>
</tr>
<tr>
<td>👶 <strong>Embryonic Development</strong></td>
<td>Blurs gene expression across multiple stages or cell types</td>
<td>Tracks cell fate decisions (e.g., mesoderm vs ectoderm vs
endoderm)</td>
</tr>
<tr>
<td>💊 <strong>Drug Response in Tumors</strong></td>
<td>Can tell if expression changes but not which cell types
responded</td>
<td>Reveals specific subpopulations (e.g., resistant cancer stem cells)
that responded</td>
</tr>
<tr>
<td>🧫 <strong>Immune Cell Profiling</strong></td>
<td>Shows immune-related genes averaged across all PBMCs</td>
<td>Identifies distinct populations: T-cells, B-cells, monocytes, NK
cells</td>
</tr>
</tbody>
</table>

### 🔍 Key Differences: Bulk vs Single-Cell RNA-seq

<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 29%" />
<col style="width: 43%" />
</colgroup>
<thead>
<tr>
<th>Feature</th>
<th>Bulk RNA-seq</th>
<th>Single-cell RNA-seq</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Unit of Analysis</strong></td>
<td>Population of cells</td>
<td>Individual cells</td>
</tr>
<tr>
<td><strong>Heterogeneity Resolution</strong></td>
<td>Lost (averaged out)</td>
<td>Captured</td>
</tr>
<tr>
<td><strong>Sensitivity</strong></td>
<td>High for abundant transcripts</td>
<td>Lower (dropout for low-expression genes)</td>
</tr>
<tr>
<td><strong>Data Complexity</strong></td>
<td>Moderate</td>
<td>Very high (sparse, high-dimensional)</td>
</tr>
<tr>
<td><strong>Cost per sample</strong></td>
<td>Lower</td>
<td>Higher</td>
</tr>
<tr>
<td><strong>Use case</strong></td>
<td>General gene expression trends</td>
<td>Discovering new cell types, rare populations</td>
</tr>
<tr>
<td><strong>Examples of Methods</strong></td>
<td>Illumina-based RNA-seq</td>
<td>10x Genomics, SMART-Seq, Drop-seq</td>
</tr>
</tbody>
</table>

Imagine you’re listening to a choir:

-   🧏‍♂️ Bulk RNA-seq = You hear the **overall music** but can’t tell
    which individual singer is singing which part.

-   👂 scRNA-seq = You **mic up** each singer and can analyze each
    person’s voice separately.

#### 🎯 When to Use Which?

<table>
<colgroup>
<col style="width: 82%" />
<col style="width: 17%" />
</colgroup>
<thead>
<tr>
<th>Question</th>
<th>Preferred Method</th>
</tr>
</thead>
<tbody>
<tr>
<td>Are genes A and B differentially expressed in cancer vs normal?</td>
<td><strong>Bulk RNA-seq</strong></td>
</tr>
<tr>
<td>Which cell types exist in a tumor, and what genes define them?</td>
<td><strong>scRNA-seq</strong></td>
</tr>
<tr>
<td>What happens to the overall transcriptional landscape after drug
treatment?</td>
<td><strong>Bulk RNA-seq</strong></td>
</tr>
<tr>
<td>How does cell A transition to cell B during development?</td>
<td><strong>scRNA-seq</strong></td>
</tr>
</tbody>
</table>

## 🧬 What is Spatial Transcriptomics?

**Spatial Transcriptomics (ST)** refers to techniques that allow
researchers to **measure gene expression in the spatial context of
tissue architecture**. Unlike bulk or scRNA-seq, spatial transcriptomics
tells you where a gene is expressed within a tissue section—**preserving
spatial relationship**s between cells.

Imagine looking at a city at night:

-   🔦 Bulk RNA-seq: Tells you the total amount of light the city emits
    (no info about location).

-   🔍 scRNA-seq: Lets you inspect light from each building, but
    buildings are removed from their location.

-   🧭 Spatial transcriptomics: Lets you see **which building emits
    which color of light and where it’s located** in the city.

### 🧪 Comparison Table

<table>
<colgroup>
<col style="width: 16%" />
<col style="width: 21%" />
<col style="width: 26%" />
<col style="width: 35%" />
</colgroup>
<thead>
<tr>
<th>Feature</th>
<th>Bulk RNA-seq</th>
<th>Single-cell RNA-seq</th>
<th>Spatial Transcriptomics</th>
</tr>
</thead>
<tbody>
<tr>
<td>🎯 <strong>Resolution</strong></td>
<td>Tissue-level (average)</td>
<td>Cell-level</td>
<td>Cell- or subcellular-level (with spatial info)</td>
</tr>
<tr>
<td>🧬 <strong>Cell Type Info</strong></td>
<td>Lost</td>
<td>Captured</td>
<td>Captured + spatial location</td>
</tr>
<tr>
<td>🧭 <strong>Spatial Info</strong></td>
<td>No</td>
<td>No</td>
<td>Yes</td>
</tr>
<tr>
<td>🧪 <strong>Data Type</strong></td>
<td>1D expression profile</td>
<td>1D expression profile per cell</td>
<td>2D expression matrix mapped to tissue section</td>
</tr>
<tr>
<td>💰 <strong>Cost &amp; Complexity</strong></td>
<td>Low to moderate</td>
<td>High</td>
<td>Very high</td>
</tr>
<tr>
<td>🧫 <strong>Sample Preparation</strong></td>
<td>Homogenized RNA from bulk tissue</td>
<td>Dissociated tissue into single cells</td>
<td>Tissue section + spatial barcoding</td>
</tr>
<tr>
<td>🔍 <strong>Use Cases</strong></td>
<td>Expression profiling, DEGs</td>
<td>Cell subtypes, rare cells, trajectories</td>
<td>Tissue microenvironment, histology + transcriptomics</td>
</tr>
<tr>
<td>🧬 <strong>Example Questions</strong></td>
<td>Are certain genes upregulated?</td>
<td>Which cells express this gene?</td>
<td>Where in the tissue is this gene expressed?</td>
</tr>
</tbody>
</table>

### 🎯 Examples by Scenario

<table>
<colgroup>
<col style="width: 68%" />
<col style="width: 31%" />
</colgroup>
<thead>
<tr>
<th>Biological Question</th>
<th>Best Technique</th>
</tr>
</thead>
<tbody>
<tr>
<td>What genes are differentially expressed in liver disease?</td>
<td><strong>Bulk RNA-seq</strong></td>
</tr>
<tr>
<td>Which immune cell types are enriched in infected lungs?</td>
<td><strong>scRNA-seq</strong></td>
</tr>
<tr>
<td>Where in a tumor do immune cells localize?</td>
<td><strong>Spatial Transcriptomics</strong></td>
</tr>
<tr>
<td>Which region of the brain expresses gene X in Alzheimer’s?</td>
<td><strong>Spatial Transcriptomics</strong></td>
</tr>
</tbody>
</table>

### 🧠 Tools/Technologies for Spatial Transcriptomics

<table>
<colgroup>
<col style="width: 60%" />
<col style="width: 39%" />
</colgroup>
<thead>
<tr>
<th>Platform/Tool</th>
<th>Features</th>
</tr>
</thead>
<tbody>
<tr>
<td>🔬 <strong>10x Genomics Visium</strong></td>
<td>Combines H&amp;E imaging with spatial transcriptomics</td>
</tr>
<tr>
<td>🧪 <strong>MERFISH</strong> (Multiplexed Error-Robust Fluorescence
in situ Hybridization)</td>
<td>RNA localization at subcellular resolution</td>
</tr>
<tr>
<td>📊 <strong>Slide-seq / Slide-seqV2</strong></td>
<td>Spatial barcoding using beads on slides</td>
</tr>
<tr>
<td>🧬 <strong>SeqFISH / ISS</strong></td>
<td>Fluorescent tagging of RNAs in situ</td>
</tr>
</tbody>
</table>

#### 🔬 Summary

<table>
<colgroup>
<col style="width: 41%" />
<col style="width: 13%" />
<col style="width: 10%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th>Question</th>
<th>Bulk RNA-seq</th>
<th>scRNA-seq</th>
<th>Spatial Transcriptomics</th>
</tr>
</thead>
<tbody>
<tr>
<td>Expression level of genes</td>
<td>✅</td>
<td>✅</td>
<td>✅</td>
</tr>
<tr>
<td>Which cell expressed the gene?</td>
<td>❌</td>
<td>✅</td>
<td>✅</td>
</tr>
<tr>
<td>Where in the tissue was it expressed?</td>
<td>❌</td>
<td>❌</td>
<td>✅</td>
</tr>
<tr>
<td>Rare cell type detection</td>
<td>❌</td>
<td>✅</td>
<td>✅ (if resolution allows)</td>
</tr>
<tr>
<td>Cell trajectory analysis</td>
<td>❌</td>
<td>✅</td>
<td>Partial (with spatial dynamics)</td>
</tr>
</tbody>
</table>
