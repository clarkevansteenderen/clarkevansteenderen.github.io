---
title: "SPEDE-sampler"
excerpt: "An R Shiny App that assesses the effects of methodological choice (e.g. tree prior, rate distribution, or clock rate) and sampling effects on the GMYC model for species delimitation."
collection: portfolio
---

This R Shiny App offers an analysis pipeline for assessing how sampling effects and paramater choices can affect the results of a Generalised Mixed Yule Coalescent (GMYC) analysis. The pipeline begins with the uploading of an aligned FASTA file, where a chosen percentage of the dataset is randomly resampled n times without replacement. Resampling can be done with guidance from user-predefined groups (e.g. morphospecies assignments), such that at least one representative sequence per group is present in the final selection. BEAST .XML files are then generated for each resampled FASTA alignment, where the user can apply desired configuration settings. Each .XML file is run in BEAST, and the results fed into TreeAnnotator. Maximum clade credibility trees are then used as input for GMYC analyses (single or multiple threshold). If the user has predefined grouping data for their samples, this can be uploaded as an Excel .csv file. These predefined groups are compared to the groups estimated by the GMYC analysis, and percentage matches calculated.
