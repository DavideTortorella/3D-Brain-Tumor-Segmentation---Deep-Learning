# Brain Tumor Segmentation with U-Net

## Intro
This project has been realized during the 'Foundations of Deep Learning' course of the Data Science Master Degree from University of Milano Bicocca.

This project is based on the **BraTS dataset** from the [Medical Segmentation Decathlon](http://medicaldecathlon.com/).  
The goal was to perform **image segmentation** on brain MRI scans: classifying each voxel of the volume into one of four categories:  
- Brain  
- Edema  
- Non-enhancing tumor  
- Enhancing tumor  

## Description
The dataset consists of **4D volumes** (3D brain scans with 4 channels) labeled according to the four segmentation classes.  

### Preprocessing steps
- **Cropping** of irrelevant regions  
- **Downsampling** of the most frequent class to address the imbalance problem  
- **Normalization** of voxel intensity values  

### Models
Two U-Net architectures were trained using a combined **Categorical Cross-Entropy (CCE) + Dice Loss** function:  
- **2D U-Net** → faster to train, ~2 million parameters  
- **3D U-Net** → more computationally expensive, ~5 million parameters  

The comparison highlights trade-offs between training efficiency and segmentation accuracy when moving from 2D to full 3D processing of medical imaging data.

## Files
`Brain Segmentation.pdf` presentation used for oral exposition \
`DL_project_final.ipynb` contains the Jupyter Notebook used to develop the code \




