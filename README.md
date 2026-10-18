# Deep learning auto-segmentation for breast and prostate radiotherapy planning

**MSc Artificial Intelligence thesis — University of Amsterdam**
Hosted at Curtin University, Perth (Jan–Jun 2026). Supervisors: Hoel Kervadec (UvA), Curtise Ng (Curtin).

*Development of Clinically Usable Deep Learning-Based Auto-Segmentation Model for Breast and Prostate Radiation Therapy Treatment Planning Through Transfer Learning*

## Summary
Manual contouring of clinical target volumes (CTVs) and organs at risk (OARs) is slow and varies between clinicians. This thesis trains and evaluates nnU-Net v2 auto-segmentation models for two cancer types and tests whether cross-anatomy transfer learning helps.

- **Breast (226 patients):** nnU-Net benchmarked against commercial auto-segmentation software. Clinically acceptable accuracy (DSC ≥ 0.90) for heart (0.965) and lungs (0.987–0.989), matching or exceeding the commercial tool; smaller structures and CTVs fell below the threshold.
- **Prostate (six genitourinary substructures):** trained from scratch and with encoder weights transferred from the breast model. Strong for the bladder (DSC 0.954), lower for the five smaller substructures (0.539–0.711).
- **Transfer learning:** no statistically significant gain from breast→prostate transfer (all differences within ±0.012, p > 0.05).
- **Main finding:** structure size is the strongest predictor of segmentation performance; custom nnU-Net models are clinically competitive for large, well-defined structures, while small and low-contrast structures need further work.

## Methods
nnU-Net v2 · PyTorch · 3D full-resolution U-Net · transfer learning (encoder initialisation) · Dice and 95th-percentile Hausdorff distance · GPU/SLURM training · statistical comparison of model variants

## Code and data
The clinical data, trained models and source code are confidential under the host agreement and are not published. 
