# 🌌 MAGIC Gamma Telescope Classification

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0+-red.svg)](https://tensorflow.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Distinguishing gamma rays from cosmic ray background using machine learning techniques on data from the MAGIC (Major Atmospheric Gamma Imaging Cherenkov) telescope.**

## 📖 Project Overview

This project tackles the challenging problem of **gamma ray detection** in high-energy astrophysics using machine learning. The MAGIC telescope detects Cherenkov light produced by gamma rays and cosmic ray particles in the atmosphere. Our goal is to build robust classifiers that can accurately distinguish between:

- **Gamma rays** (signal) - from astronomical sources
- **Hadrons** (background) - cosmic ray particles that mimic gamma ray signatures

### 🎯 Why This Matters
Accurate gamma ray detection is crucial for:
- Discovering new astronomical gamma ray sources
- Studying high-energy phenomena in the universe  
- Advancing our understanding of cosmic ray physics
- Improving telescope sensitivity and observation efficiency

## 🚀 Key Features

- **Multi-Algorithm Approach**: Comprehensive comparison of 5 different ML algorithms
- **Advanced Data Processing**: Handles class imbalance and feature standardization
- **Neural Network Optimization**: Systematic hyperparameter tuning with grid search
- **Robust Evaluation**: Performance analysis across multiple metrics
- **Production-Ready**: Clean, modular code with reproducible results

## 📊 Dataset

**Source**: [UCI Machine Learning Repository - MAGIC Gamma Telescope Dataset](https://doi.org/10.24432/C52C8B)

**Features** (10 continuous attributes):
- `fLength`: Major axis of ellipse [mm]
- `fWidth`: Minor axis of ellipse [mm] 
- `fSize`: 10-log of sum of content of all pixels [in #phot]
- `fConc`: Ratio of sum of two highest pixels over fSize [ratio]
- `fConc1`: Ratio of highest pixel over fSize [ratio]
- `fAsym`: Distance from highest pixel to center, projected onto major axis [mm]
- `fM3Long`: 3rd root of third moment along major axis [mm]
- `fM3Trans`: 3rd root of third moment along minor axis [mm]
- `fAlpha`: Angle of major axis with vector to origin [deg]
- `fDist`: Distance from origin to center of ellipse [mm]

**Target**: Binary classification (Gamma = 1, Hadron = 0)

**Size**: 19,020 instances
- Gamma events: ~65%
- Hadron events: ~35%

## 🛠️ Methods & Algorithms

### Machine Learning Models
1. **k-Nearest Neighbors (kNN)** - Instance-based learning
2. **Naive Bayes** - Probabilistic classifier  
3. **Logistic Regression** - Linear classification
4. **Support Vector Machine (SVM)** - Maximum margin classifier
5. **Neural Network** - Deep learning with hyperparameter optimization

### Data Processing Pipeline
- **Feature Standardization**: StandardScaler normalization
- **Class Balance Handling**: RandomOverSampler for minority class
- **Train/Validation/Test Split**: 60/20/20 ratio
- **Cross-Validation**: Stratified sampling for robust evaluation

### Neural Network Architecture
- **Hidden Layers**: 2 layers with ReLU activation
- **Regularization**: Dropout layers for overfitting prevention
- **Optimization**: Adam optimizer with configurable learning rate
- **Hyperparameter Tuning**: Grid search across:
  - Nodes: [16, 32, 64]
  - Dropout: [0.0, 0.2]
  - Learning Rate: [0.01, 0.005, 0.001]
  - Batch Size: [32, 64, 128]

## 📈 Results

### Model Performance Summary

| Algorithm | Accuracy | Precision | Recall | F1-Score |
|-----------|----------|-----------|---------|----------|
| **Neural Network** | **88%** | **0.89** | **0.93** | **0.91** |
| **SVM** | 87% | 0.90 | 0.90 | 0.90 |
| **kNN** | 84% | 0.86 | 0.89 | 0.88 |
| **Logistic Regression** | 80% | 0.86 | 0.82 | 0.84 |
| **Naive Bayes** | 73% | 0.74 | 0.90 | 0.81 |

### Key Insights
- **Neural Network** achieved the best overall performance (88% accuracy)
- **SVM** showed excellent precision-recall balance
- **Class imbalance handling** significantly improved minority class detection
- **Feature standardization** was crucial for distance-based algorithms

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- **Binary Classification**: Multi-algorithm approach with performance comparison
- **Data Preprocessing**: Standardization, sampling, and train/test splitting
- **Deep Learning**: Neural network architecture design and hyperparameter tuning
- **Model Evaluation**: Comprehensive metrics and validation strategies
- **Scientific Computing**: NumPy, Pandas, and scikit-learn ecosystem
- **Physics Applications**: Real-world astrophysics data analysis

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🏆 Acknowledgments

- **MAGIC Collaboration** for providing the dataset
- **UCI Machine Learning Repository** for dataset hosting
- **scikit-learn community** for excellent ML tools
- **TensorFlow team** for deep learning framework

---

⭐ **Star this repository if you found it helpful!**