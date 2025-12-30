# 🌾 Wheat Disease Binary Classifier (PyTorch)

This project is a **deep learning image classification system** that detects whether a wheat plant is **healthy** or **diseased** from an image. It is built using **PyTorch** and **EfficientNet-B0**, and is designed to be lightweight, practical, and deployable in real-world agricultural scenarios.

---

## 📌 Project Overview

Plant diseases significantly reduce crop yield and quality. Early detection allows farmers to react faster and reduce losses. This project uses a **Convolutional Neural Network (CNN)** to analyze images of wheat plants and predict:

* ✅ **Healthy**
* ❌ **Diseased**

The model outputs **probabilities**, not just labels, making it useful for decision support systems.

---

## 🧠 Model Architecture

* **Backbone:** EfficientNet-B0 (via `timm`)
* **Pretraining:** ImageNet (during training phase)
* **Custom Head:**

  * Fully connected layer → 1 output neuron
  * Sigmoid activation (binary classification)

```text
Image → EfficientNet-B0 → Linear(1280 → 1) → Sigmoid → Probability
```

---

## 🗂️ Dataset Structure

```text
wheat-plant-diseases/
├── data/
│   ├── train/
│   │   ├── healthy/
│   │   └── diseased/
│   ├── val/
│   │   ├── healthy/
│   │   └── diseased/
│   └── test/
│       ├── image1.jpg
│       ├── image2.jpg
│       └── ...
```

Images are resized to **128×128** and normalized using ImageNet statistics.

---

## 🚀 How to Run Inference

1. Load the trained model weights
2. Randomly select an image from the test directory
3. Predict health status
4. Visualize probabilities

Example output:

```text
Healthy: 0.82
Disease: 0.18
```

---

## 📊 Visualization

The project includes a visualization that shows:

* The original image
* A probability bar chart (Healthy vs Disease)

This makes predictions **interpretable**, not just numerical.

---

## 🌍 Real-World Applications

This project can be used in:

### 🌾 Agriculture

* Early disease detection in wheat fields
* Decision support for pesticide usage
* Crop health monitoring

### 📱 Mobile Applications

* Farmers take a photo → instant diagnosis

### 🚜 Smart Farming Systems

* Integrated with drones or field cameras
* Automated crop monitoring pipelines

### 🧪 Research & Education

* Plant pathology research
* Teaching applied computer vision

---

## 🛠️ Tech Stack

* Python
* PyTorch
* timm
* torchvision
* PIL
* Matplotlib

---

## 📈 Future Improvements

* Multi-class disease classification
* Grad-CAM heatmaps for explainability
* Mobile deployment (ONNX / TensorRT)
* Web API (FastAPI / Flask)
* Training on higher resolution images

---

## 👤 Author

**Darko Spasojevic**
Deep Learning & Data Analytics Enthusiast

---

## ⭐ Notes

This project demonstrates **end-to-end ML workflow**:

* Dataset handling
* Model design
* Training
* Saving/loading weights
* Inference & visualization

It is suitable for **portfolio presentation**, **internship applications**, and **real-world prototyping**.

---

If you want help deploying this as a **web app**, **API**, or **mobile solution**, feel free to ask.
