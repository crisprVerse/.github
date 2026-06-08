
# Welcome to the crisprVerse, a Bioconductor ecosystem for designing CRISPR gRNAs

The crisprVerse is a Bioconductor ecosystem of R packages that enables efficient gRNA design and annotation for a multitude of CRISPR technologies, including CRISPR knockout (CRISPRko), CRISPR activation (CRISPRa), CRISPR interference (CRISPRi), CRISPR base editing (CRISPRbe), and CRISPR knockdown (CRISPRkd). The core package, crisprDesign, offers a comprehensive, user-friendly, and unified interface to add on- and off-target annotations via several alignment methods, rich gene and SNP annotations, and a dozen on- and off-target activity scores. These functionalities are enabled for any RNA- or DNA-targeting nucleases, including Cas9, Cas12, Cas13, and Csm. Both single and paired gRNA designs are enabled. 

For an overview of the ecosystem functionalities, see the [crisprDesign page](https://github.com/crisprVerse/crisprDesign).
For detailed examples, see our [tutorials](https://github.com/crisprVerse/Tutorials).


- Project lead: Jean-Philippe Fortin
- Maintainers: Luke Hoberecht, Jean-Philippe Fortin
- Contributors: Aaron Lun, Pirunthan Perampalam

## Software Adoption and Impact

The following open-source projects directly incorporate components of the crisprVerse ecosystem:

- [CRISPRware](https://github.com/ericmalekos/crisprware) — Context-aware gRNA library design platform.
- [CRISPR-BEasy](https://github.com/CERC-Genomic-Medicine/CRISPR-BEasy) — Web platform for designing sgRNA tiling libraries for CRISPR base-editing screens.
- [PrEditR](https://github.com/fvasquezcastro/preditr/tree/main) — Analysis framework for prime-editing experiments.  
- [crisprCHOPOFF](https://github.com/JokingHero/crisprCHOPOFF) — R wrapper for CHOPOFF, a CRISPR OFF target search algorithm
- [HemTools](https://github.com/YichaoOU/HemTools) — A collection of NGS pipelines and bioinformatic analyses
- [Digenome Detect](https://github.com/nihsmtgt/Digenome-Detect) — Digenome-seq analysis tool
- [snakemake-crispr-guides](https://github.com/MPUSP/snakemake-crispr-guides) — Guide design workflow developed by the Max Planck Unit for the Science of Pathogens.

### Selected Publications

- Template-driven scaffolding of SCF-FBXO42 regulates PP2A degradation ([Nature](https://www.nature.com/articles/s41586-026-10368-z))
- Multiplexed, image-based pooled screens in primary cells and tissues with PerturbView ([Nature Biotechnology](https://www.nature.com/articles/s41587-024-02391-0))
- Engineered CRISPR-Cas12a for higher-order combinatorial chromatin perturbations ([Nature Biotechnology](https://www.nature.com/articles/s41587-024-02224-0))
- Microglia-mediated protection against Alzheimer's disease pathology and detrimental effects in white matter revealed by Ptpn6 deletion ([Neuron](https://www.cell.com/neuron/abstract/S0896-6273(26)00128-5?_returnURL=https%3A%2F%2Flinkinghub.elsevier.com%2Fretrieve%2Fpii%2FS0896627326001285%3Fshowall%3Dtrue))
- Rational design of potent small-molecule SMARCA2/A4 degraders acting via the recruitment of FBXO22 ([Nature Communications](https://www.nature.com/articles/s41467-025-64669-4))
- A CRISPR/Cas9 screen reveals proteins at the endosome-Golgi interface that modulate cellular anti-sense oligonucleotide activity ([Nature Communications](https://www.nature.com/articles/s41467-025-61039-y))
- Inhibition of GPX4 enhances CDK4/6 inhibitor and endocrine therapy activity in breast cancer ([Nature Communications](https://www.nature.com/articles/s41467-024-53837-7))
- Advancing the genetic engineering toolbox by combining AsCas12a knock-in mice with ultra-compact screening ([Nature Communications](https://www.nature.com/articles/s41467-025-56282-2))
- Accelerated drug-resistant variant discovery with an enhanced, scalable mutagenic base editor platform ([Cell Reports](https://www.cell.com/cell-reports/fulltext/S2211-1247(24)00641-7))
- CRISPR activation screens identify the SWI/SNF ATPases as suppressors of ferroptosis ([Cell Reports](https://www.cell.com/cell-reports/fulltext/S2211-1247(24)00673-9))
- Seed sequences mediate off-target activity in the CRISPR-interference system ([Cell Genomics](https://www.cell.com/cell-genomics/fulltext/S2666-979X(24)00322-7))
- An unbiased whole-genome open reading frame overexpression screen identifies B3GALT2, a novel inducer of cellular ASO activity ([Molecular Therapy Nucleid Acids](https://www.cell.com/molecular-therapy-family/nucleic-acids/fulltext/S2162-2531(25)00320-8))
- Scalable multimodal mapping of macrophage regulatory architecture by integrating optical and transcriptomic pooled screens ([bioRxiv](https://www.biorxiv.org/content/10.64898/2026.05.27.728345v1))
- A novel, high-density CRISPR activation platform for mapping cancer dependencies and resistance pathways ex vivo and in vivo ([bioRxiv](https://www.biorxiv.org/content/10.1101/2025.07.22.666069v1))

## Installation 

### Requirements

The crisprVerse is supported for macOS, Linux and Windows machines.
It requires R version >=4.4.
Some of the third-party functionalities are not
available for Windows machines (BWA alignment, and some of the scoring 
functions). To download and install R, see 
the [R-project website](https://www.r-project.org/).

### Bioconductor versions

The crisprVerse is embedded within the Bioconductor ecosystem,
therefore has 2 concurrent branches: `release` and
`devel`. Currently (July 2024), the release branch is `3.19`, and the
devel branch is `3.20`. Both branches requires R version 4.4 or higher. 
Release versions are created twice a year. See
the [Bioconductor install page](https://www.bioconductor.org/install/)
for more information regarding Bioconductor versions and to get an overview of how to install packages. 

### Installing the core crisprVerse packages

To install the packages from the release branch, type in the following commands in an R session:

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install(version="release") 
BiocManager::install("crisprVerse")
```

To install the packages from the development branch, which is up to date with the lastest pushes 
to the GitHub repos, type in the following commands in an R session:

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install(version="devel") 
BiocManager::install("crisprVerse")
```



### Optional packages

The optional data package `crisprDesignData` can be installed from GitHub using the following commands:

```r
if (!requireNamespace("devtools", quietly = TRUE))
    install.packages("devtools")
    
devtools::install_github("crisprVerse/crisprDesignData")
```

For maxOS and Linux users, the 
[crisprBwa](https://github.com/crisprVerse/crisprBwa) can be installed
from Bioconductor using the following:

```{r, eval=FALSE}
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("crisprBwa")
```




## Docker images

We are providing ready-to-use Docker images that can be downloaded from the [Docker hub](https://hub.docker.com/r/fortin946/crisprverse).
See our [Docker page](https://github.com/crisprVerse/Docker) for more information. 

## Tutorials

A comprehensive list of tutorials can be found [here](https://github.com/crisprVerse/Tutorials). 
Tutorials are often updated to take into account the latest functionalities and changes of the ecosystem. 


## Packages in the crisprVerse

### Bioconductor packages

|Package|BioC-release|BioC-devel|Description
|---|---|---|---|
|[crisprVerse](https://github.com/crisprVerse/crisprVerse)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprVerse.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprVerse/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprVerse.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprVerse/)|Easily install of the crisprVerse ecosystem|
|[crisprDesign](https://github.com/crisprVerse/crisprDesign)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprDesign.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprDesign/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprDesign.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprDesign/)|Core gRNA design package across nucleases and applications|
|[crisprBase](https://github.com/crisprVerse/crisprBase)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprBase.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprBase/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprBase.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprBase/)|Base functions and classes for CRISPR gRNA design|
|[crisprBowtie](https://github.com/crisprVerse/crisprBowtie)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprBowtie.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprBowtie/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprBowtie.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprBowtie/)|Alignment of gRNA spacer sequences using bowtie|
|[crisprBwa](https://github.com/crisprVerse/crisprBwa)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprBwa.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprBwa/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprBwa.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprBwa/)|Alignment of gRNA spacer sequences using BWA|
|[crisprScore](https://github.com/crisprVerse/crisprScore)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprScore.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprScore/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprScore.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprScore/)|On-target and off-target scoring for CRISPR gRNAs|
|[crisprScoreData](https://github.com/crisprVerse/crisprScoreData)|[![Release OK](https://bioconductor.org/shields/build/release/data-experiment/crisprScoreData.svg)](http://bioconductor.org/checkResults/release/data-experiment-LATEST/crisprScoreData/)|[![Devel OK](https://bioconductor.org/shields/build/devel/data-experiment/crisprScoreData.svg)](http://bioconductor.org/checkResults/devel/data-experiment-LATEST/crisprScoreData/)|Pre-trained models for the crisprScore package|
|[crisprViz](https://github.com/crisprVerse/crisprViz)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprViz.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprViz/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprViz.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprViz/)|Visualization of CRISPR gRNAs using genomic tracks |
|[crisprShiny](https://github.com/crisprVerse/crisprShiny)| [![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprShiny.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprShiny/)| [![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprShiny.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprShiny/)| Shiny interface for CRISPR gRNAs 
|[screenCounter](https://github.com/crisprVerse/screenCounter)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/screenCounter.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/screenCounter/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/screenCounter.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/screenCounter/)| gRNA barcode sequencing reads alignment tool |
|[Rbwa](https://github.com/crisprVerse/Rbwa)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/Rbwa.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/Rbwa/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/Rbwa.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/Rbwa/)|R wrapper for BWA-backtrack and BWA-MEM aligners|


### GitHub packages

|Package|Devel|Description
|---|---|---|
|[crisprDesignData](https://github.com/crisprVerse/crisprDesignData)|[![R-CMD-check](https://github.com/crisprVerse/crisprDesignData/actions/workflows/check-standard.yaml/badge.svg)](https://github.com/crisprVerse/crisprDesignData/actions/workflows/check-standard.yaml)|Useful data for the crisprVerse ecosystem|


## Citation

If using our software, please cite our Nature Communications paper [A comprehensive Bioconductor ecosystem for the design of CRISPR guide RNAs across nucleases and technologies](https://www.nature.com/articles/s41467-022-34320-7). Here's a bibtex citation:

```
@article{hoberecht2022comprehensive,
  title={A comprehensive Bioconductor ecosystem for the design of CRISPR guide RNAs across nucleases and technologies},
  author={Hoberecht, Luke and Perampalam, Pirunthan and Lun, Aaron and Fortin, Jean-Philippe},
  journal={Nature Communications},
  volume={13},
  number={1},
  pages={6568},
  year={2022},
  publisher={Nature Publishing Group UK London}
}

```

## License

The ecosystem is released under the MIT license. Genentech Inc. owns the copyright. 
