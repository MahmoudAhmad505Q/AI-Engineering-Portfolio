# 🌍 EuroSAT Satellite Image Classification (Computer Vision)

## 📌 Project Overview
Analyzing satellite imagery is vital for urban planning, agriculture, and environmental monitoring. This project focuses on classifying land cover from satellite images into 10 distinct categories (e.g., Forests, Highways, Industrial Areas, Rivers) using state-of-the-art Deep Learning techniques.

**Key Achievement:** Implemented **Transfer Learning** using a pre-trained **ResNet18** architecture, customized and fine-tuned to classify remote sensing data with exceptional accuracy.

## 🛠️ Tech Stack & Tools
* **Deep Learning Framework:** PyTorch, Torchvision
* **Model Architecture:** ResNet18 (Transfer Learning)
* **Image Processing:** PIL (Python Imaging Library), Matplotlib
* **Optimization Techniques:** Learning Rate Schedulers (`ReduceLROnPlateau`), Model Checkpointing

## 🧠 The Computer Vision Pipeline

### 1. Advanced Data Augmentation & Loading
* Utilized `torchvision.transforms` to apply real-time data augmentation, including random rotations and horizontal/vertical flips. This made the model robust to different satellite angles and orientations.
* Built custom PyTorch `Dataset` and `DataLoader` pipelines to efficiently feed large batches of high-resolution images into the GPU for training.

### 2. Transfer Learning (ResNet18)
* Loaded a pre-trained `ResNet18` model, which had already learned complex feature extraction from millions of images.
* Modified the final Fully Connected (FC) layer to output exactly 10 classes corresponding to the EuroSAT land cover categories.

### 3. Professional Training Loop
* Implemented a professional-grade training and validation loop.
* **Dynamic Learning Rate:** Integrated a learning rate scheduler that automatically reduces the learning rate when the model's improvement plateaus, ensuring optimal convergence.
* **Model Checkpointing:** Wrote automated logic to track validation loss and securely save (`torch.save`) the best-performing model weights during training (`best_resnet_eurosat.pth`).

## 💡 Business Value
This project showcases advanced capabilities in Computer Vision, proving readiness to tackle complex visual data problems. The techniques used here are directly transferable to medical image analysis, automated quality control in manufacturing, and intelligent geographic information systems (GIS).
