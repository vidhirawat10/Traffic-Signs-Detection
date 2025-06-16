# 🚦 Traffic Signs Detection

Welcome to the **Traffic Signs Detection** project! This repository contains a deep learning approach to identify and classify various traffic signs from images using Convolutional Neural Networks (CNNs).

---

## 📑 Table of Contents

- [About](#about)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributors](#contributors)
- [License](#license)

---

## 🧠 About

The goal of this project is to build a model capable of recognizing traffic signs to enhance autonomous vehicle systems and driver assistance applications. The project was developed as part of an internship assignment.

---

## 📂 Dataset

- **Source:** [German Traffic Sign Recognition Benchmark (GTSRB)](https://benchmark.ini.rub.de/gtsrb_news.html)
- **Classes:** 43 unique traffic sign categories.
- **Size:** ~50,000 images with annotations.
- **Preprocessing:**  
  - Resized to 32x32 pixels  
  - Normalized pixel values  
  - One-hot encoded labels  

---

## 🧰 Model Architecture

The model is built using TensorFlow/Keras with the following architecture:

Input Layer (32x32x3)<br>
→ Conv2D (32 filters, 3x3)<br>
→ ReLU<br>
→ MaxPooling (2x2)<br>
→ Conv2D (64 filters, 3x3)v
→ ReLU<br>
→ MaxPooling (2x2)<br>
→ Flatten<br>
→ Dense (128)<br>
→ Dropout (0.5)<br>
→ Output Layer (Softmax - 43 classes)<br>


---

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/vidhirawat10/Traffic-Signs-Detection.git
cd Traffic-Signs-Detection

# Install required packages
pip install -r requirements.txt
```
Or run directly in Google Colab using the .ipynb notebook.

---

## 🚀 Usage
Run the model training and evaluation notebook:
```bash
# In Jupyter Notebook or Google Colab
Open: Intern_TrafficSignDetect_Assignment.ipynb
Run all cells step-by-step
```

To use the trained model for prediction:

```bash
from tensorflow.keras.models import load_model
import cv2
import numpy as np

model = load_model('traffic_sign_model.h5')
img = cv2.imread('test_image.png')
img = cv2.resize(img, (32, 32)) / 255.0
prediction = model.predict(np.expand_dims(img, axis=0))
print("Predicted Sign Class:", np.argmax(prediction))
```

---

## 📈 Results
Metric	Value
Training Acc.	88.7%
Test Acc.	85.3%
Loss	0.15

Confusion matrix and detailed analysis available in:
📄 Analysis Report.pdf

---

## 🙋‍♀️ Contributor
@vidhirawat10

---

## ⭐️ Show Your Support
If you liked this project, feel free to ⭐️ the repository and share it !!

---
