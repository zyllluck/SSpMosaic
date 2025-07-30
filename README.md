# SSpMosaic
## Robust integration and annotation of single-cell and spatial multi-omics data using interpretable gene programs 

<p align="center">
<img src="https://github.com/zyllluck/SSpMosaic/blob/main/Workflow.png" width="800" />
</p>
Cellular identity emerges from the dynamic coordination of context-aware gene programs that encode biological functions across molecular layers. To decode this complexity, we present SSpMosaic, a computational framework that establishes metaprograms—higher-order representations of gene programs aligned across datasets—as universal anchors for biological state representation. By leveraging these metaprograms, SSpMosaic ensures consistent and accurate integration across batches, modalities, and species. Critically, SSpMosaic accurately annotates cell types within query datasets, enabling discovery and annotation of novel cell states through metaprogram-based transfer learning. The framework achieves resolution-agnostic deconvolution of spatial transcriptomics, precisely mapping cell-type distributions from spot-level (Visium) to subcellular scales (CosMx/Visium HD). As a paradigm-shifting application, we integrate single-nucleus transcriptomics, chromatin accessibility, and spatial transcriptomics to resolve multi-stage spatial domain dynamics across tissue slices. Finally, SSpMosaic enables reference-free spatial characterization, identifying conserved spatial ecotypes across tissue slices and annotating cellular niches without requiring matched single-cell data.

Installation
------------
You can install the released version of SSpMosaic from Github with the following code.

## Dependencies 
* R version >= 4.0.0.
* Dependent R packages: nnls, Seurat, SeuratObject, WGCNA, methods, Matrix, RcppAnnoy, hdWGCNA, igraph, qlcMatrix, stats, ggplot2, grDevices, uwot, utils, stringr, patchwork, dplyr

``` r
# install devtools if necessary
install.packages('devtools')

# install the SSpMosaic package
devtools::install_github('zyllluck/SSpMosaic')

# load package
library(SSpMosaic)

```




How to use `SSpMosaic`
-------------------
SSpMosaic tutorials are as follows. 

For every analytical task, the SSpMosaic program must first be generated, which comprises two steps: SSpMosaic program generation and the subsequent SSpMosaic program network-propagation step.

For integration tasks, SSpMosaic program generation should be executed on each batch of data individually, followed by running the network-propagation step as a whole; finally, proceed according to the SSpMosaic integration tutorial.

For single-cell annotation tasks，SSpMosaic program generation should be executed on the reference dataset. If the reference dataset has multiple batches,it needs to be run on each batch separately, followed by running the network-propagation step as a whole;finally, proceed according to the SSpMosaic single-cell annotation tutorial.

For deconvolution tasks, SSpMosaic program generation should be executed on the single-cell reference data. If the reference single-cell data has multiple batches,it needs to be run on each batch separately, followed by running the network-propagation step as a whole;finally, proceed according to the SSpMosaic deconvolution tutorial.

## SSpMosaic program

The following two steps should be run in sequence before using the downstream functions of SSpMosaic.

SSpMosaic program generation tutorial is in [generate program](https://zyllluck.github.io/SSpMosaic/program_generation.html)

SSpMosaic program network-propagation tutorial is in [network-propagation](https://zyllluck.github.io/SSpMosaic/network_propagation.html)

## SSpMosaic downstream functions

To use the downstream functions of SSpMosaic, it is necessary to first generate the SSpMosaic program in accordance with the above two steps.

SSpMosaic integration tutorial is in [integration](https://zyllluck.github.io/SSpMosaic/integration_tutorial.html)

SSpMosaic single-cell annotation tutorial is in [sc_annotation](https://zyllluck.github.io/SSpMosaic/sc_annotation_tutorial.html)

SSpMosaic deconvolution tutorial is in [deconvolution](https://zyllluck.github.io/SSpMosaic/spatial_deconvolution_tutorial.html)

Data
------------
All data in tutorials can be downloaded via the following link:
https://drive.google.com/drive/folders/1VDpHAHBjAoKk1u8eR10A4oqMnkeSbT8c?usp=drive_link

Issues
------------
All feedback, bug reports and suggestions are warmly welcomed! Please make sure to raise issues with a detailed and reproducible example and also please provide the output of your sessionInfo() in R! 
