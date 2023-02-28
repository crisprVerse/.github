![alt text](https://github.com/crisprVerse/.github/blob/main/profile/figs/header.jpg)


# Welcome to the crisprVerse, a Bioconductor ecosystem for designing CRISPR gRNAs

The crisprVerse is a Bioconductor ecosystem of R packages that enables efficient gRNA design and annotation for a multitude of CRISPR technologies, including CRISPR knockout (CRISPRko), CRISPR activation (CRISPRa), CRISPR interference (CRISPRi), CRISPR base editing (CRISPRbe), and CRISPR knockdown (CRISPRkd). The core package, crisprDesign, offers a comprehensive, user-friendly, and unified interface to add on- and off-target annotations via several alignment methods, rich gene and SNP annotations, and a dozen on- and off-target activity scores. These functionalities are enabled for any RNA- or DNA-targeting nucleases, including Cas9, Cas12, and Cas13. Both single and paired gRNA designs are enabled. 

For an overview of the ecosystem functionalities, see the [crisprDesign page](https://github.com/crisprVerse/crisprDesign).
For detailed examples, see our [tutorials](https://github.com/crisprVerse/Tutorials).


- Project lead: Jean-Philippe Fortin
- Maintainers: Luke Hoberecht, Jean-Philippe Fortin
- Contributors: Aaron Lun, Pirunthan Perampalam

## Installation 

### Requirements

The crisprVerse is supported for macOS, Linux and Windows machines.
It requires R version >=4.2.1 for release, and R version >=4.3 for devel.
Some of the third-party functionalities are not
available for Windows machines (BWA alignment, and some of the scoring 
functions). To download and install R, see 
the [R-project website](https://www.r-project.org/).

### Bioconductor versions

The Bioconductor project has 2 concurrent branches: `release` and
`devel`. Currently (November 2022), the release branch is `3.16`, and the
devel branch is `3.17`. The release branch requires R version 4.2 or higher, and the devel branch requires R version 4.3 or higher.
Release versions are created twice a year. See
the [Bioconductor install page](https://www.bioconductor.org/install/)
for more information regarding Bioconductor versions.

### Installing the core crisprVerse packages

Type in the following commands in an R session to install the core
crisprVerse packages from the Bioconductor devel branch:

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

#BiocManager::install(version="devel") To use the devel branch instead
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

#BiocManager::install(version="devel") To use the devel branch instead
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
|[Rbwa](https://github.com/crisprVerse/Rbwa)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/Rbwa.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/Rbwa/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/Rbwa.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/Rbwa/)|R wrapper for BWA-backtrack and BWA-MEM aligners|
|[crisprViz](https://github.com/crisprVerse/crisprViz)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprViz.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprViz/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprViz.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprViz/)|Visualization of CRISPR gRNAs using genomic tracks |


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
