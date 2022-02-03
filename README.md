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




