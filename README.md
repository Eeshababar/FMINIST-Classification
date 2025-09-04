# 👟 Fashion-MNIST Classification

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg) 
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg) 
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

This repository demonstrates **image classification on the Fashion-MNIST dataset** using five approaches:

- **Neural Network (NN)** – Fully connected baseline  
- **Convolutional Neural Network (CNN)** – From scratch conv layers  
- **Transfer Learning (VGG-19)** – Pretrained on ImageNet  
- **Transfer Learning (ResNet50)** – Pretrained residual network  
- **Transfer Learning (DenseNet121)** – Pretrained densely connected network  

---

## 📂 Dataset

We use the **Fashion-MNIST dataset**, a modern alternative to MNIST:

- 70,000 grayscale images (28×28 pixels, 10 classes)  
- 60,000 training + 10,000 test images  
- Classes: *T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot*  

---

## 🧠 Models

### 1️⃣ Neural Network (Baseline)
- `Flatten → Dense(128, ReLU) → Dense(64, ReLU) → Dense(10, Softmax)`  
- Optimizer: **Adam**  
- Loss: **Categorical Crossentropy**  
- Accuracy: ~87%  

---

### 2️⃣ CNN (Scratch)
- `Conv2D → ReLU → MaxPooling → Dropout → Dense classifier`  
- Accuracy: ~91%  

---

### 3️⃣ VGG-19 (Transfer Learning)
- Input resized: **28×28 → 224×224×3**  
- Backbone: `VGG19(include_top=False, weights="imagenet")`  
- Custom dense layers added  
- Accuracy: ~92%  

---

### 4️⃣ ResNet50 (Transfer Learning)
- Input: 224×224×3 (ImageNet preprocessing)  
- Backbone: `ResNet50(include_top=False, weights="imagenet")`  
- Head: GAP → Dense(10, Softmax)  
- Accuracy: ~92%  

---

### 5️⃣ DenseNet121 (Transfer Learning)
- Input: 224×224×3 (ImageNet preprocessing)  
- Backbone: `DenseNet121(include_top=False, weights="imagenet")`  
- Head: GAP → Dense(10, Softmax)  
- Accuracy: ~86%  

---

## 📊 Results

| Model          | Accuracy |
|----------------|----------|
| Neural Network | ~87%     |
| CNN            | ~91%     |
| VGG-19         | ~92%     |
| ResNet50       | ~92%     |
| DenseNet121    | ~86%     |

---

👩‍💻 Contributor: Eesha Tur Razia Babar


Clone this repo and install dependencies:

```bash
git clone https://github.com/your-username/fmnist-classification.git
cd fmnist-classification
pip install -r requirements.txt
