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
