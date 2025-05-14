# 🚗 Car Damage Detection for Insurance Claims

## 🔍 Overview
Car Damage Detection for Insurance Claims is a computer vision-based system designed to assist insurance companies by automating the process of vehicle damage detection and classification from images. This helps reduce human effort and speeds up the claims process.

The system performs:

- Damage Detection using Detectron2 (Mask R-CNN).
- Damage Classification using a custom CNN model.
- Built and tested in Google Colab using Python.


## 🧠 Technologies Used

| Task                   | Tool/Library           |
|------------------------|------------------------|
| Damage Detection       | Detectron2 (Mask R-CNN) |
| Damage Classification  | TensorFlow / Keras CNN |
| Image Preprocessing    | OpenCV                 |
| Visualization          | Matplotlib, Seaborn    |
| Notebook Platform      | Google Colab           |


## 📁 Project Structure
```
Car-Damage-Detection/
│
├── detectron2_model/               # Damage detection using Detectron2
├── cnn_classifier/                 # CNN classification model
├── dataset/                        # Training/test data organized by labels
├── results/                        # Sample output images and charts
├── Damage_model_training.ipynb     # Detection training & experiments
├── Model.ipynb                     # End-to-end working pipeline
└── README.md                 
```

## 📦 Dataset Structure
The dataset is divided into labeled subfolders for classification and annotated masks/boxes for detection:
```
dataset/
├── train/
│   ├── dent/
│   ├── scratch/
│   ├── crack/
│   └── no_damage/
├── test/
│   ├── dent/
│   ├── scratch/
│   ├── crack/
│   └── no_damage/
└── annotations/  # COCO-style JSON for Detectron2
```

## ⚙️ How It Works

### 🔍 Step 1: Damage Detection with Detectron2
- Used Mask R-CNN via Detectron2 to locate car damage areas.
- Dataset annotations follow COCO format.
- Outputs include bounding boxes, masks, and class labels.

### 🧪 Step 2: Damage Classification using CNN
- Cropped the detected regions from step 1.
- Trained a CNN to classify images into:
  - Dent
  - Scratch
  - Crack
  - No Damage
- Used `ImageDataGenerator` for augmentation and model robustness.

## 📊 Results & Performance

### ✅ Detectron2 Detection:
* Model: Mask R-CNN (R50-FPN)
* Precision: High IoU and mAP for bounding boxes and segmentation masks
* Visualization: Boxes and masks plotted on car images

### 🧠 CNN Classification:
* Validation Accuracy: ~93%
* Optimizer: Adam
* Loss: Categorical Crossentropy
* Visualization: Confusion Matrix and Class-wise Accuracy


## 🚧 Future Enhancements
* Deploy a Streamlit Web App for real-time detection & classification.
* Introduce damage severity scoring (minor, moderate, major).
* Add explainable AI (XAI) for model transparency.
* Expand dataset with synthetic damage using augmentation.

## 👨‍💻 Author
**Ritesh Jillewad** <br>
14-05-2025
