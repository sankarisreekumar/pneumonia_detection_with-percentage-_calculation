Pneumonia Detection & Percentage of Infection using VGG16 + Segmentation + Grad-CAM

This project detects Pneumonia from Chest X-Ray images and additionally calculates the percentage of lung infection.
It combines classification, segmentation, and explainability techniques to provide a more interpretable medical AI workflow.

 1. Pneumonia Detection (Classification Model)

Used a pretrained VGG16 model with Transfer Learning.

Trained on a public Chest X-Ray dataset from Kaggle.

The model outputs whether the given X-ray image is:

Pneumonia

Normal

 2. Lung Segmentation (Percentage Calculation)

Built a simple segmentation model (U-Net-like) and trained it on a lung segmentation dataset from Kaggle.

The segmentation mask helps isolate only the lung region for more accurate calculations.

 3. Grad-CAM Heatmap (Infection Region Localization)

Applied Grad-CAM on the classification model to highlight the most affected areas indicating pneumonia.

The Grad-CAM output provides a heatmap showing infection intensity.

 4. Infection Percentage Calculation

The percentage of lung affected by pneumonia is computed as:

Infection
 
Percentage
=
Lesion Area from Grad-CAM
Total Lung Area from Segmentation Model
×
100
Infection Percentage=
Total Lung Area from Segmentation Model
Lesion Area from Grad-CAM


	Features Included

Pneumonia detection using Transfer Learning (VGG16)

Lung segmentation using custom-trained segmentation model

Grad-CAM visualization for explainability

Infection percentage estimation

Code for preprocessing, model training, heatmap generation, and percentage calculation

 Applications

Assistive medical screening

AI-based second opinion for radiologists

Educational and research use

Explainable AI in healthcare​

×100

This gives a quantitative measure of how much of the lung is affected.
