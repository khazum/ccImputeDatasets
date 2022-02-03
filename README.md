## ccImputeDatasets
Processed single cell RNA sequencing datasets used to evaluate the performance of the ccImpute algorithm. 

## Summary of Datasets & Usage
Any of scRNA-seq datasets listed in the table below can be read-in into R as follows:
```r
library(SummarizedExperiment)

# Load dataset_name.rds in local_file_dir to SummarizedExperiment object named sce
sce <- readRDS(file = "local_file_dir/dataset_name.rds")
  
# Access the counts (row/normalized depending on the dataset)
X <- assays(sce)$counts 
  
# Access log normalized counts
X_log <- assays(sce)$logcounts
  
# Access labels (some datasets have cell_type2 with finer cell type definitions)
labels <- colData(sce)$cell_type1

```

| Filename | Samples | Features | k | Cell origin | Reference |
| :--- | :--- | :--- | :--- | :--- | :--- |
|Blakeley | 30 | 16862 | 3 | Blakeley P, Fogarty NM, del Valle I, Wamaitha SE, Hu TX, Elder K, Snell P, Christie L, Robson P, Niakan KK. Defining the three cell lineages of the human blastocyst by single-cell RNA-seq. Development. 2015 Sep 15;142(18):3151-65. doi: 10.1242/dev.123547. Epub 2015 Aug 20. Erratum in: Development. 2015 Oct 15;142(20):3613. PMID: 26293300; PMCID: PMC4582176.  | 
|Deng       | 286   | 18884 | 10| Stages of mouse pre-implementation development | Deng, Qiaolin, et al. "Single-cell RNA-seq reveals dynamic, random monoallelic gene expression in mammalian cells." Science 343.6167 (2014): 193-196. | 
|Pollen     | 301   | 23730 | 11| Human cell lines | Pollen, Alex A., et al. "Low-coverage single-cell mRNA sequencing reveals cellular heterogeneity and activated signaling pathways in developing cerebral cortex." Nature biotechnology 32.10 (2014): 1053-1058. |
|Darmanis  | 420 | 21516 | 8 | Human cortical samples | Darmanis, Spyros, et al. "A survey of human brain transcriptome diversity at the single cell level." Proceedings of the National Academy of Sciences 112.23 (2015): 7285-7290. |
|Usoskin    | 622   | 19532 | 4 | Mouse lumbar | Usoskin, Dmitry, et al. "Unbiased classification of sensory neuron types by large-scale single-cell RNA sequencing." Nature neuroscience 18.1 (2015): 145-153. |
|sim-n    | n   | 20000 | 4 | Splatter synthetically generated data | Zappia, Luke, Belinda Phipson, and Alicia Oshlack. "Splatter: simulation of single-cell RNA sequencing data." Genome biology 18.1 (2017): 1-15. |

