# Space Research 2

```python
# ===============================
# Project: Space Research 2
# Author: M. Nivetha
# Description: ML-based analysis and classification of celestial objects
# Dataset: SDSS Skyserver (Skyserver_SQL2)
# ===============================

# -------------------------------
# Overview
# -------------------------------
# This project automates the detection and classification of astronomical objects.
# It processes both tabular and image datasets from SDSS to classify galaxies, stars, and quasars.
# The project also visualizes predicted classes on galaxy images.

# -------------------------------
# Dataset Details
# -------------------------------
# Skyserver_SQL2 CSV Columns:
# objid      - unique object ID
# ra         - right ascension (celestial coordinate)
# dec        - declination (celestial coordinate)
# u,g,r,i,z  - photometric magnitudes in different filters
# run        - survey run number
# rerun      - rerun number for data reduction
# camcol     - camera column
# field      - field number
# specobjid  - spectroscopic object ID
# class      - object class (galaxy, star, quasar)
# redshift   - redshift of object
# plate      - spectroscopic plate number
# mjd        - modified Julian date
# fiberid    - fiber ID on the spectroscopic plate

# -------------------------------
# Algorithms & Techniques
# -------------------------------

# 1. Image Processing
# - Resize images to uniform dimensions
# - Convert to grayscale (optional, depending on model)
# - Normalize pixel values
# - Optional: augment data for more robust training

# 2. Machine Learning Models
# - Convolutional Neural Network (CNN) for galaxy image classification
#     - Layers: Conv2D, MaxPooling2D, Dense, Dropout
#     - Activation: ReLU for hidden layers, Softmax for output
#     - Loss: Categorical Crossentropy
# - Random Forest Classifier for tabular data
#     - Handles photometric features (u, g, r, i, z) for classification
# - Support Vector Machine (SVM) as an alternative tabular classifier
# - Train/test split: usually 80/20 or 70/30
# - Evaluation: accuracy, confusion matrix, classification report

# 3. Data Handling & Visualization
# - pandas: read/write CSV, manage tabular data
# - numpy: numerical operations
# - matplotlib / seaborn: plot distributions, correlations, predictions
# - SQL queries: fetch specific subsets from Skyserver

# -------------------------------
# Project Pipeline
# -------------------------------

# Step 1: Load CSV / FITS dataset
# Step 2: Preprocess data
#         - Images: resize, normalize, convert to arrays
#         - Tabular: handle missing values, normalize features
# Step 3: Feature extraction (optional for CNN)
# Step 4: Train ML models (CNN / Random Forest / SVM)
# Step 5: Evaluate model performance
# Step 6: Predict on test / new data
# Step 7: Visualize predictions on galaxy images with labels

# -------------------------------
# Installation
# -------------------------------

# Clone repository
# git clone https://github.com/M-Nivetha7/Space_Research_2.git
# cd Space_Research_2

# Install dependencies
# pip install -r requirements.txt

# Run project notebook
# jupyter notebook Space_Research_2.ipynb

# -------------------------------
# Usage
# -------------------------------
# - Load dataset
# - Preprocess images / tabular data
# - Train chosen ML model
# - Evaluate model
# - Visualize predictions
# - Modify parameters to experiment with models or preprocessing

# -------------------------------
# Results
# -------------------------------
# - Galaxy, star, and quasar classification
# - Accuracy metrics displayed in notebook
# - Interactive visualization of classified images

# -------------------------------
# Future Improvements
# -------------------------------
# - Use YOLO or Faster R-CNN for real-time object detection
# - Expand to detect meteors, supernovae, or other transient phenomena
# - Train on larger SDSS datasets for improved accuracy

# -------------------------------
# References
# -------------------------------
# - SDSS SkyServer: http://skyserver.sdss.org
# - Python libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow/keras
# - Research papers on galaxy classification using ML



