<script type="text/javascript"
  id="MathJax-script"
  async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# 🧠 LDSC?

**LDSC (LD Score Regression)** is a statistical method used to:

-   Estimate **heritability** from GWAS summary statistics.
-   Quantify **genetic correlation** between traits.
-   Distinguish **polygenicity** from confounding (e.g., population
    stratification).

> **Explanation**: LDSC tells you how much of a trait is due to
> genetics, and whether two traits share genetic roots — all without
> needing individual-level data.

------------------------------------------------------------------------

## 🧮 Core Concept of LD Score Regression

-   **LD Score (*ℓ*<sub>*i*</sub>)** of a SNP = sum of
    ***r*<sup>2</sup>** values with other SNPs within a 1 cM window.
-   SNPs with high LD scores tag more variants → expected to have
    **higher test statistics** under polygenicity.

### Regression Model:

$$
\Large E\[\chi^2\] = 1 + \frac{N h\_g^2 \ell}{M}
$$

Where:

-   *χ*<sup>2</sup>: test statistic for SNP i

-   *N*: sample size

-   *h*<sub>*g*</sub><sup>2</sup>: SNP heritability

-   ℓ: LD score

-   *M*: number of SNPs

-   **Slope** → heritability  

-   **Intercept** → inflation due to confounding

------------------------------------------------------------------------

### 📥 Input File Requirements

#### 1. GWAS Summary Statistics

Required columns:

<table>
<thead>
<tr>
<th>Column</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>SNP</td>
<td>rsID</td>
</tr>
<tr>
<td>CHR</td>
<td>Chromosome</td>
</tr>
<tr>
<td>BP</td>
<td>Base pair position</td>
</tr>
<tr>
<td>A1, A2</td>
<td>Alleles</td>
</tr>
<tr>
<td>P or Z</td>
<td>p-value or Z-score</td>
</tr>
<tr>
<td>N</td>
<td>Sample size</td>
</tr>
<tr>
<td>BETA/OR</td>
<td>Effect size or odds ratio</td>
</tr>
<tr>
<td>INFO</td>
<td>(Optional) imputation quality</td>
</tr>
</tbody>
</table>

#### Download LDSC

#### Step 1: Clone the LDSC GitHub repository

**git clone <https://github.com/bulik/ldsc.git>**

#### Step 2: Move into the ldsc directory

**cd ldsc**

#### Step 3: Create an environment with LDSC dependencies

**conda env create –file environment.yml**

#### Activate LDSC environment

**ldsc activate ldsc**

#### Once environment is activated

**./ldsc.py -h**

**./munge\_sumstats.py -h**

-   If these commands fail then there is some issue in installation

This will help you install ldsc `python version 2.7.15`. Once
installation is done, we need to download files from:

-   <https://zenodo.org/records/7768714>
-   <https://ibg.colorado.edu/cdrom2021/Day06-nivard/GenomicSEM_practical/eur_w_ld_chr/>

#### Mung Sumstats

Use the LDSC tool munge\_sumstats.py to format summary stats.

    python munge_sumstats.py \
      --sumstats sumstats.txt \
      --out trait1_munged \
      --merge-alleles w_hm3.snplist

#### 2. LD Scores

Precomputed files are available: \* 1000 Genomes Europeans (baselineLD
v2.2, v1.1) \* UK Biobank, East Asian, African LD scores also available

### 🧪 Key Analyses Performed by LDSC

#### A. SNP Heritability (–h2) Estimation (`ldsc.py`)

Estimates *h*<sup>2</sup> using LD regression:

Output includes:

-   Heritability (on observed and liability scale)
-   Intercept (confounding estimate)
-   Ratio of confounding vs polygenicity

<!-- -->

    python ldsc.py \
      --h2 trait1_munged.sumstats.gz \
      --ref-ld-chr eur_w_ld_chr/ \
      --w-ld-chr eur_w_ld_chr/ \
      --out trait1_h2

#### B. Genetic Correlation (`ldsc.py` with `--rg`)

Tests shared genetic architecture between traits:

-   Compares **two GWAS summary files**
-   Estimates *r*<sub>*g*</sub>: **genetic correlation**
-   Positive *r*<sub>*g*</sub>: traits share common genetic causes

<!-- -->

    python ldsc.py \
      --rg trait1.sumstats.gz,trait2.sumstats.gz \
      --ref-ld-chr eur_w_ld_chr/ \
      --w-ld-chr eur_w_ld_chr/ \
      --out trait1_trait2_rg

#### C. Partitioned Heritability (`ldsc.py` with `--h2-cts`, `--ref-ld-chr`)

Tests contribution of specific annotations:

-   Tests if specific **annotations** (e.g., promoter, enhancer,
    tissue-specific) are enriched for heritability
-   Requires baseline model files (e.g., baselineLD\_v2.2)

<!-- -->

    python ldsc.py \
      --h2 trait1.sumstats.gz \
      --ref-ld-chr baselineLD_v2.2/baselineLD. \
      --w-ld-chr weights_hm3_no_hla/weights. \
      --overlap-annot \
      --frqfile-chr 1000G_frq/1000G.EUR.QC. \
      --out trait1_partitioned

#### D. Stratified LDSC (S-LDSC)

-   Used for cell-type/tissue specific partitioning
-   Can test &gt;100 annotations (Roadmap, GTEx, etc.)

> **Explanation**: LDSC answers “how much is genetics?”, “which tissues
> matter most?”, and “are these two traits genetically similar?”

#### 📊 Interpretation of Results

<table>
<thead>
<tr>
<th style="text-align: left;">Metric</th>
<th style="text-align: left;">Meaning</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: left;"><span
class="math inline"><em>h</em><sup>2</sup></span></td>
<td style="text-align: left;">SNP-based heritability</td>
</tr>
<tr>
<td style="text-align: left;">Intercept</td>
<td style="text-align: left;">Inflation due to confounding (should be
~1.0)</td>
</tr>
<tr>
<td style="text-align: left;">Ratio</td>
<td style="text-align: left;">Proportion of inflation not due to
polygenicity</td>
</tr>
<tr>
<td style="text-align: left;"><span
class="math inline"><em>r</em><sub><em>g</em></sub></span></td>
<td style="text-align: left;">Genetic correlation (between traits)</td>
</tr>
<tr>
<td style="text-align: left;">Enrichment</td>
<td style="text-align: left;">Heritability % / SNP % in an
annotation</td>
</tr>
</tbody>
</table>

#### 🧬 Applications of LDSC

-   **GWAS QC**: Check for confounding
-   **Cross-trait analysis**: Shared etiology (e.g., ASD & depression)
-   **Tissue prioritization**: Use S-LDSC to highlight relevant tissues
-   **Cross-population analysis**: Use ancestry-matched LD scores

#### 🧩 Resources

-   GitHub: <https://github.com/bulik/ldsc>
-   Precomputed LD scores:
    <https://alkesgroup.broadinstitute.org/LDSCORE/>
-   Paper: Bulik-Sullivan et al. 2015, Nature Genetics

#### ✅ Final Tips

-   Always run munge\_sumstats.py to standardize GWAS input.
-   Choose the correct LD score panel for your population.
-   Monitor intercept and ratio to identify confounding.
-   Combine with MAGMA, FUMA, MiXeR, S-LDSC for deep insights.
