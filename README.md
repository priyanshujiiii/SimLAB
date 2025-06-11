# 🔍 Deep Research on Pretrained Model Performance for Seismic Image Denoising

This project conducts an in-depth study of how various **pretrained image classification models** perform when used as **encoders** for seismic image **denoising** tasks. Our architecture follows an **encoder-decoder** structure where:

- **Encoder** = pretrained model (e.g., EfficientNet, DenseNet, etc.)
- **Decoder** = [UNet++](https://arxiv.org/abs/1912.05074), chosen for its dense skip connections and superior performance in preserving structural information during segmentation tasks.

---

## 🧠 Problem Statement

Seismic images often contain noise that can obscure important geological structures. Our objective is to:

> **Denoise seismic images using a hybrid deep learning pipeline that leverages powerful pretrained encoders with a UNet++ decoder.**

---

## 🎯 Goals

- Evaluate the performance of **state-of-the-art pretrained models** as encoders on seismic image denoising.
- Analyze how different encoder backbones affect the **structure preservation** capability of UNet++.
- Compare performances to identify **top-performing models**.

---

## 📌 Methodology

1. **Task**: Image Denoising (Preserving key structures)
2. **Model Architecture**: Encoder–Decoder  
   - Encoder: Pretrained classification model (from torchvision or timm)
   - Decoder: UNet++
3. **Dataset**: Seismic image dataset from [Think-Towards Challenge](https://www.kaggle.com/competitions/tgs-salt-identification-challenge)
4. **Loss Functions**: Binary Cross Entropy + Dice Loss
5. **Evaluation Metrics**: PSNR, SSIM, IoU

---

## 🧱 Models Evaluated

| Model              | Year | Type       |
|-------------------|------|------------|
| AlexNet           | 2012 | CNN        |
| VGG               | 2015 | CNN        |
| ResNet            | 2015 | CNN        |
| DenseNet          | 2016 | CNN        |
| ShuffleNet V2     | 2016 | CNN        |
| MobileNet V1/V2   | 2017 | CNN        |
| EfficientNet      | 2018 | CNN        |
| EfficientNet V2   | 2019 | CNN        |
| RegNet            | 2020 | CNN        |
| ConvNeXt          | 2021 | CNN        |
| RexNet            | 2020 | CNN        |
| MaxViT, Swin, ViT | 2020–2022 | ❌ *Not tested (resource constraints)* |

---

## 🏆 Key Findings

- ✅ **Top Performers**:  
  - **RexNet**
  - **DenseNet**
  - **EfficientNetV2**

- ❌ **Transformers** (e.g., Swin, ViT, MaxViT) were **excluded** due to computational limitations.

---

## 💡 Why UNet++?

We chose **UNet++** for its dense connections that enhance gradient flow and structural fidelity—ideal for segmentation-like tasks such as denoising, especially when retaining the underlying patterns in seismic data is crucial.

---

## 📊 Results & Visuals

Based on our experiments, the following encoder backbones performed best when paired with the UNet++ decoder for seismic image denoising:

- ✅ **RexNet**
- ✅ **DenseNet**
- ✅ **EfficientNetV2**

### 📸 Visual Results of Top Performers

| Model           | Sample Output |
|----------------|---------------|
| **RexNet**      | (![image](https://github.com/user-attachments/assets/84d1bdb5-e210-4a12-b78e-4c87dac46d92)
) |
| **DenseNet**    | (![image](https://github.com/user-attachments/assets/0f3b7690-4323-4264-b2f3-bfbe290f62e3)
) |
| **EfficientNetV2** | (![image](https://github.com/user-attachments/assets/e6f42080-fb64-4d2f-a7bd-0d2f5d27813c)
) |

📑 [View Full Slide Deck with All Experiments (PDF)](https://github.com/priyanshujiiii/SimLAB/blob/main/Notebook/Seismic%20Image%20Labarortory.pdf)
---

