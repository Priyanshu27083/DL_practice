# 🚦 Traffic Sign Recognition using Deep Learning  

## 📌 Project Overview  
This project explores the application of Deep Learning techniques for traffic sign classification using the German Traffic Sign Recognition Benchmark (GTSRB) dataset.  

Multiple deep learning models were implemented and compared to understand their performance on real-world image data. The project focuses not only on accuracy but also on model behavior, overfitting, and error analysis.

---

## 📊 Dataset Description  

The dataset consists of 43 different traffic sign classes used in real-world road scenarios.

### 📁 Dataset Features:
- Image Type: Traffic sign images  
- Format: RGB  
- Classes: 43 categories  
- Variations:
  - Lighting conditions  
  - Angles and distances  
  - Background noise  

The dataset reflects real-world driving conditions, making the classification task challenging.

---

## ⚙️ Preprocessing Steps  

- Resized images:
  - 30×30 (LeNet)
  - 32×32 / 224×224 (other models)

- Normalized pixel values by scaling them between 0 and 1  

- Data split:
  - 70% Training Data  
  - 30% Validation/Test Data  

- Applied Data Augmentation (on training data only):
  - Rotation  
  - Width/Height Shifting  
  - Zoom  

The dataset was split to ensure proper model training and unbiased evaluation on unseen data.

---

## 🧠 Models Implemented  

### 1. LeNet-5  
- Lightweight CNN  
- Uses convolution layers, average pooling, and tanh activation  
- Performs efficiently on small images  

---

### 2. AlexNet  
- Deeper CNN architecture  
- Uses ReLU activation and larger filters  
- Fast learning but early saturation observed  

---

### 3. Custom CNN  
- Basic convolutional model  
- Used as baseline for comparison  

---

### 4. ZFNet  
- Improved version of AlexNet  
- Better feature extraction capability  
- Achieved highest accuracy among tested models  

---

### 5. Transfer Learning Models  
- VGG16  
- ResNet50  

These models were pretrained on large datasets and fine-tuned for traffic sign classification.

---

## ⚙️ Regularization Techniques  

- Dropout  
- Data Augmentation  
- Early Stopping  

### 🔑 Key Observation:
Dropout combined with data augmentation significantly improved generalization and reduced overfitting.

---

## 📈 Observations  

### 🔥 Overfitting in Basic LeNet
- Training Accuracy reached around 99%  
- Validation Accuracy remained around 88–90%  
- Indicates memorization of training data  

---

### ⚖️ Effect of Regularization
- Training accuracy decreased slightly  
- Validation accuracy improved (~91%)  
- Model generalized better  

---

### 🚀 Impact of Data Augmentation
- Validation accuracy improved further (~95–96%)  
- Model handled real-world variations more effectively  

---

### ⚡ AlexNet Behavior
- Rapid learning in early epochs  
- Validation accuracy plateaued early (~91%)  
- Struggled with fine distinctions between similar classes  

---

### 🧠 Model Complexity Insight
- Smaller models performed well on this dataset  
- Larger models required more data and training time  

---

### 🏆 Model Performance Comparison  

| Model | Accuracy |
|------|--------|
| ZFNet | ~96–97% |
| LeNet (Augmented) | ~95–96% |
| AlexNet | ~91–92% |
| CNN | ~90% |

---

## 🔍 Misclassification Analysis  

- Errors mainly occur in visually similar signs:
  - Speed limits (30 vs 50 vs 60)  
  - Similar shapes and colors  

Insight:  
The model struggles with fine-grained differences between closely related classes.

---

## 📊 Key Learnings  

- CNNs outperform basic models for image classification  
- Overfitting occurs without regularization  
- Data augmentation improves robustness  
- Model complexity should match dataset size  
- Analysis beyond accuracy is important  

---

## 🚀 Future Improvements  

- Apply explainable AI techniques (Grad-CAM)  
- Increase dataset size  
- Fine-tune pretrained models  
- Deploy as a real-time system  
- Improve classification of similar classes  

---

## 🛠️ Technologies Used  

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  
- Kaggle  

---

## 🧾 Conclusion  

This project demonstrates the effectiveness of deep learning models for traffic sign recognition. While simpler models like LeNet perform well, advanced models like ZFNet achieve higher accuracy. Regularization and data augmentation play a crucial role in improving model performance and generalization.

---

## ⭐ Unique Contribution  

This project focuses not only on accuracy but also on understanding model behavior through error analysis, overfitting detection, and performance comparison across different architectures.
