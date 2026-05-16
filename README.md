# Rice_Leaf_Disease_Detection_-MLPR-Project-
Hybrid ML system for rice leaf disease detection using deep + handcrafted features


# Paddy Leaf Disease Detection using Hybrid Machine Learning Approach (MLPR Project)

## 1. Overview
This project presents a hybrid machine learning-based framework for the classification of rice (paddy) leaf diseases using image data. The system integrates deep learning-based feature extraction with classical machine learning techniques to achieve accurate and interpretable disease detection. In addition, a severity estimation module is incorporated to provide insight into the progression stage of the disease.

## 2. Problem Statement
Rice crop diseases significantly impact agricultural productivity and food security. Early and accurate identification of these diseases is essential for effective crop management. Manual identification is time-consuming, subjective, and prone to error. Therefore, an automated and reliable system is required to assist in timely disease detection and classification.

## 3. Methodology

### 3.1 Image Preprocessing
- Contrast enhancement using CLAHE applied in LAB color space  
- Standardization of image size to 128×128 pixels  

### 3.2 Feature Extraction
A hybrid feature extraction approach was adopted:
- Deep Features: MobileNetV2 (pretrained and frozen model)
- Texture Features: GLCM and Local Binary Patterns (LBP)
- Shape Features: Histogram of Oriented Gradients (HOG)
- Color Features: HSV-based color moments

### 3.3 Feature Processing
- Standardization using StandardScaler  
- Dimensionality reduction using PCA retaining 95% variance  

### 3.4 Classification Models
The following machine learning models were evaluated:
- Random Forest Classifier (final selected model)
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes  

### 3.5 Severity Estimation
A rule-based approach using HSV segmentation was implemented to estimate disease severity and categorize infection levels as:
- Healthy / Very Early Stage  
- Early Stage  
- Mid Stage  
- Advanced Stage  

## 4. Results
The proposed system demonstrated strong performance on unseen test data, achieving high classification accuracy with minimal overfitting. The model exhibited consistent performance across all disease categories. Furthermore, the severity estimation module provided meaningful interpretability regarding disease progression.

## 5. Key Features
- Hybrid feature extraction combining deep and handcrafted features  
- Multi-model evaluation and comparison  
- Dimensionality reduction using PCA  
- Disease severity estimation for interpretability  
- Robust performance on real-world dataset
  
## 6. Tools and Technologies
- Python  
- OpenCV  
- TensorFlow (MobileNetV2)  
- Scikit-learn  
- NumPy, Pandas  
- Matplotlib, Seaborn  
- Scikit-image  

## 7. Future Scope
- Deployment in mobile applications for farmers  
- Integration with drone-based agricultural monitoring systems  
- Real-time disease detection in field conditions  
- Enhancement using end-to-end deep learning architectures  
