# Introduction
This repository contains R scripts used for our publication "Multiplexed functional genomic analysis of somatic 5’ untranslated region mutations across the spectrum of human prostate cancer "


## References
1) R Core Team (2018). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. URL https://www.R-project.org/.
2) Fraser, M., Sabelnykova, V., Yamaguchi, T. et al. Genomic hallmarks of localized, non-indolent prostate cancer. Nature 541, 359–364 (2017). https://doi.org/10.1038/nature20788

## Tools used for analysis 

All our analysis is done in R using the following  R/Biocondcutor packages.

1) [ggplot2](https://ggplot2.tidyverse.org/) for making most of the plots in our paper. 
2) [xtail](https://github.com/xryanglab/xtail) and [DESeq2](https://www.bioconductor.org/packages/release/bioc/html/DESeq2.html) for finding differentially expressed genes.
3) [riboSeqR](https://bioconductor.org/packages/release/bioc/html/riboSeqR.html) for finding triplate periodicity in samples.
4) [GenomicFeatures](https://bioconductor.org/packages/release/data/annotation/html/GenomicFeatures.html) , [BSgenome.Hsapiens.UCSC.hg19](http://bioconductor.org/packages/release/data/annotation/html/BSgenome.Hsapiens.UCSC.hg19.html) and [TxDb.Hsapiens.UCSC.hg19.knownGene](https://bioconductor.org/packages/release/data/annotation/html/TxDb.Hsapiens.UCSC.hg19.knownGene.html) for using annotation databases from UCSC
 
To ensure smooth execution of code in this repository, please install the 
following packages 

```{r eval=FALSE}
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(c("ggplot2", "riboSeqR", "DESeq2", 
      "GenomicFeatures", 
      "BSgenome.Hsapiens.UCSC.hg19", 
      "TxDb.Hsapiens.UCSC.hg19.knownGene"))

# directly install xtail from github
install.packages("devtools")
library("devtools")
install_github("xryanglab/xtail")
```
