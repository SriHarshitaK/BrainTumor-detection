# 🧠 Brain Tumor Detection using VGG19

> A Deep Learning project to classify brain tumors using MRI images with a Tkinter GUI frontend.

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-brightgreen)

---

## 🎯 Overview

This project leverages **Transfer Learning** with the pre-trained **VGG19** Convolutional Neural Network to classify MRI brain scans into four categories:

* **Glioma Tumor**
* **Meningioma Tumor**
* **Pituitary Tumor**
* **No Tumor**

It includes a **Tkinter-based GUI** that allows users to upload MRI scans and get instant predictions with labels.

---

## 🖼️ Demo

| GUI Upload Interface                 |
| ------------------------------------ | 
| <img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/44070c2b-01ef-4627-a01d-e35a2baf2019" />|
| Prediction Output                        |
| <img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/f04bebd7-d32d-4623-b78f-216cb5c6d5df" />|
 

---

## 📚 Table of Contents

* [Project Structure](#-project-structure)
* [Installation](#-installation)
* [Usage](#-usage)
* [Model Training](#-model-training)
* [Results](#-results)
* [Dataset](#-dataset)
* [Model Architecture](#-model-architecture)
* [Future Enhancements](#-future-enhancements)
* [Author](#-author)
* [License](#-license)

---

## 🗂️ Project Structure

```bash
├── archive/                # Dataset (Kaggle)
├── braintumor.py           # Model training script
├── gui.py                  # GUI interface using Tkinter
├── final_vgg19_brain_tumor.keras  # Trained model
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 🛠️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/brain-tumor-vgg19.git
cd brain-tumor-vgg19
```

2. **Create a virtual environment (optional but recommended)**

```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Ensure dataset is available in `archive/` folder** (from Kaggle)

---

## 🚀 Usage

### 🧪 Train the Model (optional, pre-trained model provided)

```bash
python braintumor.py
```

This trains the VGG19 model on the dataset and saves `final_vgg19_brain_tumor.keras`.

### 🖥️ Run the GUI for Predictions

```bash
python gui.py
```

* Click on `Upload` to select an MRI image.
* The model will classify it and show the predicted label.

---

## 📈 Results

| Metric   | Value      |
| -------- | ---------- |
| Accuracy | **92.35%** |
| Loss     | \~0.24     |



### Sample Predictions

| Input MRI                                                                                                                        | Predicted Label |
| ------------------------------------                                                                                             | --------------- |
|<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/6c773e8d-83cb-4dc2-9014-8c01e2bb6dbf" />| Pituitary Tumor |
|<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/ba9b7cc1-3683-42ba-932d-4ccce4892234" />| No Tumor        |

---

## 🧬 Model Architecture

We use **Transfer Learning** from VGG19 with frozen base layers and a custom head:

```
Base Model: VGG19 (include_top=False, weights='imagenet')

Head:
- Flatten
- Dense(256, activation='relu')
- Dropout(0.5)
- Dense(4, activation='softmax')
```

---

## 🗃️ Dataset

Kaggle Brain MRI Dataset:
🔗 [https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)

* **Training and Testing** images are pre-classified into folders.
* 4 Classes: `glioma`, `meningioma`, `pituitary`, `no tumor`
* <img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/75d23127-61c0-4575-9cc2-a50858f95e58" />


---

## 🌟 Future Enhancements

* [ ] ✅ Add Grad-CAM visualizations for model explainability
* [ ] 🌐 Deploy a Streamlit or Flask web app
* [ ] 📲 Convert to mobile app using Kivy or Flutter
* [ ] 💬 Add confidence score or probability for each prediction

---

## 👩‍💻 Author

**Sri Harshita**
📧 [ksriharshita04@gmail.com](mailto:your-email@example.com)
🌐 [LinkedIn](www.linkedin.com/in/sri-harshita-kasiraju) | [GitHub](https://github.com/SriHarshitaK)

---

