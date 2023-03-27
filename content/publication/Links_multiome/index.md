---
Abstract: -<br> Epigenomic profiling, including ATACseq, is one of the main tools used to define enhancers. Because enhancers are overwhelmingly cell-type specific, inference of their activity is greatly limited in complex tissues. Multiomic assays that probe in the same nucleus both the open chromatin landscape and gene expression levels enable the study of correlations (links) between these two modalities. Current best practices to infer the regulatory effect of candidate cis-regulatory elements (cCREs) in multiomic data involve removing biases associated with GC content by generating null distributions of matched ATACseq peaks drawn from different chromosomes. This strategy has been broadly adopted by popular single-nucleus multiomic workflows such as Signac. Here, we uncovered limitations and confounders of this approach. We found a strong loss of power to detect a regulatory effect for cCREs with high read counts in the dominant cell-type. We showed that this is largely due to cell-type-specific trans-ATACseq peak correlations creating bimodal null distributions. We tested alternative models and concluded that physical distance and/or the raw Pearson correlation coefficients are the best predictors for peak-gene links when compared to predictions from Epimap (e.g. CD14 area under the curve [AUC] = 0.51 with the method implemented in Signac vs. 0.71 with the Pearson correlation coefficients) or validation by CRISPR perturbations (AUC = 0.63 vs. 0.73).<br>

# author_notes:
# - Equal contribution
# - Equal contribution
authors:
- Francis JA Leblanc
- Guillaume Lettre

date: "2023-03-9"
doi: "https://doi.org/10.1038/s41598-023-31040-w"
featured: true
# image:
#   caption: ''
#   focal_point: ""
#   preview_only: false
projects: []
publication: '*Major cell-types in multiomic single-nucleus datasets impact statistical modeling of links between regulatory sequences and target genes*'
publication_short: ""
publication_types:
- "2"
publishDate: "2023-03-27T15:51:12-04:00"
tags:
- Single cell multiome
- RNAseq
- ATACseq
- cCRE
title: Major cell-types in multiomic single-nucleus datasets impact statistical modeling of links between regulatory sequences and target genes
url_code: ""
url_dataset: ""
url_pdf: ""
url_poster: ""
url_project: ""
url_slides: ""
url_source: "https://www.nature.com/articles/s41598-023-31040-w"
url_video: ""
---


