# Classification of Heart Beats using EMD-Generated 2D Grayscale Images

This repository contains the implementation of a novel approach for classifying heartbeats by converting one-dimensional (1-D) data into two-dimensional (2-D) grayscale images. The method utilizes empirical mode decomposition (EMD) to remove low-frequency intrinsic mode functions (IMFs) considered as noise from the signal. The resulting 2-D grayscale images are then processed and analyzed for accurate heartbeat classification.

## Introduction
The objective of this project is to develop a more accurate method for converting 1-D medical data into 2-D grayscale images, enabling improved heartbeat classification. The implementation involves the following key steps:

1. **Data**: The project utilizes the [MIT-BIH Arrhythmia Dataset](https://www.kaggle.com/shayanfazeli/heartbeat) available on Kaggle. This dataset provides a collection of heartbeat recordings, including various arrhythmias.

2. **EMD-based Signal Processing**: Empirical mode decomposition (EMD) is employed to decompose the 1-D ECG signal into intrinsic mode functions (IMFs), effectively separating the signal components.

3. **Grayscale Image Generation**: By squaring the pixel values of the resulting IMFs, grayscale images are created. This transformation captures the energy present in each pixel, providing a visual representation of the signal.

4. **Feature Extraction**: Local Binary Pattern (LBP) is utilized as a feature extraction method to capture precise texture data from the grayscale images. The LBP algorithm identifies patterns and textures within the images, which serve as discriminative features for classification.

5. **Heartbeat Classification**: A RandomForest classifier is trained on the extracted features to classify heartbeats into different categories. The classifier leverages the discriminative information captured by the LBP features to accurately classify heartbeats.

## Conclusion
This project demonstrates a novel approach for converting 1-D ECG data into 2-D grayscale images using empirical mode decomposition (EMD). The generated images are processed with feature extraction using Local Binary Pattern (LBP) and classified using a RandomForest classifier. The combination of signal processing and machine learning techniques results in improved accuracy in heartbeat classification.

For more details and a step-by-step implementation, refer to the `Final_code.ipynb` notebook and for results refer to the `Results.pdf` in this repository.
