
# 🇫🇷 Correspondence Analysis of the 2012 French Presidential Election Results

This repository contains Python code that performs **Correspondence Analysis (Analyse des Correspondances - CA)** on the results of the 2012 French presidential election. The goal is to visualize the relationships between French regions and presidential candidates using multivariate statistical techniques.

---

## 📊 Project Description

Correspondence Analysis (CA) is a dimensionality reduction technique used for categorical data, especially in contingency tables. It reveals associations between rows (here: regions) and columns (here: candidates) through low-dimensional visualizations.

This project performs:

- 📥 Data loading and preprocessing  
- 📈 Calculation of frequencies and marginal profiles  
- 🧮 Centering and normalization of data  
- 🔍 Singular Value Decomposition (SVD)  
- 🗂️ Computation of principal coordinates, eigenvalues, contributions, and quality of representation  
- 🖼️ Multiple 2D visualizations (e.g., F1 vs F2, F1 vs F3, etc.)

---

## 📁 Dataset

**File:** `resultats_presidentielles_2012.csv`

Expected structure:
- First column: `Region` (e.g., "Île-de-France", "Provence-Alpes-Côte d'Azur", etc.)
- Subsequent columns: vote counts for each **candidate** (e.g., Hollande, Sarkozy, etc.)

Each row represents a region's vote distribution among all candidates.

---

## 🛠️ Libraries Used

- `pandas` for data handling  
- `numpy` for numerical operations  
- `scipy.linalg` for Singular Value Decomposition (SVD)  
- `matplotlib` for plotting

---

## 🧮 How It Works

1. **Load data** and extract candidate vote counts  
2. **Normalize** to calculate relative frequencies  
3. **Compute row/column profiles** and marginal frequencies  
4. **Center and normalize** the data to get the matrix of standardized residuals  
5. **Apply SVD** to obtain singular values and derive coordinates  
6. **Plot projections** of regions and candidates on principal components  
7. **Calculate contributions** and **qualities of representation** (cos²) for deeper interpretation

---

## 📌 Outputs

- ✅ **Eigenvalues** and **explained inertia** (% variance)  
- ✅ **Coordinates of regions and candidates** on the first four principal axes  
- ✅ **Contribution and representation quality** of each row and column  
- ✅ **Plots** of projections in 2D space for easier interpretation

---

## 📸 Example Visualizations

- 🗺️ Projection of regions on F1 and F2  
- 🗺️ Projection of candidates on F1 and F2  
- 🗺️ Additional projections: F1 vs F3, F1 vs F4, F2 vs F3

These reveal associations like which candidates were more favored in specific regions.

---

## 📂 File Structure



├── resultats_presidentielles_2012.csv 
├── AFC.py          # Main script
├── README.md                           



---

## ▶️ Run Instructions

1. Place the CSV dataset file in the same folder as the script  
2. Make sure all dependencies are installed:

```bash
pip install pandas numpy matplotlib scipy
````

3. Run the script:

```bash
python AFC.py
```

---

## 🧠 Interpretation Tip

* Points close to each other on the plots are **similar** in profile
* If a region and a candidate are close on the plot, the candidate performed strongly in that region

---



