# 🌾 Crop Recommendation Analysis

An exploratory data analysis (EDA) project that studies how soil nutrients and climate conditions relate to the crops best suited to grow in them. The analysis covers data inspection, cleaning, outlier treatment, and visualization across **22 crop types**.

## 📌 Overview

Choosing the right crop for a given piece of land depends on soil composition and local weather. This project explores a crop recommendation dataset to uncover patterns such as:

- Which crops need higher nitrogen, phosphorus, or potassium
- How temperature and humidity separate different crops
- How soil pH varies across crop types

The notebook is a solid foundation for building a machine learning crop-recommendation model on top of it.

## 📂 Repository Structure

```
├── Crop_Recommendation_Analysis.ipynb   # Main analysis notebook
├── Crop_recommendation.csv              # Dataset
└── README.md
```

## 📊 Dataset

- **Rows:** 2,200
- **Columns:** 8 (7 features + 1 target label)
- **Crops (22):** rice, maize, chickpea, kidneybeans, pigeonpeas, mothbeans, mungbean, blackgram, lentil, pomegranate, banana, mango, grapes, watermelon, muskmelon, apple, orange, papaya, coconut, cotton, jute, coffee

| Feature | Description |
|---------|-------------|
| `N` | Nitrogen content in soil |
| `P` | Phosphorus content in soil |
| `K` | Potassium content in soil |
| `temperature` | Temperature in °C |
| `humidity` | Relative humidity in % |
| `ph` | Soil pH value |
| `rainfall` | Rainfall in mm |
| `label` | Recommended crop (target) |

## 🔍 What the Notebook Covers

1. **Data loading**: reading the CSV with pandas and previewing with `head()` / `tail()`
2. **Data overview**: shape, summary statistics (`describe()`), `info()`, and data types
3. **Data cleaning**: checking for missing values
4. **Exploratory data analysis**
   - Histograms of all numerical features
   - Box plots for `temperature`, `humidity`, `ph`, `N`, `P`, and `K`
5. **Outlier handling**: IQR method (Q1 − 1.5×IQR, Q3 + 1.5×IQR) used to cap outliers in `P`, `humidity`, `ph`, and `K`
6. **Relationship analysis**
   - Scatter plot of humidity vs. temperature, colored by crop
   - Violin plot of soil pH by crop type
   - Bar plot of potassium (K) levels by crop
   - Average phosphorus (P) by crop, ranked

## 🛠️ Tech Stack

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Shiva2202/<repository-name>.git
cd <repository-name>
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Run the notebook

```bash
jupyter notebook Crop_Recommendation_Analysis.ipynb
```

> **Note:** The notebook loads the data from `/content/Crop_recommendation.csv` (the Google Colab path). If you run it locally, change `file_path` to `'Crop_recommendation.csv'`.

## 🔮 Future Work

- Correlation heatmap between features
- Train and compare classification models (Random Forest, Decision Tree, SVM, KNN, etc.)
- Evaluate with accuracy, precision, recall, and a confusion matrix
- Build a simple web app (Streamlit / Flask) that recommends a crop from user input

## 👤 Author

**Borath Shiva Kumar**
GitHub: [@Shiva2202](https://github.com/Shiva2202)

## 📄 License

This project is open source and available for educational use.

---

⭐ If you found this project useful, consider giving it a star!
