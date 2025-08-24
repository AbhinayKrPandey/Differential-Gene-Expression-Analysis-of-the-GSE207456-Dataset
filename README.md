# Differential-Gene-Expression-Analysis-of-the-GSE207456-Dataset
This project is a bioinformatics mini-project that performs a Differential Gene Expression (DGE) analysis on the publicly available GSE207456 dataset from the NCBI GEO repository. The primary goal of this project is to identify significant gene expression changes in human macrophages in response to Mycobacterium abscessus infection, and to demonstrate a complete DGE analysis workflow using R.

The original dataset, titled 'Human pluripotent stem cell-derived macrophages host Mycobacterium abscessus infection,' provides valuable insights into the host cell response over time.

## Project Objectives
### Workflow Implementation: To build a robust DGE analysis pipeline using the R programming language.

- Gene Discovery: To identify genes that are significantly upregulated or downregulated in infected human macrophages.

- Statistical Stringency: To apply a stringent statistical approach using both FDR cutoff and Log Fold Change (LFC) thresholds to filter for the most biologically meaningful genes.

- Data Visualization: To use various plots and visualizations to interpret and present the results of the DGE analysis effectively.

## Methodology
The project's methodology is centered on the following key steps and software packages:

## Software and Packages
- R: The primary programming language used for statistical computing and data visualization.

- BiocManager: Used to install and manage R packages from the Bioconductor repository.

- DESeq2: The core R package for performing DGE analysis on count data. It handles normalization and statistical testing to identify significant genes.

- gplots and ggplot2: Used for creating high-quality visualizations of the results.

## Key Analysis Steps
- Data Retrieval: The dataset was sourced from the NCBI GEO public repository.

- Normalization: Raw count data was normalized to account for differences in library size between samples.

- Statistical Testing: DESeq2 was used to perform hypothesis tests for each gene to determine if its expression change was statistically significant.

- Stringent Filtering: An initial False Discovery Rate (FDR) cutoff of 10% was applied, followed by an additional Log Fold Change (LFC) threshold of 1 to narrow down the list of genes with the most pronounced expression changes.

- Data Visualization: The results were visualized using standard bioinformatics plots:

- MA-plots: To visualize the relationship between gene expression fold change and mean expression.

- Heatmaps: To show the expression levels of the top differentially expressed genes across different samples.

- Volcano Plots: To provide a global view of statistical significance versus magnitude of expression change.

- p-value Histograms: To assess the overall behavior of the statistical test.

## Key Findings & Results
- Filtered Gene List: Initially, 3,511 differentially expressed genes were identified using only the FDR cutoff. The additional LFC threshold reduced this list to 170 genes, effectively highlighting the most significant changes.

- Visual Insights: The visualizations (Heatmaps, Volcano Plots) confirmed that applying the LFC threshold drastically reduced the number of significant genes, providing a clearer and more focused view of the data. The Heatmaps revealed that the most significant expression changes occurred in the 24-hour and 48-hour post-infection samples.

- Bimodal Distribution: The p-value histogram showed a bimodal distribution, which is a key indicator of a successful DGE analysis with a true signal.

## Conclusions
This project successfully demonstrates an effective DGE analysis pipeline in R, capable of handling a complex, real-world dataset. By applying both FDR and LFC cutoffs, the analysis was refined to identify a concise list of potentially important genes. The use of multiple visualizations was crucial for interpreting the results and identifying key trends, providing a solid foundation for further functional analysis into the host-pathogen interaction.
