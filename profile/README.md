![alt text](https://github.com/crisprVerse/.github/blob/main/profile/figs/header.jpg)

# Welcome to the crisprVerse, a Bioconductor ecosystem for designing CRISPR gRNAs

Maintainers: Luke Hoberecht, Jean-Philippe Fortin

Contributors: Aaron Lun, Pirunthan Perampalam

## Installation 

This crisprVerse ecosystem is supported for macOS, Linux and Windows machines.
It was developed and tested on R version 4.2.



### Core packages

Installing the package `crisprVerse` effectively installs all of the core packgages of the crisprVerse ecosystem.
To install `crisprVerse` from Bioconductor, simply enter the following commands in a fresh R session:

```r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
    
BiocManager::install(version='devel') # To make sure this is using the devel branch of Bioconductor
BiocManager::install("crisprVerse")
```


### Optional packages

The optional data package `crisprDesignData` can be installed from GitHub using the following commands:

```r
if (!requireNamespace("devtools", quietly = TRUE))
    install.packages("devtools")
    
devtools::install_github("crisprVerse/crisprDesignData")
```



## Tutorials

A comprehensive list of tutorials can be found [here](https://github.com/crisprVerse/Tutorials). 
Tutorials are often updated to take into account the latest functionalities and changes of the ecosystem. 


## Packages in the crisprVerse

### Bioconductor packages

|Package|BioC-release|BioC-devel|Description
|---|---|---|---|
|[crisprVerse](https://github.com/crisprVerse/crisprVerse)|*Next release*|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprVerse.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprVerse/)|Easily install of the crisprVerse ecosystem|
|[crisprDesign](https://github.com/crisprVerse/crisprDesign)|*Next release*|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprDesign.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprDesign/)|Core gRNA design package across nucleases and applications|
|[crisprBase](https://github.com/crisprVerse/crisprBase)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprBase.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprBase/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprBase.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprBase/)|Base functions and classes for CRISPR gRNA design|
|[crisprBowtie](https://github.com/crisprVerse/crisprBase)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprBowtie.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprBowtie/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprBowtie.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprBowtie/)|Alignment of gRNA spacer sequences using bowtie|
|[crisprBwa](https://github.com/crisprVerse/crisprBwa)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprBwa.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprBwa/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprBwa.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprBwa/)|Alignment of gRNA spacer sequences using BWA|
|[crisprScore](https://github.com/crisprVerse/crisprScore)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/crisprScore.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/crisprScore/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/crisprScore.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/crisprScore/)|On-target and off-target scoring for CRISPR gRNAs|
|[crisprScoreData](https://github.com/crisprVerse/crisprScoreData)|[![Release OK](https://bioconductor.org/shields/build/release/data-experiment/crisprScoreData.svg)](http://bioconductor.org/checkResults/release/data-experiment-LATEST/crisprScoreData/)|[![Devel OK](https://bioconductor.org/shields/build/devel/data-experiment/crisprScoreData.svg)](http://bioconductor.org/checkResults/devel/data-experiment-LATEST/crisprScoreData/)|Pre-trained models for the crisprScore package|
|[Rbwa](https://github.com/crisprVerse/Rbwa)|[![Release OK](https://bioconductor.org/shields/build/release/bioc/Rbwa.svg)](http://bioconductor.org/checkResults/release/bioc-LATEST/Rbwa/)|[![Devel OK](https://bioconductor.org/shields/build/devel/bioc/Rbwa.svg)](http://bioconductor.org/checkResults/devel/bioc-LATEST/Rbwa/)|R wrapper for BWA-backtrack and BWA-MEM aligners|
|[crisprViz](https://github.com/crisprVerse/crisprViz)|*Next release*|*Under review*|Visualization of CRISPR gRNAs using genomic tracks |

### GitHub packages

|Package|Devel|Description
|---|---|---|
|[crisprDesignData](https://github.com/crisprVerse/crisprDesignData)||Useful data for the crisprVerse ecosystem|


## Citation

If using our software, please cite our bioRxiv preprint[A comprehensive Bioconductor ecosystem for the design of CRISPR guide RNAs across nucleases and technologies](https://www.biorxiv.org/content/10.1101/2022.04.21.488824v2). Here's a bibtex citation:

```
@article{Hoberecht2022,
	author = {Hoberecht, Luke and Perampalam, Pirunthan and Lun, Aaron and Fortin, Jean-Philippe},
	title = {A comprehensive Bioconductor ecosystem for the design of CRISPR guide RNAs across nucleases and technologies},
	year = {2022},
	doi = {10.1101/2022.04.21.488824},
	URL = {https://www.biorxiv.org/content/early/2022/04/28/2022.04.21.488824},
	eprint = {https://www.biorxiv.org/content/early/2022/04/28/2022.04.21.488824.full.pdf},
	journal = {bioRxiv}
}

```

## License

The ecosystem is released under the MIT license. Genentech owns the copyright. 
