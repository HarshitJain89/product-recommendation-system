# 🛍️ Product Recommendation System

## Overview
A recommendation engine built using popularity-based filtering and collaborative filtering (SVD), evaluated on a large product ratings dataset. The collaborative filtering model achieves an **RMSE of 0.98**, indicating strong predictive accuracy for personalised recommendations.

## Problem Statement
E-commerce platforms need to recommend the right products to the right users. This project compares a simple popularity-based approach against a personalised machine learning model.

## Dataset
- Large product ratings dataset
- Filtered to users with 50+ ratings for density
- 48,190 unique product IDs
- Rating scale: 1-5 (mean ~4.26)

## Models Built

### 1. Popularity-Based Recommendation
A non-personalised baseline using a weighted rating formula:

```
weighted_rating = (avg_rating x rating_count + mean_rating x cutoff) / (rating_count + cutoff)
```

- Cutoff set at 95th percentile of rating counts
- Returns top-N products for all users
- Limitation: Not personalised

### 2. Collaborative Filtering (SVD)

| Metric | Value |
|--------|-------|
| Train/Test Split | 70% / 30% |
| Algorithm | SVD (Matrix Factorisation) |
| **RMSE** | **0.98** |

## Key Concepts
- **Weighted Rating**: Balances average rating with number of ratings to avoid bias
- **SVD**: Decomposes the user-product interaction matrix into latent factors capturing hidden patterns
- **RMSE**: Measures difference between predicted and actual ratings - lower is better

## Tech Stack
```
Python | Surprise | NumPy | Pandas | Matplotlib | Seaborn
```

## How to Run
1. Clone the repo
2. Install dependencies: `pip install scikit-surprise numpy pandas matplotlib seaborn`
3. Open in Jupyter or Google Colab and run all cells

---
*Completed as part of the Post-Graduate Program in AI & Machine Learning - University of Texas at Austin (2021)*
