# ZEBRA-database-changelog

## Abstract
The molecular causes and mechanisms of neurodegenerative diseases remain poorly understood. A growing number of single-cell studies have implicated various neural, glial, and immune cell subtypes to affect the mammalian central nervous system in many age-related disorders. Integrating this body of transcriptomic evidence into a comprehensive and reproducible framework poses several computational challenges. Here, we introduce ZEBRA, a large single-cell and single-nucleus RNA-seq database. ZEBRA integrates and normalizes gene expression and metadata from 33 studies, encompassing 4.2 million human and mouse brain cells sampled from 39 brain regions. It incorporates samples from patients with neurodegenerative diseases like Alzheimer’s disease, Parkinson’s disease, and Multiple sclerosis, as well as samples from relevant mouse models. We employed scVI, a deep probabilistic auto-encoder model, to integrate the samples and curated both cell and sample metadata for downstream analysis. ZEBRA allows for cell-type and disease-specific markers to be explored and compared between sample conditions and brain regions, a cell composition analysis, and gene-wise feature mappings. Our comprehensive molecular database facilitates the generation of data-driven hypotheses, enhancing our understanding of mammalian brain function during aging and disease. The data sets, along with an interactive database are freely available at https://www.ccb.uni-saarland.de/zebra.
## Reference
Matthias Flotho, Jérémy Amand, Pascal Hirsch, Friederike Grandke, Tony Wyss-Coray, Andreas Keller, Fabian Kern, ZEBRA: a hierarchically integrated gene expression atlas of the murine and human brain at single-cell resolution, Nucleic Acids Research, Volume 52, Issue D1, 5 January 2024, Pages D1089–D1096, https://doi.org/10.1093/nar/gkad990

## Contact
For further questions please reach out to the authors or open a GitHub issue.

# V1.2 patch
The following changes were applied to the latest version of the ZEBRA database.

If you used ZEBRA ```human cortex``` DEGs or markers, __we strongly recommend reviewing the genes in the updated database.__

The cell type marker genes as well as the disease markers based were recomputed for each dataset as follows:
## ```human_noncortex```, ```mouse_cortex```, ```mouse_noncortex```
No changes applied.
## ```human_cortex```
- __Blanchard et al. 2022:__ During further analysis we detected a non-trivial overlap between the _Blanchard_ and _Mathys 2019_ studies of ```8``` donors and ```10388``` cells, which accounts for ```7498``` AD and ```2890``` CT cells. The duplication issue has been confirmed by the authors in their [repository](https://github.com/djunamay/apoe4myelin) and thus the detected overlaps were removed from the ZEBRA database.
- __Hardwick et al. 2021:__ Was removed from the database as the count data is duplicated in the raw data records of the _Sayed 2021_ study, affecting a total of ```15656``` control cells.

| Study             | Total cells removed | Donors (control/disease) | Contrast                | Disease Cells | Control Cells | Status |
|-------------------|-------|-------|-------------------------|---------------|---------------|---------------|
| Blanchard et al. 2022 | 10388 | 2/6     | AD vs CT               | 7498          | 2890          | Removed (duplicated in _Mathys et al. 2019_) |
| Hardwick et al. 2021   |   15656    |    1/0   | 1 |     -          | 15656         | Removed (duplicated in the original raw object from _Sayed et al. 2021_ but __not__ in the processed object used to generate results)|

### Disease DEGs
- The resulting DEGs strongly correlate with the previously reported findings:

![Mixed Sex DEGs](supplemental/mixed_sex_degs.png)
### Cell type markers
![Cell type markers](supplemental/cell_type_marker.png)
