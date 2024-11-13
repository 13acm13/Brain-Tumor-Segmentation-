# Brain Tumor Segmentation Using 3D U-Net and MRI Data

This project focuses on brain tumor segmentation from MRI images using a 3D U-Net architecture. The model was trained on the BraTS 2023 dataset to accurately delineate tumor regions, providing essential diagnostic support for identifying aggressive brain tumors like glioblastomas. Our approach incorporates specialized loss functions to enhance boundary precision and class balancing, crucial for complex tumor structures.

## Dataset
- **BraTS 2023 Dataset**: Multi-modal MRI scans with annotations for tumor regions, including T1ce, T2w, and FLAIR sequences.

## Model Architecture
- **3D U-Net**: A volumetric segmentation network that captures spatial continuity across MRI slices, enhancing segmentation accuracy for tumor regions.
- **Loss Functions**: We integrated multiple loss functions to improve segmentation precision:
  - **Dice Loss**: Maximizes overlap between predicted and ground truth masks, particularly effective for imbalanced classes.
  - **Focal Loss**: Focuses on challenging examples, addressing class imbalance by down-weighting easy-to-classify pixels.
  - **Edge-aware Loss**: Detects and emphasizes tumor boundaries using a Laplacian filter, enhancing boundary sharpness in the segmentation.
  - **Combined Loss Variants**:
    1. **Edge + Focal**: Balances edge detection with class-sensitive focal weighting.
    2. **Edge + Dice + Focal**: Combines overlap maximization, class focus, and edge awareness, boosting precision on both tumor structure and boundaries.

## Training Details
- **Data**: Trained on 50 patient MRI scans.
- **Epochs**: 100
- **Objective**: Accurately segment enhancing tumor, tumor core, and whole tumor regions.

## Results
- **IoU, Loss, Accuracy were plotted and compared.**


