Uncertainty-Weighted Grad-CAM (UTW-GradCAM) for Cardiac MRI Segmentation

This repository contains the full implementation of UTW-GradCAM, a novel explainability method that integrates epistemic uncertainty
(via Monte-Carlo dropout) directly into the Grad-CAM formulation, generating more stable, reliable, and diagnostically meaningful saliency maps 
for cardiac MRI segmentation.

Motivation
Conventional Grad-CAM in medical imaging suffers from:
*High variability
*Noisy activation maps
*Sensitivity to random seeds
*Poor reliability in low-confidence predictions

Our method addresses these limitations by incorporating uncertainty into the explanation.
Novel Contribution: UTW-GradCAM
What we propose
For an input image, we perform T Monte-Carlo stochastic forward passes (due to dropout), obtaining:

*Multiple activation maps
*Multiple Grad-CAM heatmaps
*An epistemic uncertainty estimate
*A reliability score

# UTW-GradCAM for Cardiac MRI Segmentation
This repository contains the implementation of Uncertainty-Weighted GradCAM (UTW-GradCAM)...

## Features
- Monte-Carlo dropout for epistemic uncertainty
- Layer-wise activation inspection
- Reliability-weighted GradCAM maps
- Dice-overlap evaluation
- Supports U-Net and custom architectures

## How to run
1. Open notebook in Google Colab
2. Upload your trained model
3. Run UTW-GradCAM on any MRI slice
