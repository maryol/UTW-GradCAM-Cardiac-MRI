# UTW-GradCAM for Cardiac MRI Segmentation
This repository contains the implementation of Uncertainty-Weighted GradCAM (UTW-GradCAM), a novel explainability method that integrates epistemic uncertainty(via Monte-Carlo dropout) directly into the Grad-CAM formulation, generating more stable, reliable, and diagnostically meaningful saliency maps for cardiac MRI segmentation.

Conventional Grad-CAM in medical imaging suffers from:
*High variability
*Noisy activation maps
*Sensitivity to random seeds
*Poor reliability in low-confidence predictions

Our method addresses these limitations by incorporating uncertainty into the explanation.
For an input image, we perform T Monte-Carlo stochastic forward passes (due to dropout), obtaining:
*Multiple activation maps
*Multiple Grad-CAM heatmaps
*An epistemic uncertainty estimate
*A reliability score
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

Conventional Myocardium GRAD-CAM results on some slices:

<img width="993" height="339" alt="download (2)" src="https://github.com/user-attachments/assets/ad578ec1-41ee-4a9b-98cf-1de37771a59e" />
<img width="993" height="339" alt="download (5)" src="https://github.com/user-attachments/assets/e88cd5ed-3bfe-446a-80a0-ffce78098ad1" />
<img width="993" height="339" alt="download (7)" src="https://github.com/user-attachments/assets/560fd98e-6e2b-4c83-af1f-f24e7eb37ab8" />
<img width="993" height="339" alt="download (11)" src="https://github.com/user-attachments/assets/e146103a-48b9-4dea-9e71-f1e4092be726" />
