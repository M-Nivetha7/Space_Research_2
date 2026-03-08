# 🚀 Space Research 2

## 🌌 Overview
Space Research 2 is a machine learning-based project for detecting and classifying celestial objects.  
It processes tabular and image datasets from SDSS to classify galaxies, stars, and quasars, and provides interactive visualizations for easier analysis.

---

## 🗂 Dataset Details
The project uses the **Skyserver_SQL2 dataset** with the following columns:

- `objid`      : Unique object ID  
- `ra`, `dec`  : Celestial coordinates (Right Ascension, Declination)  
- `u, g, r, i, z` : Photometric magnitudes in different filters  
- `run`, `rerun` : Survey and reduction run numbers  
- `camcol`     : Camera column  
- `field`      : Field number  
- `specobjid`  : Spectroscopic object ID  
- `class`      : Object class (Galaxy, Star, Quasar)  
- `redshift`   : Redshift of the object  
- `plate, mjd, fiberid` : Spectroscopic details  

---

## 🧠 Algorithms & Techniques Used

### 1️⃣ Image Processing
- Resize images to uniform dimensions  
- Convert to grayscale (optional for CNN)  
- Normalize pixel values  
- Data augmentation for robust model training  

### 2️⃣ Machine Learning Models
- **Convolutional Neural Network (CNN)**: Classifies galaxy images  
  - Layers: Conv2D, MaxPooling2D, Dense, Dropout  
  - Activation: ReLU (hidden), Softmax (output)  
  - Loss function: Categorical Crossentropy  
- **Random Forest Classifier**: Classifies tabular data (photometric features)  
- **Support Vector Machine (SVM)**: Alternative classifier for tabular data  
- Train/test split: 80/20  
- Evaluation: Accuracy, Confusion Matrix, Classification Report  

### 3️⃣ Data Handling & Visualization
- `pandas` for CSV data manipulation  
- `numpy` for numerical computations  
- `matplotlib` and `seaborn` for visualization  
- SQL queries to fetch specific subsets from Skyserver  

---

## 🔄 Project Pipeline
1. Load CSV or FITS dataset  
2. Preprocess images and tabular data  
3. Feature extraction (for CNN)  
4. Train ML models (CNN / Random Forest / SVM)  
5. Evaluate model performance  
6. Predict new or test data  
7. Visualize predictions with labeled images  

---

## ⚙ Installation

```bash
# Clone the repository
git clone https://github.com/M-Nivetha7/Space_Research_2.git
cd Space_Research_2

# Install required dependencies
pip install -r requirements.txt

# Run Jupyter notebook
jupyter notebook Space_Research_2.ipynb
