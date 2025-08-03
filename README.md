# Urban_Street_Network_Clustering_with_Python

This project implements a computational method to classify street segments in an urban street network using topological properties. It is based on the research article:

> Chen, H.-H., Mumm, O., & Carlow, V. M. (2024).  
> *A computational approach for categorizing street segments in urban street networks based on topological properties*.  
> Frontiers in Built Environment. [DOI: 10.3389/fbuil.2023.1216888](https://www.frontiersin.org/articles/10.3389/fbuil.2023.1216888/full)

---

## 🧭 Overview

The project presents a **Network-based Street Categorization (NSC)** framework that clusters street segments by their **centrality measures** rather than predefined functional classes. This allows data-driven, topology-informed street categorization, which can support:

- Urban planning
- Infrastructure design
- Mobility system optimization
- Detection of functional mismatches in street classifications

---

## 🔍 Methodology Summary

The core steps in this workflow are:

1. **Download and build a street network** from OpenStreetMap for Braunschweig, Germany
2. **Compute centrality metrics** for each street segment:
   - Betweenness Centrality (Cb)
   - Closeness Centrality (Cc)
   - Degree Centrality (Cd)
   - PageRank Centrality (Cp)
3. **Standardize features** using Z-score normalization
4. **Cluster segments** using Hierarchical Agglomerative Clustering (HAC)
5. **Visualize** spatial distribution of NSC categories
6. **Compare with OSM’s Functional Classification Scheme (FCS)** using statistical tests (e.g. KS test)

---

## Requirements
This project uses Python 3.x and the following libraries:
- osmnx
- networkx
- geopandas
- pandas
- matplotlib
- scikit-learn
- pyclustertend
- scipy

---

## Install via:
pip install osmnx networkx geopandas pandas matplotlib scikit-learn pyclustertend scipy

---

## Running the Analysis
- Run the notebook from top to bottom.
- All core functions (data download, centrality calculation, clustering) are wrapped into logical steps.
- The clustering result (NSC category) is added to the GeoDataFrame and ready for export/visualization.
- Use QGIS or geopandas to visualize the output.

---

## Output Highlights
- NSC classification maps with 6 clusters
- Boxplots showing variation in centrality values by cluster
- Dendrogram from hierarchical clustering
- Silhouette score analysis
- Statistical comparison between NSC and FCS (KS test)

---

## Related Paper
If you use this code or workflow, please cite:
@article{chen2024street,
  title={A computational approach for categorizing street segments in urban street networks based on topological properties},
  author={Chen, Hsiao-Hui and Mumm, Olaf and Carlow, Vanessa Miriam},
  journal={Frontiers in Built Environment},
  volume={9},
  year={2024},
  doi={10.3389/fbuil.2023.1216888}
}

---

## Applications
- Reclassification of road segments for smarter transport planning
- Identifying segments mismatched with their expected functional role
- Site selection for street redesign, noise monitoring, or modal infrastructure (bike lanes, pedestrian routes)

---

## Author & Contact
This project is developed by Dr.-Ing. Hsiao-Hui Chen.

## License
This work is shared under the Creative Commons Attribution License (CC BY 4.0).
