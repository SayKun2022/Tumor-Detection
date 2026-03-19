# Brain Tumor Detection

**Overview**

This project focuses on detecting and classifying brain tumors from MRI images using a deep learning model based on VGG16 (Transfer Learning). The model classifies images into four categories:

Pituitary Tumor
Glioma Tumor
No Tumor

**Features:-**

- Transfer Learning using VGG16
- Custom Image Augmentation (Brightness & Contrast)
- Batch Data Generator (memory efficient)
- Classification Report & Confusion Matrix
- Visualization of predictions with confidence score
- Simple tumor detection function for new images

**Dataset Structure:-**

archive/
│
├── Training/

│   ├── glioma/

│   ├── meningioma/

│   ├── pituitary/

│   └── notumor/
│

└── Testing/

    ├── glioma/
    
    ├── meningioma/
    
    ├── pituitary/
    
    └── notumor/

**Tech Stack:-**
Python 
TensorFlow / Keras
NumPy
Matplotlib
Seaborn
PIL (Image Processing)
Scikit-learn

**Model Architecture:-**

Pretrained VGG16 (ImageNet weights)
Frozen base layers (except last few)
Custom head:
Flatten
Dense (128, ReLU)
Dropout
Output Layer (Softmax)

**Data Pipeline:-**

Load image paths and labels
Shuffle dataset
Apply augmentation:
Brightness adjustment
Contrast adjustment
Normalize images
Generate batches using custom generator

**Training:-**
Optimizer: Adam
Learning Rate: 0.0001
Loss Function: Sparse Categorical Crossentropy
Metrics: Accuracy=
Epochs: 5

**Evaluation:-**
Classification Report
Confusion Matrix Visualization
Accuracy & Loss Plot

**Results:-**
Achieves good classification performance on MRI images
Handles multi-class tumor detection
Provides prediction confidence for better interpretability

**Future Improvements:-**
Add real-time web app (Streamlit / Flask)
Use advanced architectures (EfficientNet, ResNet)
