# Clustering Goalkeepers Using PCA and Data Analysis

## Purpose of the Analysis
Goalkeepers play a pivotal role in football, and their unique skill sets often define match outcomes. However, analyzing and categorizing goalkeepers' performances remains a complex task due to the diverse nature of their responsibilities. The purpose of this analysis is to understand goalkeeper performance, identify patterns, and group players with similar traits or playing styles through clustering techniques.

### Possible Applications
- **Scouting and Recruitment**: Identify goalkeepers that fit specific team needs, such as those excelling in distribution or shot-stopping.
- **Training and Development**: Customize training programs based on identified clusters to enhance specific skills.
- **Match Preparation**: Study opponent goalkeepers to strategize attacks.
- **Fan Engagement**: Provide a deeper understanding of goalkeeping styles and attributes.

---

## Data Used
The analysis utilizes comprehensive data sourced from [FBRef](https://fbref.com), encompassing:

### Standard Goalkeeping Metrics
- **Goals Against (GA90)**
- **Saves (Save%)**
- **Clean Sheet Percentage (CS%)**

### Advanced Goalkeeping Metrics
- **Post-Shot Expected Goals (PSxG)**
- **Goals Saved Above Expected (PSxG +/-)**
- **Sweeper Keeper Actions** (e.g., Avg Distance of Defensive Actions)

### Possession Metrics
- **Touches** in defensive, middle, and attacking thirds.
- **Progressive passes and carries.**

### Passing Metrics
- Completion percentages for **short, medium, and long passes.**
- **Progressive passing distance.**

---

## PCA and Clustering

### Principal Component Analysis (PCA)
PCA reduces the complexity of data by transforming it into a smaller set of dimensions called principal components. These components retain the majority of the data's variability, enabling meaningful analysis.

### Clustering Techniques
This analysis employed:
- **K-Means Clustering**: Groups players by minimizing intra-cluster variance.
- **Hierarchical Clustering**: Provides a tree-like structure to explore subgroups within clusters.

---

## Analysis Workflow

### Standardization
Standardized the data using `StandardScaler` to ensure all features contributed equally.

### PCA and Clustering
```python
from sklearn.decomposition import PCA
from sklearn.cluster import KMeans

# Standardization
scaler = preprocessing.StandardScaler().fit(X_teams)
X_teams_scaled = scaler.transform(X_teams)

# PCA
pca = decomposition.PCA()
pca_values_teams = pca.fit_transform(X_teams_scaled)
