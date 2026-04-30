# Introduction
This project aims to develop an Artificial Intelligence (AI) model for automated sleep stage classification using Ballistocardiograph (BCG) signals. By leveraging deep learning architectures (such as CNNs and Transformers), we aim to provide an accurate, non-invasive alternative to traditional sleep staging methods.
# Single-Channel Sleep Classification

Sleep stages can be estimated using a single physiological channel such as ECG by analyzing autonomic nervous system activity. However, single-lead ECG alone often provides lower accuracy than full PSG because it lacks direct EEG information.

By using BCG, we obtain a richer contact-free signal that captures:

 1. Cardiac activity (ECG proxy)
 2. Respiratory patterns
 3. Body movements

This provides more information than a traditional single-lead ECG while maintaining a simple acquisition setup.

# Why BCG Instead of Direct ECG?

Traditional ECG requires skin-attached electrodes, which may cause discomfort, motion artifacts, and reduced long-term usability.

BCG sensors, placed under the mattress, offer:

 1. Contact-free monitoring
 2. Minimal disturbance during sleep
 3. Improved user comfort and long-term compliance
 4. Stable overnight acquisition without wearable sensors

Raw BCG Signal
      ↓
Preprocessing
      ↓
ECG Reconstruction
      ↓
R-Peak Detection
      ↓
HRV Feature Extraction
      ↓
Sleep Stage Classification
