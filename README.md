# 🌸 Clustering Assignment – UCI Iris Dataset

This project performs a comparative analysis of clustering algorithms on the **Iris dataset** from the UCI Machine Learning Repository. It evaluates the impact of different preprocessing techniques and cluster counts on clustering quality using various evaluation metrics.

---

## 📊 Dataset

- **Source**: [Iris Data – UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/iris)
- **Features Used**: 4 numerical features (sepal and petal length and width)
- **Samples**: 150 (3 classes of 50 instances each)

---

## 🧪 Clustering Algorithms Used

- **KMeans**
- **Hierarchical Clustering (Agglomerative)**
- **Mean Shift Clustering**

---

## ⚙️ Preprocessing Techniques

- Raw (No Processing)
- Normalization (Min-Max Scaling)
- Log Transformation
- PCA (Dimensionality Reduction)
- T+N (Log Transform + Normalization)
- T+N+PCA

---

## 📈 Evaluation Metrics

- **Silhouette Score** (Higher = Better)
- **Calinski-Harabasz Index** (Higher = Better)
- **Davies-Bouldin Index** (Lower = Better)

---


---

## ✅ Results Summary

| Algorithm           | Best Preprocessing | Best k  | Silhouette | CH Score | DB Score |
|---------------------|--------------------|--------|------------|----------|----------|
| **KMeans**          | **Log Transform**  | 3      | **0.619**  | **1279.73** | **0.53**  |
| **Hierarchical**    | Log Transform      | 3      | 0.616      | 1259.35  | 0.54     |
| **Mean Shift**      | Log Transform      | auto (2 clusters) | 0.789  | 1095.36  | **0.27**  |

---

## 📌 Conclusion

- The **best overall clustering performance** was achieved using **KMeans with Log Transformation and k=3**, yielding the highest Silhouette score and Calinski-Harabasz index, along with a low Davies-Bouldin score.
- **Hierarchical Clustering** also performed well under the Log Transformed data with similar metrics, though it slightly underperformed compared to KMeans.
- **Mean Shift**, although not relying on a pre-defined number of clusters, performed best when it auto-detected **2 clusters** after log transformation, achieving the **highest Silhouette score** (0.789) and **lowest DB index** (0.268). However, this may indicate under-segmentation compared to the true number of Iris species (3).
- **Log Transformation** consistently enhanced cluster separation across all algorithms, making it the most effective preprocessing step in this analysis.

---

