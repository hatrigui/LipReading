# Lip Reading Project

## Description
This repository explores various approaches to lip reading, leveraging both traditional machine learning and deep learning methods. The aim is to develop models that accurately interpret lip movements, contributing to advancements in visual speech recognition.

---

## Contents
### **1. Traditional Approaches**

- **Classical Machine Learning Approach.ipynb**  
  Implements a classical machine learning pipeline using HOG (Histogram of Oriented Gradients) features and SVM (Support Vector Machine) classifiers for lip reading.

- **haarcascade_frontalface_default.xml**  
  Pre-trained Haar Cascade model for face detection.

- **haarcascade_mcs_mouth.xml**  
  Pre-trained Haar Cascade model for mouth detection.

- **Deep Learning Approach.ipynb**  
  Explores deep learning models for lip reading, incorporating modern neural network architectures.

- **LipReading.ipynb**  
  Contains initial manipulations and explorations with traditional deep learning techniques.

---

### **3. Resources and Documentation**

- **lip reading.pdf**  
  The Presentation

- **Paper.pdf**  
  A research paper called **Lip reading using CNN and LSTM** used as a reference or guide for the traditional methodologies.

---

## 🚀 **Key Sections and Contributions**  

### **Problem Statement**  
#### **Hearing Loss & Speech Disorders**:  
- Over 430 million people globally experience hearing loss, projected to rise to 700 million by 2050.  
- 15.3% of children suffer from speech disorders.  

#### **Challenges in Lip Reading**:  
- **Viseme Ambiguity**: Multiple phonemes map to a single viseme (e.g., 23 consonants grouped into 5 visual categories).  
- **Coarticulation Effects**: Overlapping mouth movements between syllables.  
- **Human Limitations**: Hearing-impaired individuals achieve only ~17% accuracy in word recognition.

---

### **Approaches to Lip Reading**

#### **Traditional Methods**  
- **Two-stage Pipelines**: Hand-engineered features (e.g., HOG) + classifiers like SVM.  
- **Results**: Achieved 47.65% accuracy after hyperparameter tuning on a custom dataset (3,000 instances).  

#### **Deep Learning Methods**  
- **VGG16 + LSTM**: Feature extraction using pretrained VGG16, followed by LSTM for sequence learning.  
- **Challenges**: Overfitting due to small dataset, failure to handle temporal dependencies effectively.

#### **LipNet (Breakthrough Model)**  
- **End-to-End Architecture**: Combines Spatiotemporal CNNs (STCNN), Bidirectional LSTMs, and CTC loss for sentence-level prediction.  
- **GRID Corpus**: Trained on structured sentences (e.g., "Place blue at C 9 now").  

---

### **Technical Innovations**

- **Spatiotemporal Convolutions (STCNN)**: Captures both spatial (lip shape) and temporal (movement) features.  
- **CTC Loss**: Aligns variable-length input frames (video) with output text, handling misalignments and repetitions.  
- **Bidirectional LSTMs**: Model temporal dependencies in both forward and backward directions.

---

### **Results and Limitations**  

#### **Traditional Approaches**:  
- Accuracy plateaued at ~47% due to fragmented pipelines and handcrafted features.  

#### **LipNet**:  
- Achieved state-of-the-art (SOTA) performance in 2016 with 86% accuracy.  
- Later surpassed by newer models (e.g., LCANet, WAS).

#### **Challenges**:  
- Small datasets (e.g., MIRACL-VC1) leading to overfitting.  
- High computational demands (e.g., GRID Corpus requires significant memory).

---

### **Future Directions**  

- **Multilingual and Generalizable Models**: Adapting LipNet for diverse languages and real-world conditions.  
- **Medical Applications**: Early detection of Parkinson’s disease or jaw anomalies through facial gesture analysis.  
- **Efficiency Improvements**: Developing lightweight models (e.g., Small Vision-Language Models) for practical deployment.  
- **Integration with LLMs**: Enhancing text prediction using large language models.
