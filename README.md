# ProcDNA-Assignment
Customer Segmentation with K-Means A data science project to segment casino customers using K-Means clustering. Includes feature selection, outlier detection, cluster visualization (2D), and data quality assessment. Final insights are summarized in a PowerPoint for business presentation.

# 🎯 Customer Segmentation using K-Means Clustering

This project presents an end-to-end clustering pipeline for customer segmentation using the K-Means algorithm. The goal is to analyze and group casino customers based on various behavioral and business attributes.

---

## 📌 Objectives

1. **Develop a clustering model** to segment customers into meaningful groups.
2. **Visualize and interpret clusters** with statistical summaries and 2D projections.
3. **Explain feature selection** logic using statistical rationale.
4. **Detect and handle outliers** in the data.
5. **Assess data quality issues** and propose validation checks.
6. **Deliver business insights** via Excel/PPT-ready summaries.

---

## 🧠 Algorithms & Tools Used

- **Clustering Algorithm**: K-Means (scikit-learn)
- **Dimensionality Reduction**: PCA (Principal Component Analysis)
- **EDA & Visualization**: pandas, matplotlib, seaborn
- **Outlier Detection**: IQR & Z-score methods
- **Data Quality**: Missing value & consistency checks
- **Reporting**: PPT summary with statistical highlights

---
![Screenshot 2025-05-14 121529](https://github.com/user-attachments/assets/6e954ead-f081-410d-961e-3fb6996935dd)

![Screenshot 2025-05-14 121517](https://github.com/user-attachments/assets/d5268457-1b7e-4efc-bb94-247f9e122622)

## 🔍 Key Features Used for Clustering

- `Seasonality_Segment`
- `EA_Segment`
- `Revenue_Bucket`
- `Profit_Bucket`
- `Market_Share_Segment`
- `Casino_Size_Segment`
- `Market_Potential_Segment`
- `Churn_Segment`
- `Competitiveness_Flag`
- `Volume_Segment`
- `Density_Segment`
- `Propensity`

After careful evaluation, non-informative and redundant features were dropped to reduce noise.

---

## 📊 Cluster Summary & Naming

Based on statistical profiling of each cluster, business-relevant names were assigned:

| Cluster ID | Cluster Name             | Key Traits                                                  |
|------------|--------------------------|-------------------------------------------------------------|
| 0          | High-Value Loyalists     | High revenue, high profit, low churn                        |
| 1          | At-Risk Low Spenders     | Low volume, high churn, minimal engagement                  |
| 2          | Emerging Potentials      | Moderate volume and potential with growth opportunity       |
| 3          | Low Engagement Accounts  | Inactive or inconsistent accounts with low profitability    |

---

## 📈 Cluster Evaluation

Two methods were used to determine the optimal number of clusters:

- **Elbow Method**: Assesses inertia (distortion) across different `k`.
- **Silhouette Score**: Measures the separation distance between clusters.

📌 **Chosen number of clusters: 4**

---

## 📉 Outlier Detection Logic

Implemented two statistical methods:
- **Z-Score**: Threshold-based detection using standard deviation.
- **IQR**: Identifies outliers outside 1.5× IQR range.

Outliers were either removed or capped depending on their impact.

---

## 🧪 Data Quality Checks

### Detected Issues:
- Inconsistent labels (e.g., `'None'`, `'-'`, and `NaN`)
- Mixed data types in categorical fields
- Missing values in key segmentation fields

### Quality Checks Implemented:
- Missing value percentage per feature
- Categorical consistency checks
- Unique value count
- Data type validation
- Duplicate row detection

---

## 📂 Project Structure

1. **clustering_pipeline.ipynb # Jupyter notebook with code and results**
2. **data/**
   2a. ***Clustering_Data.ftr # Input dataset***
3. **output/**
   3a. ***cluster_summary.xlsx # Account-cluster mapping***
   3b. ***cluster_plot.png # 2D PCA visualization***
4. **presentation/**
   4a. ***Customer_Clustering.pptx # Final presentation with insights***
5. **README.md # Project documentation**

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/Raj87Sudhanshu/ProcDNA-Assignment.git
   cd ProcDNA-Assignment

## Install dependencies:
pip install -r requirements.txt

## Run the notebook or Python scripts:
jupyter notebook clustering_pipeline.ipynb
