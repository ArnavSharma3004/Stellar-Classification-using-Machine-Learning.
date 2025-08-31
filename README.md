# 🌌 Stellar Classification using Machine Learning  

### 📍 Project Overview  
This project focuses on **classifying celestial objects** — **Stars, Galaxies, and Quasars (QSOs)** — using **Machine Learning techniques**.  
The dataset is sourced from the **Sloan Digital Sky Survey (SDSS)**, which provides photometric and spectral measurements for astronomical objects.  

We apply **both supervised and unsupervised learning approaches**:  
- **Support Vector Machine (SVM, supervised):** to train a predictive classifier.  
- **KMeans Clustering (unsupervised):** to explore natural groupings in the data.  

---

### 🎯 Objectives
- Clean and preprocess the dataset (handle missing values like `-9999.0`, engineer **color indices** such as `u-g, g-r, r-i, i-z`).  
- Perform **Exploratory Data Analysis (EDA)** to understand distributions, correlations, and separability of classes.  
- Apply **SVM** for classification and evaluate accuracy.  
- Apply **KMeans Clustering** to identify natural patterns without labels.  
- Compare both approaches and interpret results.  

---

### 📊 Dataset
- **Source:** Sloan Digital Sky Survey (SDSS).  
- **Size:** ~100,000 rows × 18 columns.  
- **Features:**  
  - Spectral magnitudes: `u, g, r, i, z`  
  - Engineered color indices: `u_g, g_r, r_i, i_z`  
  - Positional coordinates: `alpha, delta`  
  - Time of observation: `mjd`  
- **Target Variable:** `class` → `GALAXY`, `STAR`, `QSO`.  

---

### 🔍 Exploratory Data Analysis (EDA)
We conducted:  
- **Histograms:** Distribution of each spectral band.  
- **Pairplots:** Feature relationships, separability by class.  
- **Correlation Heatmap:** Identify highly correlated features.  
- **Boxplots:** Detect outliers and class-specific patterns.  
- **KDE plots:** Visualize class-wise density of features.  

---

### 🤖 Machine Learning Models

#### 1. **Supervised: Support Vector Machine (SVM)**
- Train-test split: 70:30.  
- Kernel: **RBF (Radial Basis Function)**.  
- Achieved **~85% accuracy**.  
- Confusion matrix shows strong performance on **Galaxy classification**, with some overlap between **Stars** and **QSOs**.  

#### 2. **Unsupervised: KMeans Clustering**
- Applied with **k=3** clusters.  
- Evaluated with **Silhouette Score (0.62)**.  
- Clustering revealed natural groupings that align reasonably with true classes.  

---

### 📈 Results
- **SVM Classifier:** ~85% accuracy, robust generalization.  
- **KMeans Clustering:** Useful for exploring patterns, but less precise than supervised classification.  
- **Key Insight:** **Color indices** (`u-g, g-r, r-i, i-z`) are strong discriminators for stellar classification.  

---

### 🚀 Future Scope
- Explore **deep learning models** (e.g., CNNs on spectral data).  
- Apply **ensemble methods** for better accuracy.  
- Handle **imbalanced classes** for fair predictions.  
- Use physics-informed features for domain-specific improvements.  

---

### 📂 Project Structure
