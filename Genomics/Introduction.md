# Introduction to Genomics

## 1.1 Definition and Scope of Genomics

### 1.1.1 Genomics as the Study of Entire Genomes

Genomics is defined as the scientific discipline that investigates the
entirety of an organism’s genetic material—its **genome**—in a holistic,
high-throughput, and integrative manner. A genome encompasses all DNA
within an organism, including nuclear, mitochondrial, and (in plants)
chloroplast genomes. Unlike classical genetics, which examines
individual genes in isolation, genomics treats the genome as a dynamic
system, analyzing structure, function, interactions, and evolution
simultaneously across all genetic elements.

> **Note**: The term genome was coined by Hans Winkler in 1920 as a
> portmanteau of gene and chromosome.

### 1.1.2 Structural, Functional, and Comparative Genomics

-   **Structural Genomics**: Focuses on determining the
    three-dimensional organization of DNA within chromosomes, including
    gene mapping, repeat identification,, and regulatory landscapes.
-   **Functional Genomics**: Seeks to elucidate the biological roles of
    genes and non-coding regions through transcriptomics, proteomics,
    and gene perturbation studies.
-   **Comparative Genomics**: Aligns genomes across species to infer
    evolutionary relationships, identify conserved elements, and detect
    lineage-specific adaptations.

### 1.1.3 Interdisciplinary Nature: Biology, Computing, Statistics

Genomics is inherently **interdisciplinary**: \* **Molecular Biology**
provides mechanistic insights into DNA replication, transcription, and
repair. \* **Bioinformatics** enables storage, retrieval, and analysis
of terabase-scale data using algorithms and databases. \*
**Biostatistics** ensures rigorous hypothesis testing, multiple-testing
correction, and probabilistic modeling of genomic phenomena. \*
**Machine Learning** powers variant calling, gene prediction, and
phenotype prediction from genomic data.

### 1.1.4 Applications Across Medicine, Agriculture, Evolution

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Domain</th>
<th style="text-align: left;">Application</th>
<th style="text-align: left;">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><strong>Medicine</strong></td>
<td style="text-align: left;">Precision oncology, pharmacogenomics</td>
<td style="text-align: left;">Tumor mutational profiling, warfarin
dosing</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Agriculture</strong></td>
<td style="text-align: left;">Genomic selection, GMO design</td>
<td style="text-align: left;">Drought-resistant maize via CRISPR</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Evolution</strong></td>
<td style="text-align: left;">Phylogenomics, adaptation studies</td>
<td style="text-align: left;">Neanderthal introgression in modern
humans</td>
</tr>
</tbody>
</table>

### 1.1.5 Distinction from Molecular Biology and Biochemistry

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Discipline</th>
<th style="text-align: left;">Focus</th>
<th style="text-align: left;">Scale</th>
<th style="text-align: left;">Methodology</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><strong>Molecular Biology</strong></td>
<td style="text-align: left;">Mechanisms of gene expression</td>
<td style="text-align: left;">Single gene/protein</td>
<td style="text-align: left;">PCR, cloning, gel electrophoresis</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Biochemistry</strong></td>
<td style="text-align: left;">Chemical reactions in cells</td>
<td style="text-align: left;">Pathway level</td>
<td style="text-align: left;">Enzyme assays, mass spectrometry</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Genomics</strong></td>
<td style="text-align: left;">System-wide genetic architecture</td>
<td style="text-align: left;">Entire genome</td>
<td style="text-align: left;">NGS, microarrays, genome browsers</td>
</tr>
</tbody>
</table>

## 1.2 Historical Development and Milestones

### 1.2.1 Discovery of DNA Structure (Watson and Crick, 1953)

Using X-ray diffraction data from Rosalind Franklin and Maurice Wilkins,
James Watson and Francis Crick proposed the **double-helical model of
DNA** with antiparallel strands, complementary base pairing (A-T, G-C),
and a sugar-phosphate backbone. This model, published in Nature,
provided the structural basis for genetic inheritance and replication.

> Watson, J. D., & Crick, F. H. C. (1953). Molecular structure of
> nucleic acids: A structure for deoxyribose nucleic acid. Nature,
> 171(4356), 737–738.

### 1.2.2 Early Sequencing Efforts (Frederick Sanger, 1977)

Frederick Sanger developed the dideoxy chain-termination method,
enabling sequence determination of DNA fragments up to 1,000 bp. This
breakthrough earned him the 1980 Nobel Prize in Chemistry and was used
to sequence the first genome—bacteriophage φX174 (5,369 bp).

> Sanger, F., Nicklen, S., & Coulson, A. R. (1977). DNA sequencing with
> chain-terminating inhibitors. Proceedings of the National Academy of
> Sciences, 74(12), 5463–5467.

### 1.2.3 Launch of the Human Genome Project (1990)

Initiated by the U.S. Department of Energy and National Institutes of
Health, the **Human Genome Project (HGP)** aimed to sequence the entire
~3 billion base pairs of the human genome by 2005. It was an
international collaboration involving 20 institutions across six
countries.

> U.S. Department of Energy & National Institutes of Health. (1990).
> Understanding Our Genetic Inheritance: The U.S. Human Genome Project:
> The First Five Years FY 1991–1995.

### 1.2.4 Completion of First Human Genome Draft (2001)

Two draft sequences were published simultaneously:

-   **Public Consortium** (IHGSC): Hierarchical shotgun approach
-   **Celera Genomics** (Venter et al.): Whole-genome shotgun

> International Human Genome Sequencing Consortium. (2001). Initial
> sequencing and &gt;analysis of the human genome. Nature, 409(6822),
> 860–921.
>
> Venter, J. C., et al. (2001). The sequence of the human genome.
> Science, 291(5507), 1304–1351.

### 1.2.5 Development of High-Throughput Sequencing (2005 Onward)

**Next-Generation Sequencing (NGS)** platforms (454, Illumina, SOLiD)
introduced massively parallel sequencing, reducing cost from ~$100
million (HGP) to &lt;$1,000 per genome by 2020.

> Metzker, M. L. (2010). Sequencing technologies—the next generation.
> Nature Reviews Genetics, 11(1), 31–46.

### 1.2.6 Key Projects: 1000 Genomes, ENCODE, TCGA

-   **1000 Genomes Project (2008–2015)**: Catalogued common and rare
    variants in 2,504 individuals from 26 populations. &gt; The 1000
    Genomes Project Consortium. (2015). A global reference for human
    genetic variation. Nature, 526(7571), 68–74.
-   **ENCODE (2003–present)**: Mapped functional elements (transcription
    factor binding, histone marks) across the human genome. &gt; ENCODE
    Project Consortium. (2012). An integrated encyclopedia of DNA
    elements in the human genome. Nature, 489(7414), 57–74.
-   **TCGA (2006–2016)**: Multi-omics profiling of &gt;11,000 tumors
    across 33 cancer types. &gt; Weinstein, J. N., et al. (2013). The
    Cancer Genome Atlas Pan-Cancer analysis project. Nature Genetics,
    45(10), 1113–1120.

## 1.3 Differences Between Genetics and Genomics

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr>
<th style="text-align: left;">Aspect</th>
<th style="text-align: left;">Classical Genetics</th>
<th style="text-align: left;">Genomics</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><strong>Scope</strong></td>
<td style="text-align: left;">Single or few genes</td>
<td style="text-align: left;">Entire genome</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Methodology</strong></td>
<td style="text-align: left;">Pedigree analysis, crosses</td>
<td style="text-align: left;">High-throughput sequencing</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Data Scale</strong></td>
<td style="text-align: left;">Genotypes at 1–100 loci</td>
<td style="text-align: left;">&gt;10⁶ variants</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Analytical Approach</strong></td>
<td style="text-align: left;">Reductionist (gene → phenotype)</td>
<td style="text-align: left;">Systems-level (networks,
interactions)</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Key Tools</strong></td>
<td style="text-align: left;">Mendelian ratios, linkage mapping</td>
<td style="text-align: left;">GWAS, WGS, bioinformatics pipelines</td>
</tr>
</tbody>
</table>

> **Example**: Cystic fibrosis (single CFTR mutation) vs. height
> (polygenic, &gt;10,000 variants).

## 1.4 Key Concepts: Genes, Genomes, and Genetic Variation

### 1.4.1 Gene Definition and Annotation

A **gene** is a functional unit of DNA that is transcribed into RNA and
(in protein-coding genes) translated into protein. Annotation involves:

-   Identifying **open reading frames (ORFs)**
-   Predicting **splice junctions**
-   Assigning **functional categories** (GO terms)

Tools: Ensembl, GENCODE, RefSeq.

### 1.4.2 Genome Size and Complexity Across Organisms

<table>
<thead>
<tr>
<th style="text-align: left;">Organism</th>
<th style="text-align: left;">Genome Size (Mb)</th>
<th style="text-align: left;">Gene Count</th>
<th style="text-align: left;">Coding DNA (%)</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;">Escherichia coli</td>
<td style="text-align: left;">4.6</td>
<td style="text-align: left;">~4,400</td>
<td style="text-align: left;">~88%</td>
</tr>
<tr>
<td style="text-align: left;">Saccharomyces cerevisiae</td>
<td style="text-align: left;">12</td>
<td style="text-align: left;">~6,000</td>
<td style="text-align: left;">~70%</td>
</tr>
<tr>
<td style="text-align: left;">Caenorhabditis elegans</td>
<td style="text-align: left;">100</td>
<td style="text-align: left;">~20,000</td>
<td style="text-align: left;">~25%</td>
</tr>
<tr>
<td style="text-align: left;">Homo sapiens</td>
<td style="text-align: left;">3,200</td>
<td style="text-align: left;">~19,000</td>
<td style="text-align: left;">~1.5%</td>
</tr>
<tr>
<td style="text-align: left;">Triticum aestivum (wheat)</td>
<td style="text-align: left;">16,000</td>
<td style="text-align: left;">~100,000+</td>
<td style="text-align: left;">&lt;1%</td>
</tr>
</tbody>
</table>

### 1.4.3 Coding vs. Non-Coding DNA

-   **Coding DNA (~1.5%)**: Exons translated into proteins.
-   **Non-Coding DNA (~98.5%)**:
    -   Introns (~25%)
    -   Regulatory elements (promoters, enhancers)
    -   Repetitive sequences (LINEs, SINEs, satellites)
    -   Pseudogenes, lncRNAs

### 1.4.4 Types of Genetic Variation

<table>
<thead>
<tr>
<th style="text-align: left;">Variant Type</th>
<th style="text-align: left;">Size</th>
<th style="text-align: left;">Example</th>
<th style="text-align: left;">Frequency</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><strong>SNP</strong></td>
<td style="text-align: left;">1 bp</td>
<td style="text-align: left;">A → G</td>
<td style="text-align: left;">~1/300 bp</td>
</tr>
<tr>
<td style="text-align: left;"><strong>Indel</strong></td>
<td style="text-align: left;">1–50 bp</td>
<td style="text-align: left;">Insertion/deletion</td>
<td style="text-align: left;">~1/1,000 bp</td>
</tr>
<tr>
<td style="text-align: left;"><strong>CNV</strong></td>
<td style="text-align: left;">1 kb–5 Mb</td>
<td style="text-align: left;">Duplication</td>
<td style="text-align: left;">~12% of genome</td>
</tr>
<tr>
<td style="text-align: left;"><strong>SV</strong></td>
<td style="text-align: left;">&gt;50 bp</td>
<td style="text-align: left;">Inversion, translocation</td>
<td style="text-align: left;">~0.5% of genome</td>
</tr>
</tbody>
</table>

### 1.4.5 Heritability and Genotype-Phenotype Relationships

-   Narrow-sense heritability *h*<sup>2</sup>

$$
\large h^2 = \frac{V\_{A}}{V\_{P}}
$$

where *V*<sub>*A*</sub> additive genetic variance, *V*<sub>*P*</sub> =
total phenotypic variance.

-   **Polygenic Risk Scores (PRS)**: Aggregate effect of thousands of
    variants.
-   **Penetrance**: Probability of phenotype given genotype.

## 1.5 Overview of Genomic Data Types

### 1.5.1 DNA Sequence Data (FASTA, FASTQ)

-   **FASTA**: Simple sequence format

<!-- -->

    >chr1:1000-1100
    ATGCCGATCGTAGCTAGCTA...

-   **FASTQ**: Includes Phred quality scores (Q = −10
    *l**o**g*<sub>10</sub> P\_error)

<!-- -->

    @SEQ_ID
    ATGCCGATCG...
    +
    IIIIIIIIII...  (Q ≥ 30 → 99.9% accuracy)

### 1.5.2 Variant Data (VCF Files)

**Variant Call Format (VCF)** stores genomic variants:

    #CHROM  POS  ID  REF  ALT  QUAL  FILTER  INFO  FORMAT  SAMPLE1
    1       12345  rs123  A    G    99   PASS  DP=30  GT:GQ   0/1:45

### 1.5.3 Expression Data (Counts, TPM, FPKM)

-   **Raw Counts**: Reads mapped to gene
-   **FPKM**: Fragments Per Kilobase Million
-   **TPM** (preferred):

$$
\large TPM\_{i} = (\frac{reads\_{i}}{length\_{i}}) \times \frac{10^6}{\sum(\frac{reads\_{j}}{length\_{j}})}
$$

### 1.5.4 Epigenetic Data (Methylation, Chromatin States)

-   **Bisulfite Sequencing**: Detects 5-methylcytosine (5mC)
-   **ChIP-seq**: Maps histone modifications (e.g., H3K4me3 → active
    promoter)
-   **ATAC-seq**: Identifies open chromatin
-   **Chromatin States**: 15-state model (Roadmap Epigenomics)

### 1.5.5 Metadata: Sample Info, Experimental Design, Quality Metrics

Essential for reproducibility:

-   **Sample**: Donor ID, tissue, age, sex
-   **Experiment**: Platform, library prep, read length
-   **Quality**: % mapped reads, duplication rate, GC bias, FastQC
    scores

### References

-   Alberts, B., Johnson, A., Lewis, J., et al. (2014). Molecular
    Biology of the Cell (6th ed.). Garland Science.
-   Brown, T. A. (2018). Genomes 4 (4th ed.). CRC Press.
-   Krebs, J. E., Goldstein, E. S., & Kilpatrick, S. T. (2017). Lewin’s
    GENES XII. Jones & Bartlett Learning.
-   Str.org Resources: NCBI Genome Database. Available at:
    <https://www.ncbi.nlm.nih.gov/genome>
-   UCSC Genome Browser. Available at: <https://genome.ucsc.edu>
