🧠 Project Description

PersoTrak – Person Detection with Faster R-CNN

This project implements a person detection system using the Faster R-CNN object detection framework.
The goal is to accurately detect and localize people in surveillance (CCTV) images or videos by drawing bounding boxes around detected individuals.

The notebook contains the end-to-end pipeline for training, validating, and testing a Faster R-CNN model using PyTorch.
It includes dataset preprocessing, augmentation, model training, performance evaluation using mAP (mean Average Precision), and visualization of detection results.

🔍 Key Features

Model: Faster R-CNN (based on ResNet backbone)

Framework: PyTorch & TorchVision detection API

Dataset: Custom dataset with “person” class annotations (VOC/COCO format)

Evaluation Metrics: mAP@50, mAP@50–95, Precision, Recall

Visualization: Bounding box visualization with confidence scores

Optional: Model inference on user-uploaded images

⚙️ Pipeline Overview

Dataset Preparation
Dataset loaded from custom directories and annotations converted to PyTorch-compatible format.

Data Augmentation & Transformation
Applied random flips, rescaling, and normalization to improve model generalization.

Model Training
Fine-tuning the Faster R-CNN model on the “person” dataset using SGD optimizer.

Evaluation
Computation of mAP, precision, and recall metrics after each epoch to track model performance.

Visualization
Bounding boxes are drawn on test images along with class labels and confidence percentages.

📊 Results Summary

mAP@50: 0.8649

mAP@50–95: 0.5434

Precision: 1.000

Recall: 1.000

Inference Speed: ~0.16 img/sec

These results indicate the model performs with high precision on the test dataset, although mAP@50–95 suggests further improvement could be made for varied IoU thresholds.

🧩 Repository Contents
📦 FasterRCNN-PersoTrak/
 ┣ 📜 Faster_RCNN_PersoTrak.ipynb      ← Main notebook
 ┣ 📂 src/
 ┃ ┣ 📜 engine.py                      ← Training & evaluation utilities
 ┃ ┣ 📜 utils.py                       ← Helper functions
 ┃ ┣ 📜 transforms.py                  ← Image augmentation/transformations
 ┃ ┗ 📜 config.py                      ← Configuration settings
 ┣ 📂 results/                         ← Detection samples & metrics plots
 ┣ 📜 requirements.txt                 ← Dependency list
 ┗ 📜 README.md                        ← Project documentation

🚀 How to Use

Clone the repository:

git clone https://github.com/username/FasterRCNN-PersoTrak.git
cd FasterRCNN-PersoTrak


Install dependencies:

pip install -r requirements.txt


Open and run the notebook:

Faster_RCNN_PersoTrak.ipynb


(Optional) Upload a custom image for testing:

The notebook includes a section for uploading an image and visualizing the detection results.

🧾 License

This project is released under the MIT License.
Feel free to use, modify, and distribute it with proper attribution.
