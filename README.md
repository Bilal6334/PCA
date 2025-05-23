# 🧠 PCA from Scratch on Fashion-MNIST

This project demonstrates how to implement **Principal Component Analysis (PCA) from scratch** (using only NumPy) and apply it to the [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) image dataset for dimensionality reduction and visualization.

## 📌 Project Highlights

- ✅ PCA implemented **from scratch** without `scikit-learn`
- ✅ Applied on image data: **Fashion-MNIST (28x28 grayscale)**
- ✅ Visualized clusters using 2D PCA
- ✅ Measured **reconstruction error** (MSE) to evaluate information loss
- ✅ Compared performance for different numbers of components (`k`)
- ✅ Plotted **explained variance** for insight into compression quality

---

## 📊 Dataset

- 60,000 training images of clothing items (10 categories)
- 28 × 28 grayscale (flattened to 784 features)
- Loaded via `tensorflow.keras.datasets.fashion_mnist`

---

## 📈 PCA Workflow

1. **Data Normalization**  
   Standardized pixel values using mean and standard deviation

2. **Covariance Matrix**  
   Computed 784 × 784 covariance matrix of standardized data

3. **Eigen Decomposition**  
   Computed eigenvalues and eigenvectors manually using `np.linalg.eigh`

4. **Dimensionality Reduction**  
   Projected original data onto top `k` eigenvectors

5. **Data Reconstruction**  
   Reconstructed original data from reduced dimensions to calculate MSE

6. **Evaluation**  
   - Visualized 2D projections  
   - Calculated reconstruction loss (MSE)  
   - Plotted cumulative variance explained

---

## 🔍 Results

### 🎨 2D PCA Visualization

![PCA Scatter Plot](#)

### 📉 Reconstruction Loss vs Components

| Components (k) | Reconstruction MSE |
|----------------|---------------------|
| 2              | 0.0467              |
| 10             | 0.0258              |
| 50             | 0.0143              |
| 100            | 0.0099              |
| 200            | 0.0057              |

- ✅ 50 components retain significant information (MSE = 0.0143)
- ✅ 200 components reduce loss to just 0.0057

---

## 📁 Files

- `pca_from_scratch.ipynb`: Main notebook with full implementation
- `README.md`: Project overview and explanation

---

## 🚀 How to Run

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload and run `pca_from_scratch.ipynb`
3. Follow cells step-by-step (no external libraries like `scikit-learn` used)

---

## 🧠 What You’ll Learn

- PCA theory and math (eigen decomposition, projection)
- How to code PCA manually
- How to analyze reconstruction loss and variance
- Data visualization for high-dimensional compression

---

## 📬 Contact

Feel free to reach out for collaboration or questions!

---

