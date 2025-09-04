# 👟 Fashion-MNIST Classification

This repository demonstrates **image classification on the Fashion-MNIST dataset** using three approaches:

1. **Neural Network (NN)** – Fully connected baseline  
2. **Convolutional Neural Network (CNN)** – Feature extraction with Conv layers  
3. **Transfer Learning (VGG-19)** – Leveraging pretrained ImageNet weights  

---

## 📂 Dataset

We use the **Fashion-MNIST dataset**, a modern alternative to MNIST:
- 70,000 grayscale images (28x28 pixels, 10 classes)
- 60,000 training + 10,000 test images
- Classes: *T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot*

---

## 🧠 Models

1. Neural Network (Baseline)
Flatten → Dense(128, ReLU) → Dense(64, ReLU) → Dense(10, Softmax)
Optimizer: Adam
Loss: Categorical Crossentropy
Expected Accuracy: ~83%


2. Convolutional Neural Network (CNN)
Conv2D → ReLU → MaxPooling → Dropout
Dense classifier at the end
Expected Accuracy: ~90–92%


3. Transfer Learning (VGG-19)

Resize 28x28 → 224x224x3
Pretrained VGG-19 on ImageNet
Custom dense layers on top
Freeze/unfreeze conv base
Expected Accuracy: ~93–95%


📌 Future Work

 Hyperparameter tuning with Optuna/W&B
 Explore ResNet, EfficientNet, MobileNet
 Add deployment with Streamlit/Gradio


---

## ⚙️ Installation

Clone this repo and install dependencies:

```bash
git clone https://github.com/your-username/fmnist-classification.git
cd fmnist-classification
pip install -r requirements.txt



