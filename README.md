# CTGAN-Based Synthetic Fetal CTG Dataset

## 📌 Overview

This repository contains a **synthetically balanced fetal cardiotocography (CTG) dataset** generated using a **Conditional Tabular Generative Adversarial Network (CTGAN)**.

The dataset was developed from an existing fetal CTG dataset containing three clinical classes:

* **Normal**
* **Suspect**
* **Pathological**

CTGAN was employed to generate synthetic samples while preserving the statistical characteristics and relationships present in the original fetal CTG data.

After synthetic data generation and preprocessing, the dataset contains **1,936 samples for each class**, resulting in a total of **5,808 samples**.

The dataset is intended for **machine learning, deep learning, data analysis, class-balancing experiments, and research on automated fetal health-status classification**.

---

## 🎯 Dataset Objective

The primary objective of this dataset is to provide a balanced fetal CTG dataset that can be used to investigate machine-learning approaches for the classification of fetal health conditions.

The three target classes are:

| Class        | Description                                                                             |   Samples |
| ------------ | --------------------------------------------------------------------------------------- | --------: |
| Normal       | CTG recordings/features corresponding to normal fetal condition                         |     1,936 |
| Suspect      | CTG recordings/features indicating a potentially abnormal or suspicious fetal condition |     1,936 |
| Pathological | CTG recordings/features associated with pathological fetal condition                    |     1,936 |
| **Total**    |                                                                                         | **5,808** |

The equal number of samples in each class makes the dataset suitable for evaluating classification algorithms without introducing class imbalance from the dataset size itself.

---

## 🧠 Data Generation Methodology

The synthetic data generation process follows the general pipeline:

```text
Original Fetal CTG Dataset
          │
          ▼
   Data Preprocessing
          │
          ▼
 Class-wise Data Separation
          │
          ▼
     CTGAN Training
          │
          ▼
 Synthetic Data Generation
          │
          ▼
 Quality & Statistical Analysis
          │
          ▼
 Data Normalization
          │
          ▼
 Balanced Dataset
          │
          ▼
 1,936 Samples / Class
          │
          ▼
 GitHub Repository
```

### CTGAN

**CTGAN (Conditional Tabular Generative Adversarial Network)** is a generative model designed for generating synthetic tabular data.

In this work, CTGAN was used to generate additional fetal CTG samples for the three target categories:

* Normal
* Suspect
* Pathological

The generated samples were subsequently processed and normalized before being included in the final dataset.

---

## 📊 Dataset Structure

The final dataset contains:

```text
Total Samples = 5,808

Normal       = 1,936
Suspect      = 1,936
Pathological = 1,936
```

The dataset consists of normalized CTG-related numerical features along with the corresponding class label.

A typical dataset structure can be represented as:

```text
Dataset
│
├── Feature_1
├── Feature_2
├── Feature_3
├── ...
├── Feature_N
└── Label
```

Where:

```text
Label = Normal
Label = Suspect
Label = Pathological
```

> The exact feature names and descriptions should be interpreted according to the source fetal CTG dataset and the corresponding preprocessing notebook provided in this repository.

---

## 🔄 Data Preprocessing

The generated dataset underwent preprocessing before being used for machine-learning experiments.

The major preprocessing stages include:

1. **Data cleaning**
2. **Class-wise organization**
3. **Synthetic sample generation using CTGAN**
4. **Integration of original and generated data**
5. **Feature normalization**
6. **Class balancing**
7. **Dataset validation**
8. **Export of the final dataset**

Normalization was performed to bring numerical features into a comparable range and facilitate their use in machine-learning and deep-learning models.

---

## ⚖️ Class Balancing

One of the major objectives of using CTGAN was to address class imbalance.

The final dataset has an equal number of samples in all three categories:

```text
                 Samples
Normal        ████████████████████  1,936
Suspect       ████████████████████  1,936
Pathological  ████████████████████  1,936
```

Therefore:

**Total Dataset = 1,936 × 3 = 5,808 samples**

This balanced structure can help researchers evaluate classification models using metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* Specificity
* Sensitivity
* ROC-AUC
* Confusion Matrix

---

## 🔬 Recommended Machine Learning Applications

The dataset can be used for research and experimentation in:

### 1. Fetal Health Classification

Development of models for:

```text
CTG Features
     ↓
Machine Learning Model
     ↓
┌───────────┬───────────┬──────────────┐
│  Normal   │  Suspect  │ Pathological │
└───────────┴───────────┴──────────────┘
```

Possible algorithms include:

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine
* K-Nearest Neighbors
* XGBoost
* LightGBM
* Artificial Neural Networks
* Deep Neural Networks

### 2. Deep Learning

The dataset can also be used for:

* Feed-forward neural networks
* Multilayer perceptrons
* 1D CNN
* CNN-LSTM
* Autoencoders
* Attention-based architectures

### 3. Synthetic Data Research

The dataset can be used to investigate:

* CTGAN-based data augmentation
* Synthetic medical data generation
* Class balancing
* Generative AI for healthcare
* Synthetic-versus-real data analysis
* Privacy-preserving data generation

---

## 🧪 Suggested Experimental Workflow

Researchers can follow the workflow below:

```text
Dataset
   │
   ▼
Exploratory Data Analysis
   │
   ├── Feature Distribution
   ├── Correlation Analysis
   ├── Class Distribution
   └── Outlier Analysis
   │
   ▼
Train/Test Split
   │
   ▼
Machine Learning / Deep Learning
   │
   ▼
Model Training
   │
   ▼
Model Evaluation
   │
   ├── Accuracy
   ├── Precision
   ├── Recall
   ├── F1-score
   ├── ROC-AUC
   └── Confusion Matrix
   │
   ▼
Comparative Analysis
```

---

## 📈 Data Analysis

Before model development, the following analyses are recommended:

### Class Distribution

Verify that all three categories contain:

```text
Normal       → 1,936
Suspect      → 1,936
Pathological → 1,936
```

### Statistical Analysis

Recommended statistical measures include:

* Mean
* Median
* Standard deviation
* Minimum
* Maximum
* Quartiles
* Skewness
* Kurtosis

### Correlation Analysis

Feature correlation can be analyzed using:

* Pearson correlation
* Spearman correlation
* Correlation heatmaps

---

## 🛡️ Important Note on Synthetic Data

This repository contains **synthetically generated data** produced using CTGAN.

Synthetic samples should **not be interpreted as actual patient records or real clinical observations**.

The generated data are intended for:

* Research
* Educational purposes
* Algorithm development
* Machine-learning experimentation
* Data augmentation studies

They should **not be used directly for clinical diagnosis, treatment decisions, or patient management**.

---

## ⚠️ Clinical Disclaimer

This dataset is intended for **research and academic purposes only**.

The classification labels represent categories derived from the source dataset and should not be interpreted as an independent clinical diagnosis.

Any model developed using this dataset requires appropriate validation using **independent real-world clinical data** before consideration for clinical applications.

---

## 🔐 Privacy and Ethical Considerations

Synthetic data generation can provide a useful approach for research where sharing real patient data may be restricted.

However, synthetic data should still be evaluated for:

* Similarity to the original dataset
* Potential memorization
* Statistical validity
* Privacy risks
* Clinical representativeness
* Generative model bias

The synthetic dataset should therefore be considered a **research dataset rather than a replacement for clinically validated data**.

---

## 📂 Repository Organization

A recommended repository structure is:

```text
Fetal-CTG-CTGAN/
│
├── data/
│   ├── fetal_ctg_synthetic.csv
│   └── README.md
│
├── notebooks/
│   ├── 01_Data_Preprocessing.ipynb
│   ├── 02_CTGAN_Data_Generation.ipynb
│   ├── 03_Data_Analysis.ipynb
│   └── 04_ML_Classification.ipynb
│
├── results/
│   ├── figures/
│   ├── confusion_matrix/
│   └── performance_metrics/
│
├── requirements.txt
│
└── README.md
```

---

## 🛠️ Technologies Used

The dataset generation and analysis can be implemented using:

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* SDV / CTGAN
* Jupyter Notebook

---

## 🚀 Future Research Directions

The dataset can support further research in:

* Explainable AI for fetal health classification
* Deep learning-based CTG analysis
* Hybrid ML-DL models
* Attention-based fetal health prediction
* Federated learning
* Privacy-preserving machine learning
* Synthetic data quality assessment
* Generative AI for biomedical signals
* Quantum machine learning for fetal health classification
* Edge AI for real-time fetal monitoring

A potential research pipeline is:

```text
CTG Data
   ↓
CTGAN-Based Data Augmentation
   ↓
Feature Normalization
   ↓
Feature Selection / Extraction
   ↓
Deep Learning
   ↓
Explainable AI
   ↓
Fetal Health Classification
   ↓
Clinical Validation
```

---

## 📚 Citation

If you use this dataset in your research, please cite the corresponding source dataset and the CTGAN methodology used to generate the synthetic samples.

A suitable citation for this repository can be added after publication or assignment of a DOI.

**Suggested citation format:**

> L. Alekhya, "CTGAN-Based Synthetic Fetal CTG Dataset," GitHub Repository, 2026.

---

## 🤝 Contribution

Contributions are welcome for:

* Data analysis
* Machine-learning implementations
* Deep-learning models
* Synthetic data evaluation
* Explainable AI
* Feature engineering
* Benchmarking

Please create an issue or submit a pull request for proposed improvements.

---

## ⭐ Acknowledgement

This repository is intended to support research and educational activities in **Artificial Intelligence, Machine Learning, Biomedical Signal Processing, and Fetal Health Monitoring**.

---

## 📜 License

Please specify an appropriate license for this repository based on the licensing terms of the **original CTG dataset** and the rights associated with the generated synthetic data.

If the original dataset has restrictions, those restrictions should be respected when redistributing derived or synthetic data.

---

### Keywords

`Fetal CTG` · `Cardiotocography` · `Fetal Health` · `CTGAN` · `Synthetic Data` · `Generative AI` · `Machine Learning` · `Deep Learning` · `Biomedical Signal Processing` · `Fetal Health Classification` · `Healthcare AI` · `Synthetic Medical Data`
