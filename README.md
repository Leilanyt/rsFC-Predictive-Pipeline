# rsFC-Predictive-Pipeline

This project implements a first version of a resting‑state functional connectivity (rsFC) predictive pipeline using an initial small dataset of (N = 30 participants) from the UCLA Consortium for Neuropsychiatric Phenomics dataset, which includes resting‑state fMRI from healthy controls and individuals with mood and psychotic disorders.

In this v1 analysis, I focus on distinguishing healthy vs. bipolar participants using connectivity between large‑scale functional networks. I extract rsFC features from 6 Yeo networks with a Schaefer ROI mask, build network‑level connectivity matrices, and train a linear SVM classifier with stratified 5‑fold cross‑validation.

The goals of this pipeline are to:
- Test whether rsFC edges are predictive of diagnostic group (HC vs. BD).  
- Quantify model stability via permutation testing (observed mean accuracy ≈ 0.73 vs. null distribution).  
- Map SVM weights back into a 7×7 network‑by‑network matrix to identify which connections contribute most to classification.
