# ZEBRA-database-changelog

The molecular causes and mechanisms of neurodegenerative diseases remain poorly understood. A growing number of single-cell studies have implicated various neural, glial, and immune cell subtypes to affect the mammalian central nervous system in many age-related disorders. Integrating this body of transcriptomic evidence into a comprehensive and reproducible framework poses several computational challenges. Here, we introduce ZEBRA, a large single-cell and single-nucleus RNA-seq database. ZEBRA integrates and normalizes gene expression and metadata from 33 studies, encompassing 4.2 million human and mouse brain cells sampled from 39 brain regions. It incorporates samples from patients with neurodegenerative diseases like Alzheimer’s disease, Parkinson’s disease, and Multiple sclerosis, as well as samples from relevant mouse models. We employed scVI, a deep probabilistic auto-encoder model, to integrate the samples and curated both cell and sample metadata for downstream analysis. ZEBRA allows for cell-type and disease-specific markers to be explored and compared between sample conditions and brain regions, a cell composition analysis, and gene-wise feature mappings. Our comprehensive molecular database facilitates the generation of data-driven hypotheses, enhancing our understanding of mammalian brain function during aging and disease. The data sets, along with an interactive database are freely available at https://www.ccb.uni-saarland.de/zebra.

# V1.2 patch
The following changes applied to the latest version of the ZEBRA database:
## ```human_cortex```
- __Blanchard et al 2022__ in further analysis we detected an non-trivial overlap between the Blanchard et al and Mathys 2019 study of ```8``` donor and ```10388``` cells, which has been confirmed by the authors on their [repository](https://github.com/djunamay/apoe4myelin). We re-computed the DEGs and marker genes for the cell types for the current release
## __Hardwick et al__ was removed from the database as the data is duplicated in the ```Sayed et al``` study.

# ```human_noncortex```, ```mouse_cortex```, ```mouse_noncortex```
No changes applied
