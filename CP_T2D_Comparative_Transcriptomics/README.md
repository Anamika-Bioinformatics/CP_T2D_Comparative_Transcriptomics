# Comparative Transcriptomic Analysis of Chronic Pancreatitis and Type 2 Diabetes

## Overview
This project performs a comparative transcriptomic analysis of human pancreatic tissue
from Chronic Pancreatitis (CP) patients and pancreatic islets from Type 2 Diabetes (T2D) patients.
Publicly available microarray datasets were analyzed to identify disease-specific and
shared transcriptional patterns.

The analysis highlights contrasting transcriptomic architectures:
- **Chronic Pancreatitis** shows extensive bidirectional transcriptomic remodeling.
- **Type 2 Diabetes** exhibits a focused and predominantly downregulated transcriptional response.

## Datasets Used
- **GSE143754**: Chronic Pancreatitis vs Adjacent Normal pancreatic tissue  
  Platform: Affymetrix Clariom S (GPL17586)

- **GSE25724**: Type 2 Diabetes vs Non-diabetic pancreatic islets  
  Platform: Affymetrix HG-U133A (GPL96)

## Methods
- Data retrieval from GEO using `GEOquery`
- Differential expression analysis using `limma`
- Multiple testing correction (Benjamini–Hochberg)
- Stringent DEG filtering (adjusted p < 0.01, |log2FC| ≥ 1.5)
- Comparative visualization across diseases

## Project Structure
CP_T2D_Comparative_Transcriptomics/
├── CP_T2D_Comparative_Transcriptomics.R
├── CP_T2D_Comparative_Transcriptomics.Rproj
├── README.md
├── results/
│ ├── Figure_1A_CP_volcano.png
│ ├── Figure_1B_T2D_volcano.png
│ ├── Figure_2_Directionality_comparison.png
│ └── Figure_3_logFC_distribution.png
└── tables/
├── Table_1_Comparative_summary_CP_vs_T2D.csv
├── Table_S1_Top_CP_transcripts.csv
└── Table_S2_Top_T2D_transcripts.csv


## Key Outputs
- Volcano plots for CP and T2D
- Directionality comparison of differential expression
- Distribution of transcript-level fold changes
- Summary and supplementary DEG tables

## Reproducibility
To reproduce the analysis:
1. Clone the repository
2. Open `CP_T2D_Comparative_Transcriptomics.Rproj`
3. Run:
```r
source("CP_T2D_Comparative_Transcriptomics.R")
Author
Anamika
(Computational transcriptomics project)

License
This project is intended for academic and research use.

