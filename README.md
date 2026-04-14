# 🚦 Traffic Sign Recognition using Deep Learning

## 📌 Project Overview

This project explores the application of **Deep Learning techniques** for traffic sign classification using the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset.

Multiple deep learning models were implemented and compared to analyze their performance on real-world image data. The project focuses not only on accuracy but also on **model behavior, overfitting, and error analysis**.

---

## 📊 Dataset Description

The dataset consists of **43 different traffic sign classes** used in real-world road scenarios.

### 📁 Dataset Features:
- **Image Type:** Traffic sign images  
- **Format:** RGB  
- **Classes:** 43 categories  

### 🔄 Variations:
- Lighting conditions  
- Different angles and distances  
- Background noise  

👉 The dataset reflects real-world driving conditions, making the task challenging.

---

## ⚙️ Preprocessing Steps

To prepare the dataset:

- **Image Resizing:**
  - `30×30` (LeNet)
  - `32×32 / 224×224` (other models)

- **Normalization:**
  ```python
  image = image / 255.0
