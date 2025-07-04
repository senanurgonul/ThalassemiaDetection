# ThalassemiaDetection

**ThalassemiaDetection** is a project designed to classify various subtypes of **thalassemia** using routine blood test (CBC) data. The aim is to enable accurate and early diagnosis using only hematological values—without the need for genetic testing—thus contributing to clinical decision support systems.

---

## 🎯 Project Goals

Thalassemia is a hereditary blood disorder, particularly prevalent in the Mediterranean, Middle Eastern, and Southeast Asian regions. The goals of this project are:

- Accurately classify thalassemia and its subtypes using CBC data without relying on genetic tests  
- Provide an accessible and low-cost pre-diagnostic tool for clinical settings  
- Evaluate multiple classification models to determine the most effective approach  
- Enhance model interpretability to support physicians in clinical decision-making  

Correct classification of thalassemia is crucial for developing treatment plans and identifying carriers. This project aims to deliver a high-impact system in terms of both medical accuracy and practical usability.

---

## 🧬 Dataset

The dataset was obtained from a collaborative academic study conducted in Thailand and is available for academic use only.

### 📂 Files

- `csv_result-Train90.csv` — Training data  
- `csv_result-Test90.csv` — Test data

### 📊 Features (CBC Parameters)

- **MCV (Mean Corpuscular Volume):** Distinguishing factor in thalassemia and iron-deficiency anemia  
- **MCH, MCHC:** Hemoglobin concentration  
- **HbA2:** Key marker for beta-thalassemia carriers  
- **HbE, HbF, Hb Bart’s:** Special hemoglobin types crucial in subtype classification  
- **HbA0, Hb D/S/CS/C:** Help distinguish other variants  

### 📌 Data Cleaning & Preparation

- Removed rare classes (e.g., < 5 samples)  
- Balanced minority classes using SMOTE  
- Downsampled overrepresented classes (4000 → 500)  
- Prevented data leakage and duplicate records  
- Ensured balanced train/test split using stratified sampling  

The dataset contains **11 classes**, covering both common and rare thalassemia subtypes.


---


## 🚀 Installation & Usage

1. Install required packages:

```bash
pip install pytorch-tabnet scikit-learn pandas matplotlib imblearn
```

2. Run the notebook:

```bash
jupyter notebook Untitled12.ipynb
```

You can load data, train models, and analyse results by following the steps in the notebook.

---

This project aims to produce a model that not only achieves accuracy but also **produces clinically reliable and interpretable results**. The model's most successful output, **TabNet**, has attracted attention for its accuracy and interpretability.

