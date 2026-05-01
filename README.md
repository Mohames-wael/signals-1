# Introduction
This project aims to develop an Artificial Intelligence (AI) model for automated sleep stage classification using Ballistocardiograph (BCG) signals. By leveraging deep learning architectures (such as CNNs and Transformers), we aim to provide an accurate, non-invasive alternative to traditional sleep staging methods.
# Single-Channel Sleep Classification. Is it possible?
Feasibility: Yes, sleep stages can be effectively classified using a single-channel signal (like ECG) by analyzing variations in the autonomic nervous system.

# Why BCG Instead of Direct ECG?

Traditional ECG requires skin-attached electrodes, which may cause discomfort, motion artifacts, and reduced long-term usability.

BCG sensors, placed under the mattress, offer:

 1. Contact-free monitoring
 2. Minimal disturbance during sleep
 3. Improved user comfort and long-term compliance
 4. Stable overnight acquisition without wearable sensors

# Project Pipeline
<img width="315" height="1024" alt="image" src="https://github.com/user-attachments/assets/3fd05860-305f-466a-b3b3-2a4d595e6902" />

# Dataset
This project uses sleep-related physiological recordings and annotation files containing sleep stage labels extracted from XML data.


# Window Segmentation

The continuous BCG recordings are divided into fixed 30-second windows (epochs), following the standard approach used in sleep staging systems.

Each window represents a single sleep stage label extracted from the XML annotations (Wake, N1, N2, N3, or REM).

# Training Strategy

To improve model robustness and address class imbalance:

1. Oversampling is applied only to the N1 class within the training set
2. Noise-based augmentation is added to training samples
3. Focal Loss is used to improve learning on minority classes

# Results

The proposed CNN + Transformer model achieved promising performance for single-channel BCG-based sleep stage classification.

# Performance Metrics
Accuracy: 76.96%
Loss: 0.1060

The model was evaluated on the original test set after applying preprocessing, class balancing, and data augmentation techniques.
