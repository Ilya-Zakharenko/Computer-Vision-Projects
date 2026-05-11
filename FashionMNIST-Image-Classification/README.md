![E-commerce Cross-Sell Recommendation](figures/project-header.jpg)

# <center> **PROJECT: E-commerce Cross-Sell Recommendation System**

End-to-end recommender system designed to increase **add-on sales (cross-sell)** in an online store.

---

### **Project Goal**

Build an effective recommendation system for suggesting additional products (cross-sell) to users in order to increase average order value.

---

### **Models Implemented**

- Popularity-based
- Content-Based Filtering
- Item-Based Collaborative Filtering
- Matrix Factorization (SVD)
- Neural MF

---

### **Evaluation Results**

| Model                  | Precision@5 | Recall@5  | nDCG@5   | MAP@5    |
|------------------------|-------------|-----------|----------|----------|
| Popularity             | 0.003000    | 0.005640  | 0.006974 | 0.001671 |
| Content-Based          | 0.000000    | 0.000000  | 0.000000 | 0.000000 |
| **Item-Based CF**      | **0.061538**| **0.077514** | **0.174900** | **0.051400** |
| Matrix Factorization   | 0.009877    | 0.007795  | 0.034097 | 0.003640 |
| Neural MF              | 0.000000    | 0.000000  | 0.000000 | 0.000000 |

---

### **Conclusion**

Among all tested models, **Item-Based Collaborative Filtering** demonstrated the best performance across all key ranking metrics:

- Highest `Precision@5`
- Highest `Recall@5`
- Significantly better `nDCG@5`
- Best `MAP@5`

This indicates that in this dataset, **behavioral similarity between items** is the strongest signal for recommendations. Users tend to interact with logically related products, and item-item collaborative filtering captures this pattern most effectively.

More complex models, including the neural approach, did not provide improvement due to the high sparsity of the data. In this particular case, a relatively simple classical collaborative model proved to be the most effective solution.

---

### **Project Stages**
1. Basic data analysis
2. Data preprocessing and cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Engineering (Item & User-Item features)
5. Machine Learning
6. Model evaluation and comparison
7. Conclusions

---

### **Technologies Used**
- `pandas`, `numpy`, `scikit-learn`, `scipy`
- `PyTorch`
- `matplotlib`, `seaborn`, `plotly`

---

### **Project Structure**
- `notebooks/` — main analysis
- `src/` — model implementations
- `data/` — datasets
- `figures/` — visualizations
- `requirements.txt`

---

### **How to run**
```bash
cd E-commerce-Cross-Sell-Recommendation
pip install -r requirements.txt
jupyter notebook "PROJECT - E-commerce Cross-Sell Recommendation System.ipynb"