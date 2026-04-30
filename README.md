# 🦴 Bone Features Dataset

![License](https://img.shields.io/badge/license-MIT-green)

This repository provides datasets (in CSV format) accompanying the preprint:

> **“Leveraging topological data analysis to estimate bone strength from microCT images as a surrogate for advanced imaging.”**

The dataset includes multiple feature representations extracted from microCT images, along with ground-truth measurements of apparent bone strength.

---

## 📁 Repository Structure

The dataset is organized into the following feature groups:

- Morphometric features (Otsu-based methods)
- Topological features (Signed distance persistence images)
- Ground truth targets (apparent strength)

---

## 🧮 Morphometric Features

These features are derived using variations of local Otsu thresholding methods.

### 1. Local (1D) Otsu

- **Filename format:**  
  `otsu{window_size}.csv`

- **Description:**  
  Standard local Otsu thresholding applied with a specified window size.

---

### 2. Modified Local Otsu

- **Filename format:**  
  `otsu{window_size}-{contrast}.csv`

- **Description:**  
  Extension of local Otsu incorporating a contrast parameter to enhance segmentation sensitivity.

---

### 3. Local 2D Otsu

- **Filename format:**  
  `otsu2D{intensity_window}-{mean_window}.csv`

- **Description:**  
  Two-dimensional Otsu thresholding that considers both local intensity and local mean values.

---

## 🔷 Signed Distance Persistence Images (SDPI)

- **Filename format:**  
  `sdpi{dimension}-{x_resolution}-{y_resolution}-{x_spread}-{y_spread}.csv`

- **Parameters:**
  - `dimension`: Homology dimension (0, 1, or 2)
  - `x_resolution`, `y_resolution`: Image resolution
  - `x_spread`, `y_spread`: Gaussian spread parameters

- **Notes:**
  - Files are grouped based on whether **scaled** or **unscaled** persistence images are used.

---

## 🎯 Apparent Strength

- **Filename:**  
  `targets.csv`

- **Description:**  
  Contains the ground-truth apparent strength values corresponding to each sample in the dataset.

---

## ⚠️ Notes

- All files are in **CSV format** and can be loaded using standard data analysis tools.
- The persistence image files are not provided with a header, while all other files are.
