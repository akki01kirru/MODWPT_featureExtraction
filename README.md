MIT-BIH Arrhythmia Dataset – Feature Extraction Using MODWPT
📌 Overview

This repository contains MATLAB code for feature extraction from the MIT-BIH Arrhythmia Database using the Maximal Overlap Discrete Wavelet Packet Transform (MODWPT) technique.

The repository includes the 100m ECG signal and MATLAB functions for extracting time-domain, morphological, and RR-interval-related features from the ECG signal.

📊 Dataset

Dataset: MIT-BIH Arrhythmia Database
Record: 100m
Signal: ECG

The file:

100m.mat

contains the ECG signal used for feature extraction.

The extracted features include characteristics related to:

RR intervals
QRS complexes
ECG waveform morphology
Signal slope
Amplitude/statistical measures
Power spectral density
🔬 Feature Extraction Method

The feature extraction process is based on MODWPT (Maximal Overlap Discrete Wavelet Packet Transform).

Processing Flow
MIT-BIH Arrhythmia ECG Signal
            │
            ▼
       100m.mat
            │
            ▼
       Preprocessing
            │
            ▼
          MODWPT
            │
            ▼
     Feature Extraction
            │
            ├── RR Features
            ├── QRS Features
            ├── Morphological Features
            ├── Statistical Features
            └── Spectral Features
            │
            ▼
      Extracted Feature Set
📁 Repository Contents
File	Description
100m.mat	MIT-BIH ECG record 100m used for analysis
features_extract_modwpt.m	Main MATLAB script for MODWPT-based feature extraction
find_NN50.m	Calculates NN50-related feature
find_PSD.m	Calculates Power Spectral Density
find_QRSarea.m	Calculates QRS complex area
find_QRtoQS_RstoQS.m	Calculates Q/R/S related morphological feature
find_RMSSD.m	Calculates RMSSD feature
find_RSslope.m	Calculates R-S slope
find_SDSD.m	Calculates SDSD feature
find_SD_RR.m	Calculates standard deviation of RR intervals
find_angle.m	Calculates ECG waveform angle-related feature
find_dis.m	Calculates distance-related feature
find_mean_RR.m	Calculates mean RR interval
find_peri.m	Calculates perimeter-related feature
find_slope.m	Calculates slope-related feature
🧮 Extracted Features

The MATLAB implementation extracts several ECG characteristics, including:

RR-Interval Features
Mean RR interval
SD of RR intervals
RMSSD
SDSD
NN50
QRS Features
QRS area
Q/R/S-related characteristics
R-S slope
Morphological Features
Slope
Angle
Distance
Perimeter
Frequency-Domain Features
Power Spectral Density (PSD)

These features can subsequently be used for ECG arrhythmia analysis and classification.

⚙️ Requirements
Software
MATLAB
Signal Processing Toolbox recommended
Wavelet Toolbox recommended for MODWPT processing
🚀 How to Run
Step 1: Clone the Repository
git clone <YOUR-GITHUB-REPOSITORY-URL>
Step 2: Open MATLAB

Open MATLAB and navigate to the repository folder.

Step 3: Add the Folder to MATLAB Path
addpath(genpath(pwd));
Step 4: Load the ECG Signal
load('100m.mat');
Step 5: Run Feature Extraction

Execute:

features_extract_modwpt

The script uses the supporting MATLAB functions to calculate the required ECG features.

📈 Applications

The extracted features can be used for:

ECG arrhythmia classification
Abnormal heartbeat detection
Heart-rate variability analysis
Machine learning-based ECG analysis
Feature selection
Deep learning research
Biomedical signal processing
Automated cardiac disease analysis

Possible machine-learning classifiers include:

Random Forest
SVM
KNN
Decision Tree
XGBoost
ANN
CNN
LSTM
🔄 Overall Workflow
MIT-BIH Arrhythmia Database
            ↓
        ECG Record
         (100m)
            ↓
       Signal Processing
            ↓
          MODWPT
            ↓
     Feature Extraction
            ↓
 ┌─────────────────────────┐
 │ RR Features             │
 │ QRS Features            │
 │ Morphological Features │
 │ Spectral Features       │
 └─────────────────────────┘
            ↓
      Feature Dataset
            ↓
   ML / DL Classification
            ↓
   Arrhythmia Detection
⚠️ Dataset Note

The 100m.mat file represents a record from the MIT-BIH Arrhythmia Database. Users should refer to the original MIT-BIH database documentation and PhysioNet licensing/usage conditions when redistributing or publishing results based on the data.

This repository primarily provides the MATLAB feature-extraction implementation associated with the ECG signal.

🎯 Purpose

The objective of this repository is to provide a reproducible MATLAB implementation for MODWPT-based ECG feature extraction that can serve as a preprocessing stage for subsequent arrhythmia detection and machine-learning classification research.

👩‍💻 Author

Dr. L. Alekhya
Department of Electronics and Communication Engineering
Lendi Institute of Engineering & Technology, Vizianagaram, India

🔑 Keywords
MIT-BIH Arrhythmia Database
ECG
Arrhythmia Detection
MODWPT
Wavelet Transform
ECG Feature Extraction
QRS Complex
RR Interval
HRV
MATLAB
Biomedical Signal Processing
Machine Learning
Deep Learning
MIT-BIH Arrhythmia · ECG · Arrhythmia Detection · MODWPT · Wavelet Transform · ECG Feature Extraction · RR Interval · QRS Complex · HRV · MATLAB · Biomedical Signal Processing · Machine Learning
