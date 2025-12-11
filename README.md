# 🧠 Classifying Alzheimer’s Disease from MRI Scans Using CNNs

This project applies deep learning and machine learning methods to classify Alzheimer's disease from MRI brain scans. The goal is to support earlier and more accurate detection by improving how structural changes in the brain are interpreted. Models implemented include a custom CNN, MobileNet, KNN, and Random Forest.

---

## 📌 Project Overview

Alzheimer’s disease is a progressive neurological disorder and the leading cause of dementia. MRI scans can reveal structural changes such as brain atrophy and gray matter loss, making them useful for early detection even though they cannot provide a definitive diagnosis.

This project classifies MRI images into four categories:

- Non Demented  
- Very Mild Demented  
- Mild Demented  
- Moderate Demented  

Improving classification accuracy can support better clinical decision-making and earlier intervention.

---

## 📁 Dataset

The dataset is a publicly available Alzheimer’s MRI dataset hosted on Kaggle. It includes both original and augmented MRI images separated into four classes.

### Preprocessing Steps

- Resized all images to 224 × 224  
- Normalized pixel values to [0, 1]  
- Batched datasets for efficient training  
- Applied random horizontal and vertical flips  
- Adjusted brightness and contrast  
- Cached and prefetched data to optimize training speed  

These steps help improve generalization and reduce training bottlenecks.

---

## 🧩 Models Implemented

### 1. 🧱 Custom CNN  
A lightweight convolutional neural network built with:

- Four convolutional layers  
- Max pooling layers  
- Flatten layer and dense layers  
- Dropout regularization  

This model serves as a strong baseline and performs well despite its simplicity.

---

### 2. ⚡ MobileNet (Transfer Learning)  
MobileNet achieved the highest overall performance. It includes:

- Pretrained ImageNet weights  
- Depthwise separable convolutions  
- Global average pooling  
- Batch normalization  
- Dropout layers  

MobileNet reached about 99% accuracy and precision, making it the top-performing model.

---

### 3. 📊 Traditional Machine Learning Models

The project also implements:

- K Nearest Neighbors (KNN)  
- Random Forest with PCA  

These provide baselines to compare against deep learning approaches. Accuracies ranged from 76% to 79%.

---

## 📈 Performance Summary

Key performance highlights:

- MobileNet achieved the strongest results across all metrics  
- The custom CNN achieved about 91% accuracy  
- Models with high learning rates or strong regularization showed instability  
- Traditional models performed significantly lower than CNN models  
- Most misclassifications occurred between Mild and Very Mild Demented categories  

---

## 🔍 Key Findings

- Lightweight models often outperform deeper networks for this dataset  
- Smaller CNNs trained faster and generalized better  
- High learning rates can lead to unstable training  
- Batch normalization and dropout improved model performance  
- Efficient model design matters more than excessive depth  

---

## ✅ Conclusion

Deep learning models, especially MobileNet and custom CNNs, provide highly accurate classification of Alzheimer’s stages from MRI scans. Lightweight architectures are both effective and computationally efficient, making them strong candidates for real-world medical diagnostic support.

---

## 📚 References

A complete list of references is included in the accompanying written report.

---
