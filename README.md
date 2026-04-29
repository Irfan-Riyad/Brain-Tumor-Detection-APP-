# 🧠 Brain Tumor Detection App

A deep learning-powered web application for automated brain tumor detection and classification using MRI images. This application leverages convolutional neural networks (CNN) to assist medical professionals in identifying brain tumors with high accuracy.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0%2B-orange?logo=tensorflow)
![Streamlit](https://img.shields.io/badge/Streamlit-1.0%2B-red?logo=streamlit)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 Overview

Brain tumors are one of the most critical health challenges worldwide. Early and accurate detection can significantly improve patient outcomes. This application uses advanced deep learning techniques to automatically classify brain MRI images and detect the presence of tumors.

The system is designed to:
- **Assist medical professionals** in diagnosis by providing AI-powered predictions
- **Achieve high accuracy** through state-of-the-art neural networks
- **Provide user-friendly interface** via web application
- **Support multiple tumor classifications** for comprehensive analysis

**Note**: This tool is designed to assist medical professionals and should not be used as the sole diagnostic tool.

---

## ✨ Features

- ✅ **Real-time Image Analysis** - Upload and analyze MRI images instantly
- ✅ **Multi-class Classification** - Identifies different types of brain tumors
- ✅ **High Accuracy** - Trained on extensive medical imaging datasets
- ✅ **User-Friendly Interface** - Built with Streamlit for easy accessibility
- ✅ **Detailed Predictions** - Provides confidence scores and probability distributions
- ✅ **Batch Processing** - Analyze multiple images at once
- ✅ **Interactive Visualizations** - View images and results side-by-side
- ✅ **Fast Processing** - GPU-optimized inference

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|-----------|
| **Backend** | Python 3.8+ |
| **Deep Learning Framework** | TensorFlow / Keras |
| **Web Framework** | Streamlit |
| **Image Processing** | OpenCV, Pillow, NumPy |
| **Data Science** | Pandas, Scikit-learn |
| **Visualization** | Matplotlib, Plotly |

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Virtual environment (recommended)

### Steps

1. **Clone the repository**
```bash
git clone https://github.com/Irfan-Riyad/Brain-Tumor-Detection-APP-.git
cd Brain-Tumor-Detection-APP-
```

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Download the pre-trained model**
- Download the model from [this link](https://drive.google.com/drive/u/0/folders/1y9bTLNtT64yyx2d4Kj57KI7zuhbXCwdo)
- Place it in the `models/` directory

---

## 🚀 Usage

### Running the Application

```bash
streamlit run app.py
```

The application will open in your default browser at `http://localhost:8501`

### How to Use

1. **Upload an MRI Image**
   - Click on the file uploader
   - Select a brain MRI image (JPEG, PNG, or other standard image formats)

2. **View Results**
   - The application will process the image
   - Results will show:
     - Original and preprocessed images
     - Prediction class (Tumor / No Tumor / Tumor Type)
     - Confidence score

3. **Interpret the Output**
   - **Confidence Score**: Indicates how confident the model is about the prediction
   - **Visualization**: Side-by-side comparison of original and processed images

---

## 🧠 Model Architecture

### CNN Model Details

The model uses a **Convolutional Neural Network (CNN)** architecture optimized for medical image analysis:

```
Input Layer (224 × 224 × 3)
    ↓
Convolutional Blocks (32, 64, 128 filters)
    ↓
Max Pooling Layers
    ↓
Dropout Layers (Regularization)
    ↓
Fully Connected Layers
    ↓
Output Layer (Softmax)
```

### Key Features
- **Transfer Learning**: Fine-tuned on medical imaging datasets
- **Data Augmentation**: Improved generalization through augmentation
- **Regularization**: Dropout and L2 regularization to prevent overfitting
- **Batch Normalization**: Stabilized training

---

## 📊 Dataset

The model is trained on a comprehensive brain tumor MRI dataset including:

- **Classes**: 
  - Glioma
  - Meningioma
  - Pituitary
  - No Tumor

- **Dataset Size**: [Specify your dataset size]
- **Train/Validation/Test Split**: 70% / 15% / 15%
- **Preprocessing**: Normalization, Resizing to 224×224

**Dataset Source**: [Specify dataset source or link]

---

## 📈 Results

### Model Performance

| Metric | Value |
|--------|-------|
| **Accuracy** | [Your accuracy]% |
| **Precision** | [Your precision]% |
| **Recall** | [Your recall]% |
| **F1-Score** | [Your F1-score] |

### Confusion Matrix & ROC Curve
- [Include visualization descriptions or links]

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open a Pull Request**

### Guidelines
- Follow PEP 8 coding standards
- Add descriptive commit messages
- Update documentation for new features
- Test your changes thoroughly

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 👤 Contact & Support

- **Author**: Irfan Riyad
- **GitHub**: [@Irfan-Riyad](https://github.com/Irfan-Riyad)
- **Project Link**: [Brain Tumor Detection App](https://github.com/Irfan-Riyad/Brain-Tumor-Detection-APP-)
- **Live Demo**: [Streamlit App](https://brain-iccit-mryummflnwm76tphvrajyg.streamlit.app/)

### Issue Reporting
Found a bug? Have a suggestion? Please [open an issue](https://github.com/Irfan-Riyad/Brain-Tumor-Detection-APP-/issues)

---

## ⚠️ Disclaimer

**This application is for research and educational purposes only.** It should not be used as a replacement for professional medical diagnosis. Always consult with qualified medical professionals for actual medical diagnosis and treatment.

---

## 🙏 Acknowledgments

- TensorFlow and Keras communities
- Streamlit for the amazing web framework
- Medical imaging research community
- All contributors and users

---

**Made with ❤️ by Irfan Riyad**
