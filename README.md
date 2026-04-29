# 🧠 Brain Tumor Detection App

A deep learning-powered web application for automated brain tumor detection and classification using MRI images. This application leverages convolutional neural networks (CNN) to assist medical professionals in identifying brain tumors with high accuracy.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0%2B-orange?logo=tensorflow)
![Streamlit](https://img.shields.io/badge/Streamlit-1.0%2B-red?logo=streamlit)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📋 Table of Contents

- [About](#about)
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Setup & Configuration](#setup--configuration)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 📖 About

The **Brain Tumor Detection App** is an innovative AI-powered healthcare solution designed to assist medical professionals in the early and accurate detection of brain tumors. This project demonstrates the practical application of deep learning in medical imaging.

### Project Goals:
- 🏥 **Support Healthcare Professionals** - Provide an AI assistant tool for medical diagnosis
- 🔍 **High Accuracy Detection** - Achieve state-of-the-art performance in tumor classification
- 🎓 **Advance Medical Research** - Contribute to AI in healthcare development
- 🌐 **Accessibility** - Make advanced medical imaging technology accessible to institutions worldwide

This is a research and educational initiative showcasing how machine learning can revolutionize medical diagnostics.

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

---

## ⚙️ Setup & Configuration

### Step 1: Download the Pre-trained Model

The application requires a pre-trained CNN model for inference. Follow these steps:

1. **Download the model file** from [this Google Drive link](https://drive.google.com/drive/u/0/folders/1y9bTLNtT64yyx2d4Kj57KI7zuhbXCwdo)
   - Look for the model file (typically `.h5` or `.pkl` format)
   - Download it to your computer

2. **Create the models directory** (if it doesn't exist)
   ```bash
   mkdir -p models
   ```

3. **Place the model in the correct location**
   ```
   Brain-Tumor-Detection-APP-/
   ├── models/
   │   └── your_model.h5  (Place downloaded model here)
   ├── app.py
   └── README.md
   ```

### Step 2: Download the Classes File

The `classes.txt` file contains the list of tumor classifications that the model uses.

1. **Download classes.txt** from [this Google Drive link](https://drive.google.com/drive/u/0/folders/1y9bTLNtT64yyx2d4Kj57KI7zuhbXCwdo)
   - Look for `classes.txt` in the shared folder

2. **Place it in the project root directory**
   ```
   Brain-Tumor-Detection-APP-/
   ├── classes.txt  (Place downloaded file here)
   ├── models/
   ├── app.py
   └── README.md
   ```

3. **Verify the classes file contains your tumor classifications**
   ```
   Glioma
   Meningioma
   Pituitary
   No Tumor
   ```

### Step 3: Upload Classes in the App

When running the app, you'll be prompted to upload the `classes.txt` file:

1. Click on the **"Upload classes.txt"** section in the sidebar
2. Select the `classes.txt` file from your computer
3. The app will automatically load the classification labels

---

## 🚀 Usage

### Running the Application

```bash
streamlit run app.py
```

The application will open in your default browser at `http://localhost:8501`

### How to Use

1. **Upload classes.txt** (First time setup)
   - Use the sidebar uploader to upload your `classes.txt` file
   - This defines all possible tumor classifications

2. **Upload an MRI Image**
   - Click on the file uploader
   - Select a brain MRI image (JPEG, PNG, or other standard image formats)
   - Supported formats: JPG, JPEG, PNG, BMP

3. **View Results**
   - The application will process the image
   - Results will show:
     - Original and preprocessed images
     - Prediction class (Tumor type or No Tumor)
     - Confidence score (probability percentage)
     - Classification breakdown for all classes

4. **Interpret the Output**
   - **Confidence Score**: Indicates how confident the model is about the prediction (0-100%)
   - **Visualization**: Side-by-side comparison of original and processed images
   - **Probability Distribution**: Bar chart showing predictions for all classes

### Testing with Sample Images

We recommend testing the app with sample brain MRI images before using actual medical data.

#### Option 1: Download Sample Images from Kaggle

We use the [Brain Tumor MRI Images dataset](https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-44c) from Kaggle:

**Steps to download:**
1. Visit: [https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-44c](https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-44c)
2. Click the **"Download"** button (requires Kaggle account)
3. Extract the downloaded ZIP file
4. Navigate to the appropriate folder:
   ```
   brain-tumor-mri-images/
   ├── Training/
   │   ├── glioma_tumor/
   │   ├── meningioma_tumor/
   │   ├── pituitary_tumor/
   │   └── no_tumor/
   └── Testing/
   ```

#### Option 2: Use Your Own Dataset

If you have your own brain MRI images:
1. Organize them by tumor type in separate folders
2. Place them in a `sample_images/` directory
3. Use them to test the application

#### Testing the App with Sample Images

1. **Create a test images folder** (optional)
   ```bash
   mkdir -p sample_images
   # Copy some MRI images here from Kaggle dataset
   ```

2. **Run the app and upload images**
   ```bash
   streamlit run app.py
   ```

3. **Upload an MRI image** from the Kaggle dataset
   - The model will analyze and provide prediction results
   - Compare the predictions with the actual labels

4. **Check the accuracy**
   - Verify predictions against the folder names
   - Test multiple images from different categories

#### Kaggle Dataset Details

- **Dataset Name**: Brain Tumor MRI Images
- **Total Images**: 7,023 MRI scans
- **Classes**: 4 (Glioma, Meningioma, Pituitary, No Tumor)
- **Size**: ~1.5 GB
- **Format**: JPEG images (512×512 pixels)
- **Kaggle Link**: [https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-44c](https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-44c)

**Note**: You need a Kaggle account to download the dataset. It's free to create one.

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

### Classes:
- 🧠 **Glioma** - Most common type of malignant brain tumor
- 🧠 **Meningioma** - Tumors of the brain's outer membrane
- 🧠 **Pituitary** - Tumors of the pituitary gland
- 🧠 **No Tumor** - Normal, healthy brain scans

### Dataset Specifications:
- **Primary Source**: [Brain Tumor MRI Images - Kaggle](https://www.kaggle.com/datasets/fernando2rad/brain-tumor-mri-images-44c)
- **Dataset Size**: 7,023 MRI images
- **Train/Validation/Test Split**: 70% / 15% / 15%
- **Image Resolution**: 512×512 pixels
- **Preprocessing**: Normalization, Resizing to 224×224

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
- Kaggle for providing the Brain Tumor MRI dataset
- All contributors and users

---

**Made with ❤️ by Irfan Riyad**
