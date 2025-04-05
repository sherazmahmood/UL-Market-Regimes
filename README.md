# Unsupervised Learning for Market Regimes  
**By Sheraz Mahmood — CU Boulder, Unsupervised Learning Course**

## 📌 Overview

This project applies unsupervised and supervised machine learning techniques to **discover, analyze, and predict financial market regimes** using:

- The **VIX Volatility Index**
- **News Sentiment Index** from the Federal Reserve Bank of San Francisco
- The **US Unemployment Rate** from FRED

Goal: Can we uncover latent market structures — like calm, volatile, or crisis regimes — without labels, and predict them from observable indicators?*

## Methodology

### 1. **Data Collection & Feature Engineering**
- **VIX**: Daily data from Yahoo Finance
- **Sentiment**: Daily sentiment scores from the Federal Reserve
- **Unemployment**: Monthly macroeconomic data (forward-filled)
- Engineered features:
  - `Log_Close_Change` (VIX log returns)
  - `Log_Sentiment_Change`
  - `VIX_Range` (High - Low)

### 2. **Exploratory Data Analysis (EDA)**
- Boxplots, histograms, and correlation analysis
- Identified multicollinearity and transformed data
- Normalized and cleaned for modeling

### 3. **Dimensionality Reduction with PCA**
- Reduced to 2 principal components
- Explained variance assessed
- Used for clustering, visualization, and recommendation

### 4. **Clustering with KMeans**
- Identified 4 latent **market regimes**
- Labeled historical periods using unsupervised learning
- Validated regime alignment with known financial crises (e.g., 2008, COVID-19)

### 5. **Nearest Neighbors Recommender**
- Found similar historical market conditions to a given day
- Interactive comparison of “market feel” using PCA proximity

### 6. **Supervised Regime Prediction with SVM**
- Trained an **SVM classifier** on the unsupervised regime labels
- Achieved **97% accuracy** on test and validation sets
- Confirmed that the latent regimes are **predictable and explainable**

## Results

- Discovered **distinct market regimes** from unlabeled data
- Achieved **strong predictive performance** using Support Vector Machines
- Built a working recommender for **market similarity search**
- Visualized **regime transitions over time**, aligned with real-world events
