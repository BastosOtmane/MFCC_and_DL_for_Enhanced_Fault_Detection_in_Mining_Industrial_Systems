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
1. CMG data:
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

## Results :
1. CMG data:
   | Architecture  | Training Duration (min) | Tr/Loss  |  Tr/Acc  |  Tr/AUC | Vl/Loss    |  Vl/Acc  | Vl/AUC  | Tst/Loss| Tst/Acc  | Tst/AUC |
   |---------------|-------------------------|:--------:|----------|---------|:----------:|----------|---------|:-------:|----------|---------|
   | AlexNet       | 68.94                   | 0.0548   | 97.89    | 0.9986  | 0.1531     | 95.73    | 0.9925  | 0.1692  | 95.94    | 0.9935  |
   | VGG16         | 281.50                  | 0.0227   | 99.24    | 0.9996  | 0.3015     | 94.63    | 0.9818  | 0.3467  | 94.03    | 0.9810  |
   | VGG19         | 334.03                  | 0.0326   | 98.90    | 0.9991  | 0.1840     | 95.13    | 0.9892  | 0.2475  | 95.11    | 0.9881  |
   | Inception v1  | 100.68                  | 0.0319   | 98.85    | 0.9994  | 0.1305     | 95.57    | 0.9942  | 0.1340  | 96.03    | 0.9815  |
   | ResNet18      | 80.71                   | 0.0106   | 99.62    | 0.9999  | 0.3286     | 93.22    | 0.9786  | 0.3367  | 93.14    | 0.9802  |
   | ResNet34      | 125.16                  | 0.0139   | 99.54    | 0.9996  | 0.2817     | 93.03    | 0.9837  | 0.2998  | 92.22    | 0.9827  |
   | ResNet50      | 157.79                  | 0.0129   | 99.60    | 0.9997  | 0.2365     | 94.43    | 0.9860  | 0.2342  | 94.56    | 0.9857  |
   | DenseNet121   | 219.80                  | 0.0132   | 99.67    | 0.9996  | 0.2681     | 94.52    | 0.9834  | 0.2853  | 94.56    | 0.9815  |
   | MobileNet v1  | 66.40                   | 0.0337   | 98.81    | 0.9989  | 0.1756     | 95.15    | 0.9895  | 0.1750  | 95.00    | 0.9897  |
   | MobileNet v2  | 96.21                   | 0.0143   | 99.56    | 0.9996  | 0.1718     | 95.78    | 0.9906  | 0.1789  | 95.67    | 0.9891  |
   | MobileNet v3L | 80.61                   | 0.0194   | 99.46    | 0.9994  | 0.2410     | 95.20    | 0.9842  | 0.2348  | 95.00    | 0.9859  |
   | MobileNet v3S | 43.40                   | 0.0103   | 99.62    | 0.9999  | 0.2778     | 95.40    | 0.9828  | 0.3124  | 94.94    | 0.9804  |
2. CWRU dataset :
   | Architecture  | Training Duration (min) | Tr/Loss  |  Tr/Acc  |  Tr/AUC | Vl/Loss    |  Vl/Acc  | Vl/AUC  | Tst/Loss| Tst/Acc  | Tst/AUC |
   |---------------|-------------------------|:--------:|----------|---------|:----------:|----------|---------|:-------:|----------|---------|
   | AlexNet       | 68.94                   | 0.0548   | 97.89    | 0.9986  | 0.1531     | 95.73    | 0.9925  | 0.1692  | 95.94    | 0.9935  |
   | VGG16         | 281.50                  | 0.0227   | 99.24    | 0.9996  | 0.3015     | 94.63    | 0.9818  | 0.3467  | 94.03    | 0.9810  |
   | VGG19         | 334.03                  | 0.0326   | 98.90    | 0.9991  | 0.1840     | 95.13    | 0.9892  | 0.2475  | 95.11    | 0.9881  |
   | Inception v1  | 100.68                  | 0.0319   | 98.85    | 0.9994  | 0.1305     | 95.57    | 0.9942  | 0.1340  | 96.03    | 0.9815  |
   | ResNet18      | 80.71                   | 0.0106   | 99.62    | 0.9999  | 0.3286     | 93.22    | 0.9786  | 0.3367  | 93.14    | 0.9802  |
   | ResNet34      | 125.16                  | 0.0139   | 99.54    | 0.9996  | 0.2817     | 93.03    | 0.9837  | 0.2998  | 92.22    | 0.9827  |
   | ResNet50      | 157.79                  | 0.0129   | 99.60    | 0.9997  | 0.2365     | 94.43    | 0.9860  | 0.2342  | 94.56    | 0.9857  |
   | DenseNet121   | 219.80                  | 0.0132   | 99.67    | 0.9996  | 0.2681     | 94.52    | 0.9834  | 0.2853  | 94.56    | 0.9815  |
   | MobileNet v1  | 66.40                   | 0.0337   | 98.81    | 0.9989  | 0.1756     | 95.15    | 0.9895  | 0.1750  | 95.00    | 0.9897  |
   | MobileNet v2  | 96.21                   | 0.0143   | 99.56    | 0.9996  | 0.1718     | 95.78    | 0.9906  | 0.1789  | 95.67    | 0.9891  |
   | MobileNet v3L | 80.61                   | 0.0194   | 99.46    | 0.9994  | 0.2410     | 95.20    | 0.9842  | 0.2348  | 95.00    | 0.9859  |
   | MobileNet v3S | 43.40                   | 0.0103   | 99.62    | 0.9999  | 0.2778     | 95.40    | 0.9828  | 0.3124  | 94.94    | 0.9804  |
