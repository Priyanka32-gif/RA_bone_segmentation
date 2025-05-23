# Bone Segmentation and Landmark Localization from CT Scans of Knee

This project focuses on the segmentation of the **femur** and **tibia** bones from 3D CT scans and the identification of key anatomical landmarks on the tibial plateau, including **medial and lateral lowest points**. The pipeline includes preprocessing, visualization of different views ** Axial, Sagttial, and Coronal**, identifying slices, segmentation, region separation, 3D visualization, contour expansion, contour randomization and precise spatial analysis.

## 🔍 Overview

The project is divided into four key tasks:

- **Task 1.1:** Femur and Tibia Bone Segmentation from CT images
- **Task 1.2:** Visualization of segmented volumes and Contour expansion by 2mm and 4mm
- **Task 1.3:** Randomized contour expansion within 2 mm of the original boundary
- **Task 1.4:** Landmark identification on the tibial plateau using clustering and 3D depth analysis

### p

## ⚙️ How to Run

Install all dependenies from requirement.txt file 
    ''' pip install -r requirements.txt '''

🎯 Task 1.1 – Bone Segmentation

CT scans were loaded using  or nibabel.

A threshold-based method was used to isolate bone (threshold 350).

Morphological operations were applied to refine segmentation.

Connected components analysis helped isolate femur and tibia masks.


Task 1.2 – Contour Expansion

Mask erosion performed to get outer shell of bone.

Used Euclidial Distance Transform to expand contour by 2mm and 4mm.


🔀 Task 1.3 – Randomized Contour Expansion

Randomized contour using distance transform and numpy operation between 2mm expanded mask and orginal mask of bone


📍 Task 1.4 – Landmark Localization
Extract tibial plateau surface

PCA + K-Means clustering

Find lowest medial & lateral points (Z-max)

