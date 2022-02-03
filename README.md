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
| :---: | :---: | :---: | :---: | :---: | :--- |
|Blakeley | 30 | 16862 | 3 | Human blastocyst samples| cite{blakeley2015defining}  | 
|Deng       | 286   | 18884 | 10| Stages of mouse pre-implementation development | cite{deng2014single} | 
|Pollen     | 301   | 23730 | 11| Human cell lines | cite{pollen2014low} |
|Darmanis  | 420 | 21516 | 8 | Human cortical samples | cite{darmanis2015survey} |
|Usoskin    | 622   | 19532 | 4 | Mouse lumbar | cite{usoskin2015unbiased} |
|sim-n    | n   | 20000 | 4 | Splatter synthetically generated data | ref |

