
---

# 🌿 CropDoc: Plant Disease Classification using ResNet-9

**CropDoc** is an end-to-end Deep Learning solution designed for the rapid and accurate identification of plant diseases. Developed as a Final Year Project for a BS in Data Science, the system utilizes a customized, lightweight **ResNet-9** architecture to achieve high performance on mobile and edge devices.

---

## 👥 Project Team

* **Students:** Hamza Shahid, Hottam ud din, Tariq jamil
* **Supervisor:** Dr. Bahar Ali
* **Institution:** BS Data Science
* **Date:** February 2026

---

## 🚀 Key Innovations & Results

* **Optimized Architecture:** Selected ResNet-9 (6.6M parameters) over VGG-16 and ResNet-18 for the best balance of speed and accuracy.
* **High Performance:** Achieved **98.62% Validation Accuracy** and **100% Test Accuracy**.
* **Efficient Training:** Used the **OneCycleLR** scheduler to reach target accuracy in just 20 epochs—2x faster than baseline methods.
* **Explainable AI (XAI):** Integrated **Grad-CAM** to visualize which parts of the leaf (spots, lesions) the model focuses on, building user trust.
* **Deployment Ready:** Exports to both **PyTorch (.pth)** and **ONNX** formats for mobile and web integration.

---

## 📊 Architecture Comparison

We benchmarked several architectures to justify the use of ResNet-9 for mobile agriculture applications:

| Architecture | Parameters | Accuracy | Inference (ms) | Mobile Friendly |
| --- | --- | --- | --- | --- |
| VGG-16 | 138M | 97.2% | 150 | ❌ |
| ResNet-18 | 11.7M | 98.8% | 60 | ⚠️ |
| **ResNet-9 (Ours)** | **6.6M** | **98.6%** | **45** | ✅ |
| MobileNetV2 | 3.5M | 97.5% | 30 | ✅ |

---

## 🧪 Fine-Tuning Experiments

To find the optimal training strategy, we conducted 5 distinct experiments:

1. **Baseline:** Constant Learning Rate (0.001) → 96.8% Accuracy.
2. **Config 1:** StepLR + Weight Decay → 98.1% Accuracy.
3. **Config 2:** CosineAnnealing → 98.3% Accuracy.
4. **Config 3 (Winner):** **OneCycleLR** → **98.6% Accuracy** (Reached 98% in only 20 epochs).
5. **Config 4:** OneCycleLR + Enhanced Augmentation → 98.4% Accuracy.

---

## 🛠️ Technical Stack

* **Language:** Python
* **Framework:** PyTorch
* **Data Processing:** OpenCV, Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Deployment:** ONNX Runtime

---

## 📈 Real-World Impact

* **Economic:** Potential to save significant agricultural costs by preventing crop loss.
* **Environmental:** Supports a 30-40% reduction in pesticide use through targeted diagnosis.
* **Social:** Provides accessible, high-tech diagnostics to rural farmers with budget smartphones.

---

## 📂 Project Structure

* `Setup & Imports`: Library configuration and reproducibility seeds.
* `Dataset Exploration`: Analysis of 38 plant disease classes from the PlantVillage dataset.
* `ResNet-9 Implementation`: Custom architecture with residual skip connections to prevent vanishing gradients.
* `Grad-CAM`: Visual explanation module.
* `Deployment`: Model serialization for production.

---

