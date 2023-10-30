# RNAseq_plots
A program for producing several graphs for RNAseq data, primarily with EdgeR and ggplot2

RNAseq_plots.R graphs dataframes of interest for RNAseq data mapped by Salmon. Note that a 'mapping' directory containing each sample's Salmon output directory (including the quant.sf file) is required. Included is the directory "RNAseq_plots_DemoData," which contains all needed files to test run this program and observe its outputs. 

RNAseq_plots requires the following packages, which will be installed upon running:
- BiocManager (from bioconductor.org), which contains the following for differential expression analysis:
- tximport
- edgeR
For output data management:
- ggplot2
- ggrepel
- tidyr

Syntax: RNAseq_plots.R <libraries.tsv> <-graph_option> <baseline_name & assessed_name>

RNAseq_plots.R requires 3 user arguments:
     1. <libraries.tsv> must be a 2-column dataframe of library names and categories (tissue types, developmental stages, etc.) seperated by a tab. Don't include headers.
     A minimum of 3 replicates per category is required. Example dataframe from the demo data:
         MG_SK1    skin
         MG_SK2    skin
         MG_SK3    skin
         MG_B1    barbel
         MG_B2    barbel
         MG_B3    barbel
     2. A RNAseq_plots.R graph option (given in <>):
     All graphs <-all>
     Read (CPM) Distribution <-CPMd>
     Multidimensional Scaling <-MDS>
     Biological Coefficient of Variation <-BCV>
     MA plot <-MA>
     Volcano plot of DGE <-Vol>
     
