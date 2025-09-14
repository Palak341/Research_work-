# Baby Cry Detection using SimCLR and Scalogram Images (ResNet-18 Encoder)

## 📌 Overview
This repository contains the implementation of a **self-supervised learning approach** for **baby cry detection**.  
We use **SimCLR pretraining** on scalogram images (generated from infant cry audio signals) and fine-tune a **ResNet-18 encoder** for classification.  

The objective is to detect and classify baby cries (e.g., hunger, pain, discomfort), supporting caregivers and advancing healthcare applications.

---

## 🧪 Methodology
1. **Data Preprocessing**
   - Infant cry audio samples are transformed into **scalogram images** using Continuous Wavelet Transform (CWT).
   - Images are normalized and resized for ResNet-18 input.

2. **SimCLR Pretraining**
   - A contrastive learning framework (SimCLR) is used with data augmentations such as cropping, color jitter, and Gaussian blur.
   - Encoder: **ResNet-18** (backbone without classification head).
   - Projection head added during pretraining.

3. **Supervised Fine-Tuning**
   - Pretrained ResNet-18 encoder is fine-tuned with labeled scalogram images.
   - A classification head is attached for downstream baby cry classification.

4. **Evaluation**
   - Metrics used: **Accuracy, Precision, Recall, and F1-score**.
   - Performance compared against models trained from scratch.

---


