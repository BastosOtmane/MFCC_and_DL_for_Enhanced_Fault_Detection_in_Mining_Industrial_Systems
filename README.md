# MFCC and DL for Enhanced Fault Detection in Mining Industrial Systems

## Introduction

With the rapid and remarkable development of artificial intelligence technology worldwide, the integration of these techniques into industrial plants has become a necessity in order to benefit from the advantages these technologies offer. Mining industrial systems and machines are also concerned to use these revolutionary technologies given the advantages they bring, such as predict equipment failures before they occur, enabling rapid interventions and reducing unplanned downtime.

In this project, we explored various deep convolutional neural networks (CNNs) architectures, and conducted some experiments using two datasets, the first is vibration data of a grinding mill collected from a real industrial environment and the second is the [Case western reserve university (CWRU) vibration bearing dataset](https://engineering.case.edu/bearingdatacenter/download-data-file). The results of our experiments shows the effectiveness of using MFCC spectrograms and CNNs in fault detection and vibration analysis.

## CNN architecures :
* AlexNet
* VGG 16 & 19
* ResNet 18, 34 & 50
* Inception v1
* DenseNet121
* MobileNet v1, v2 & v3 (small and large)

## Vibration data characteristics :
1. Real industrial data:
   - Recording location : Pignon
   - Sampling rate : 2 Hz
   - Spectrogram images extracted : 21 600 (1200 data points each)
       - Training : 14 400
       - Validation : 3600
       - Testing : 3600
   - Number of conditions : 3
2. CWRU dataset :
   - Recording location : Bearing
   - Sampling rate : 12 kHz
   - Spectrogram images extracted : 18 465 (1200 data points each)
       - Training : 12 909
       - Validation : 2741
       - Testing : 2815
   - Number of conditions : 16

## Frameworks and Packages :
- TensorFlow
- OpenCV
- Librosa
- Pandas
- Scipy
- Numpy
- Scikit-learn
- SHAP
