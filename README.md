# Hybrid Customer Segmentation System

Customer segmentation analysis using hybrid clustering algorithms (K-Means++, Affinity Propagation, and DBSCAN).

## Project Overview

This project provides two different customer segmentation approaches for textile/e-commerce data analysis with automatic outlier detection and performance evaluation.

## Code Files

### 01_5cluster_segmentation.py
Fixed 5-cluster segmentation with K-Means++ and DBSCAN noise detection.
- **Output**: Excel report + Heatmap visualization (PNG)
- **Use Case**: When exactly 5 customer segments are required

### 02_hybrid_model.py
Dynamic cluster discovery using Affinity Propagation for automatic K determination.
- **Output**: Excel report with hybrid segment assignments
- **Use Case**: When discovering natural cluster structure from data

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
# Fixed 5-cluster segmentation
python 5cluster_segmentation

# Dynamic hybrid model
python hybrid_model
```

Both scripts will open a file dialog to select your data file (Excel/CSV) and generate results in the same directory.

## Data Features

- University code (`uni_kodu`)
- Department code (`bolum_kodu`)
- Transaction amount (`totalamount`)
- Discount applied (`discount`)
- Customer city (`usercity`)
- Customer class (`sinif`)
- SMS interaction count (`sms_tekrar_sayisi`)
- Discount code usage (`indirim_kodu`)

## Technologies Used

- Python 3.7+
- Pandas, NumPy
- Scikit-learn (KMeans, DBSCAN, AffinityPropagation)
- Matplotlib, Seaborn
- OpenPyXL

## Performance Metrics

- **Silhouette Score**: Cluster quality (-1 to +1, higher is better)
- **Davies-Bouldin Index**: Cluster separation (lower is better)

## References

- Arthur, D., & Vassilvitskii, S. (2007). k-means++
- Frey, B. J., & Dueck, D. (2007). Affinity Propagation
- Ester, M., et al. (1996). DBSCAN
