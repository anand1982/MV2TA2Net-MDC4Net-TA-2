# Lightweight Attention-Enhanced CNN for Multi-Class Plant Disease Classification

## Overview

This repository contains the complete implementation for the research paper:

**"Lightweight Attention-Enhanced Convolutional Learning Framework for Multi-Class Plant Disease Classification Across Diverse Crops"**

The proposed framework integrates:

* **MobileNetV2+Channel Attention**
* **MobileNetV2+Transformer Attention 1**
* **MobileNetV2+Transformer Attention 2**
* **(Mob+Den)+Channel Attention**
* **(Mob+Den)+Transformer Attention 1**
* **(Mob+Den)+Transformer Attention 2**
* **Channel attention module**

for efficient and robust multi-class plant disease classification under resource-constrained agricultural environments.

The framework is designed to capture:

* local disease texture patterns
* global contextual relationships
* channel-wise disease relevance

while maintaining low computational complexity.

---

## Dataset Description
![CCMT Dataset Sample Images](L-D.png)
The dataset used in this study contains leaf images from four crop species:

* cassava
* cashew
* maize
* tomato

Each crop contains multiple healthy and diseased classes.

### Dataset Directory Structure

dataset/
├── train/
│ ├── class_1/
│ ├── class_2/
│ ├── ...
├── validation/
│ ├── class_1/
│ ├── class_2/
│ ├── ...
├── test/
│ ├── class_1/
│ ├── class_2/
│ ├── ...

### Image Settings

* Image size: **224 × 224**
* Color mode: **RGB**
* File format: **JPG / PNG**

### Dataset Split

* Training: 80%
* Validation: 10%
* Testing: 10%

---

## Environment Requirements

### Software

* Python 3.10 or above
* TensorFlow 2.x
* NumPy
* Matplotlib
* scikit-learn
* Pandas
* OpenCV

### Hardware Used

* GPU: NVIDIA GPU recommended
* RAM: Minimum 8 GB

---

## Installation

Clone repository:

git clone https://github.com/anand1982/MV2TA2Net-MDC4Net-TA-2.git

Move to project folder:

cd yourrepository

Install dependencies:

pip install -r requirements.txt

---

## Requirements File

Example requirements:

tensorflow
numpy
matplotlib
scikit-learn
pandas
opencv-python

---

## Training Procedure

Run training script:

python train.py

### Default Training Parameters

* Epochs: 50
* Batch size: 32
* Learning rate: 0.0001
* Optimizer: Adam
* Loss function: categorical crossentropy

### Reproducibility Settings

Random seeds are fixed:

* NumPy seed = 42
* TensorFlow seed = 42

This ensures reproducibility of reported results.

---

## Testing Procedure

To test on unseen images:

python test.py --image sample_leaf.jpg

---

## Model Architecture

The proposed framework consists of:

### Backbone

* MobileNetV2 pretrained feature extractor

### Attention Modules

* Self-attention for global spatial dependency learning
* Channel attention for feature recalibration

### Classification Head

* Global Average Pooling
* Dense layer
* Softmax output

---

## Output Generated

After training, the following outputs are generated:

outputs/
├── saved_model/
├── accuracy_graph.png
├── loss_graph.png
├── confusion_matrix.png
├── classification_report.txt

---

## Performance Metrics

The following evaluation metrics are computed:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## Reproducing Manuscript Results

To reproduce manuscript experiments:

1. Place dataset in dataset/ folder
2. Run train.py
3. Run evaluation.py
4. Compare outputs with manuscript tables

All hyperparameters are identical to manuscript settings.

---

## File Description

train.py → training script
test.py → testing script
evaluation.py → metric calculation
model.py → architecture definition

---

## Saved Model

Trained model is stored at:

saved_model/model.h5

Load model:

from tensorflow.keras.models import load_model
model = load_model('saved_model/model.h5')

---

## Citation

If you use this code, please cite:

Author Name, "Lightweight Attention-Enhanced Convolutional Learning Framework for Multi-Class Plant Disease Classification Across Diverse Crops", submitted to Pattern Analysis and Applications.

---



For questions related to implementation or reproducibility, please contact the corresponding author through manuscript email.
