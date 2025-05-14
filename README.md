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

#### 🔍 Step 1: Damage Detection with Detectron2
- Used Mask R-CNN via Detectron2 to locate car damage areas.
- Dataset annotations follow COCO format.
- Outputs include bounding boxes, masks, and class labels.


