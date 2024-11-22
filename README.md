# ZEBRA-database-changelog

The molecular causes and mechanisms of neurodegenerative diseases remain poorly understood. A growing number of single-cell studies have implicated various neural, glial, and immune cell subtypes to affect the mammalian central nervous system in many age-related disorders. Integrating this body of transcriptomic evidence into a comprehensive and reproducible framework poses several computational challenges. Here, we introduce ZEBRA, a large single-cell and single-nucleus RNA-seq database. ZEBRA integrates and normalizes gene expression and metadata from 33 studies, encompassing 4.2 million human and mouse brain cells sampled from 39 brain regions. It incorporates samples from patients with neurodegenerative diseases like Alzheimer’s disease, Parkinson’s disease, and Multiple sclerosis, as well as samples from relevant mouse models. We employed scVI, a deep probabilistic auto-encoder model, to integrate the samples and curated both cell and sample metadata for downstream analysis. ZEBRA allows for cell-type and disease-specific markers to be explored and compared between sample conditions and brain regions, a cell composition analysis, and gene-wise feature mappings. Our comprehensive molecular database facilitates the generation of data-driven hypotheses, enhancing our understanding of mammalian brain function during aging and disease. The data sets, along with an interactive database are freely available at https://www.ccb.uni-saarland.de/zebra.

# V1.2 patch
The following changes applied to the latest version of the ZEBRA database. If you used ZEBRA human cortex degs or markers, we recommend rechecking the gene in the database.
For further questions please reach out to the authors or open an issue.
Recomputation of the cell type marker genes, as well as the disease markers based on the listed modifications:
## ```human_cortex```
- __Blanchard et al 2022__ in further analysis we detected an non-trivial overlap between the Blanchard et al and Mathys 2019 study of ```8``` donor and ```10388``` cells, which splits into  ```7498``` AD and ```2890``` CT cells. The duplication has been confirmed by the authors on their [repository](https://github.com/djunamay/apoe4myelin). 
- __Hardwick et al__ was removed from the database as the data is duplicated in the __Sayed et al__ study affecting a total of  ```15656``` control cells.

| Study             | Total Cells | Donor (control/disease) | Contrast                | Disease Cells | Control Cells | Reason |
|-------------------|-------|-------|-------------------------|---------------|---------------|---------------|
| Blanchard et al. 2022 | 10388 | 2/6     | AD vs CT               | 7498          | 2890          | Removed (duplicated in Mathys et al. 2019) |
| Hardwick et al. 2021   |   15656    |    1/0   | 1 |     -          | 15656         | Removed (duplicated in Sayed et al. 2021) |

### Disease DEGs
- The resulting DEGs strongly correlate with the previously reported findings:
![Mixed Sex DEGs](supplemental/mixed_sex_degs.png)
### Cell type marker
![Cell type marker](supplemental/cell_type_marker.png)

## ```human_noncortex```, ```mouse_cortex```, ```mouse_noncortex```
No changes applied
