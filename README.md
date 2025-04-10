# ☕ Coffee Quality Clustering with PCA and t-SNE

This project applies **dimensionality reduction techniques (PCA + t-SNE)** and **unsupervised clustering** to uncover patterns in physical and sensory data from coffee samples. The results reveal two main groups with distinct characteristics, interpreted as **commercial-grade** and **high-quality** coffees.

## 📊 Techniques Used

- **Dimensionality Reduction:**
  - `PCA` for variance retention and pre-processing
  - `t-SNE` for 2D visualization with local structure preservation
- **Clustering:**
  - `KMeans` with optimal `k=2` based on elbow and silhouette analysis
- **Cluster Profiling:**
  - Z-score standardization
  - Interpretation based on quality-impacting features

## 🧩 Results

### Cluster 0 – Commercial Coffees

| Feature              | Interpretation                              | Quality Impact                        |
|----------------------|----------------------------------------------|----------------------------------------|
| **Altitude**         | Slightly above average (~1,300–1,500m)       | Medium-density beans                  |
| **Moisture**         | Above ideal (>12%)                           | Risk of moldy or musty flavors        |
| **Quakers**          | Significant presence (+0.33 Z)               | Unpleasant bitter notes               |
| **Aroma & Flavor**   | Weaker sensory notes                         | Lower flavor complexity               |
| **Visual Defects**   | 5–15 defects per 300g                        | Compromised visual appeal             |

**📌 Technical Profile:**  
Likely processed using dry/natural or quick-dry methods.  
**⚠️ Risks:** Sensory imbalance.  
**✅ Recommendations:**
- Improve drying to reach ~11% moisture
- Use manual or electronic sorting to reduce quakers

---

### Cluster 1 – High-Quality Coffees

| Feature              | Interpretation                              | Competitive Advantage                 |
|----------------------|----------------------------------------------|----------------------------------------|
| **Altitude**         | Below average (~900–1,200m)                  | Less dense beans                      |
| **Moisture**         | Well-controlled (~10–11%)                    | Preserves flavor characteristics      |
| **Quakers**          | Nearly absent (-0.30 Z)                      | Uniform cup profile                   |
| **Aroma & Flavor**   | Balanced, well-defined notes                 | Rich sensory profile                  |
| **Visual Defects**   | Max 3–5 defects per 300g                    | Excellent visual quality              |

**📌 Technical Profile:**  
Likely **washed (wet)** processing.  
**💪 Strengths:** High process control.  
**🌱 Opportunities:**
- Market positioning as **single origin**
- Light roasting to enhance acidity and aroma

---

## 🔍 Hidden Patterns Uncovered

1. **Altitude Paradox**:  
   Coffees from **lower altitudes** (Cluster 1) showed **better overall quality**, suggesting **post-harvest processing** can compensate for bean density.

2. **Moisture vs Defects**:  
   Higher moisture correlates with more defects → **drying control is critical**.

3. **Quakers as a Key Metric**:  
   Z-score gap of +0.63 between clusters → a strong indicator for **sensory segmentation**.

---

## 📌 Next Steps

- **Cluster 0**:
  - Experiment with lowering moisture to 10.5–11% and track defect rates.

- **Cluster 1**:
  - Trace the exact origin to study high-quality outliers at lower altitudes.

- **Additional Insights**:
  - Cross-reference with `Processing Method` to validate washed vs natural hypotheses.

---

## 📁 Project Structure

```bash
.
├── data/
│   └── coffee_quality_dataset.csv
├── notebooks/
│   └── clustering_analysis.ipynb
├── visuals/
│   └── cluster_profiles.png
├── README.md
└── requirements.txt
```

## 🧠 Conclusion  

This project demonstrates how data science techniques can reveal hidden patterns and drive actionable decisions in the coffee industry. Combining dimensionality reduction, clustering, and profile analysis provides practical insights—from post-harvest improvements to specialty coffee market strategies.
