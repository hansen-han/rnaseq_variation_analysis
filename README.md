# RNAseq Variation Analysis
Investigating variance in RNAseq data from GEO across multiple studies and platforms.



## Data
To download and process expression data for this analysis, I used my `ena_rnaseq_quantification` tool (https://github.com/hansen-han/ena_rnaseq_quantification) and ran the following commmand:

```run_pipeline.py PRJNA433853 PRJNA510012 PRJNA587698 PRJNA613909 PRJNA649786 PRJNA679264 PRJNA774204 PRJNA932798 PRJNA982094 PRJNA997301```

All data processing and analysis can be found in `analysis.Rmd`. 

## Findings

**Data**  
I looked at a total of 575 samples from 10 studies in GEO (GSE110487, GSE123835, GSE139940, GSE147339, GSE155454, GSE161731, GSE186505, GSE224849, GSE234585, GSE237960). I only looked at studies which had measured whole blood bulk RNAseq data from one of the following platforms (Illumina HiSeq 2500, IlluminaHiSeq 3000, Illumina HiSeq 4000, and Illumina NovaSeq 6000). To try and minimize potential sources of variance, I quantified all samples from their FASTQ files using Salmon. 

**Results**
![PCA Plots](pca_plots.png)

**Batch Effects Present Even In Only Healthy Samples**
![PCA Plots](healthy_pca_plots.png)

