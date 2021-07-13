# Applying copy number signature analysis in multiple myeloma

Kylee Maclachlan, maclachk@mskcc.org

The following analysis workflow is a companion to the manuscript “Copy number signatures predict chromothripsis and clinical outcomes in newly diagnosed multiple myeloma” by Maclachlan et al.

Chromothripsis is a complex chromosomal shattering event associated with random rejoining, and is emerging as strong, independent adverse prognostic factor across multiple malignancies. Reliable detection of chromothripsis requires whole genome sequencing (WGS) and the integration of both structural variants (SVs) and copy number (CN) data.

Copy number (CN) signature analysis was described by Macintyre et al in Nature Genetics 2018 as a BRCAness surrogate. It takes WGS data and assesses 6 key copy number features. The optimal number of categories in each feature, which may differ between cancer types, is defined by a mixed effects model. De novo signature extraction is performed by the hierarchical Dirichlet process, producing a dataframe detailing the relative proportional contribution from each CN signature.

- **Supplementary Data 1** applies CN signature analysis to multiple myeloma (MM).<br /> 
- **Supplementary Data 2** applies SV signature analysis to MM. Using the size, type and clustering of SVs as input, de novo signature extraction is performed by the hierarchical Dirichlet process, producing a data frame detailing the relative proportional contribution from each SV signature.<br /> 
- **Supplementary Data 3** demonstrates how genomic signatures can be used to predict the presence of chromothripsis in MM, defined by manual curation of CN and SV data. Chromothripsis is predicted by estimating the average area-under-the-curve from receiver operating characteristic curves using 10-fold cross validation.<br /> 
- **Supplementary Data 4** demonstrates how CN signatures are more accurate for the prediction of chromothripsis than an alternate CN analysis tool. The genomic scar score (calculated using the R package scarHRD) sums 3 features (loss-of-heterozygosity, telomeric allelic imbalance, and number of large-scale transitions) to produce a final score. We estimated the average area-under-the-curve from receiver operating characteristic curves using 10-fold cross validation for each method, then calculated the difference in average AUC between the methods. 
