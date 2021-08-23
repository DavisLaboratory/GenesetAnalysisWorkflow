# Gene-set enrichment analysis workshop

## Overview

This workshop will focus on performing gene-set enrichment analysis of transcriptomic data and visualising the results of enrichment analysis. We will perform single-sample gene-set enrichment using methods in the `singscore` package to explore molecular phenotypes in individual samples. Following this, we will perform gene-set enrichment analysis using tools from the `limma` and `edgeR` packages. Finally, we will demonstrate a graph-based approach to visualise, summarise and interpret resutls of gene-set enrichment analysis.

The workshop will be organised into two broad sections:
* Molecular phenotyping of individual samples
* Identifying and visualising higher-order phenotypes

Detailed material can be found [here](https://davislaboratory.github.io/GenesetAnalysisWorkflow/articles/workflow_singscore_vissE.html).

## Pre-requisites 

The course is aimed at PhD students, Master's students, and third & fourth year undergraduate students. 
Some basic R knowledge is assumed - this is not an introduction to R course. 
If you are not familiar with the R statistical programming language it is compulsory that you work through an introductory R course before you attend this workshop.

## _R_ packages used

The following key R packages will be used: 

* `singscore`
* `vissE`
* `msigdb`
* `emtdata`
* `edgeR`
* `limma`
* `GSEABase`
* `igraph`

## Time outline

| Activity                                                        | Time |
|-----------------------------------------------------------------|------|
| Introduction & setup                                            | 10m  |
| Part 1. Molecular phenotyping of individual samples             | 45m  |
| Part 2. Identifying and visualising higher-order phenotypes     | 45m  |
| Q & A                                                           | 10m  |


## Workshop goals and objectives

### Learning goals

 - Learn how to perform gene-set testing in R.
 - Understand the results of gene-set enrichment analysis.
 - Understand the importance of visualisation in bioinformatics and computational biology.

### Learning objectives

 - Perform a gene-set enrichment analysis and interpret the results.
 - Apply vissE to identify higher-order phenotypes and to visualise the results of any gene-set enrichment analysis.

## Workshop package installation 

### Guide

This is necessary in order to reproduce the code shown in the workshop. 
The workshop is designed for R `4.1` and can be installed using one of the two ways below.

### Via Docker image

If you're familiar with [Docker](https://docs.docker.com/get-docker/) you could use the Docker image which has all the software pre-configured to the correct versions.

```
docker run -e -p 8787:8787 bhuvad/genesetanalysisworkflow:latest
```

Once running, navigate to <http://localhost:8787/> and then login with
`Username:rstudio` and `Password:rstudio`.

You should see the Rmarkdown file with all the workshop code which you can run.

### Via GitHub

Alternatively, you could install the workshop using the commands below in R `4.1`.

```
install.packages('remotes')

# Install workshop package
remotes::install_github("DavisLaboratory/GenesetAnalysisWorkflow", build_vignettes = TRUE)

# To view vignettes
library(GenesetAnalysisWorkflow)
browseVignettes("GenesetAnalysisWorkflow")
```
