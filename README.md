# Clustering Goalkeepers Using PCA and Data Analysis

## Overview
Goalkeepers play a crucial role in football, and their performances often determine match outcomes. This project uses data analysis, Principal Component Analysis (PCA), and clustering techniques to analyze and categorize goalkeepers based on their attributes and playing styles. The goal is to provide actionable insights for recruitment, training, and match preparation.

## Key Features
- **PCA for Dimensionality Reduction**: Simplifies complex data into principal components while retaining key variability.
- **K-Means and Hierarchical Clustering**: Groups goalkeepers into distinct profiles based on their attributes.
- **Sub-Clustering**: Further refines large clusters to uncover nuanced playing styles.
- **Similarity Analysis**: Identifies the most similar goalkeepers to target players.

---

## Data Used
This project utilizes data sourced from [FBRef](https://fbref.com), including:
- **Standard Goalkeeping Metrics**: Goals Against (GA90), Saves (Save%), Clean Sheet Percentage (CS%).
- **Advanced Goalkeeping Metrics**: Post-Shot Expected Goals (PSxG), Goals Saved Above Expected (PSxG +/-), Sweeper Keeper Actions.
- **Possession Metrics**: Touches, progressive passes, and carries.
- **Passing Metrics**: Pass completion percentages and progressive passing distance.

---

## Methods
### 1. Data Preprocessing
- Data was standardized using `StandardScaler` to ensure all features contributed equally to the analysis.

### 2. Principal Component Analysis (PCA)
- PCA was applied to reduce dimensionality and identify key components driving variability.
- Explained variance ratio was analyzed to retain the most informative components.

### 3. Clustering
- **K-Means Clustering**: Grouped goalkeepers into four distinct clusters based on PCA-transformed data.
- **Hierarchical Clustering**: Applied to the largest cluster to identify sub-clusters for greater granularity.

### 4. Similarity Analysis
- Identified the five most similar players to a given set of target goalkeepers using Euclidean distances in PCA space.

---

## Results
### Clustering Insights
- **Cluster 1**: Goalkeepers excelling in distribution and shot-stopping (e.g., Alisson, Courtois).
- **Cluster 2**: Reliable performers and emerging talents (e.g., De Gea, Mamardashvili).
- **Cluster 3**: Consistent performers (e.g., Neuer, Maignan, Ramsdale).
- **Cluster 4**: Sweeper-keepers (e.g., Martínez, Pope, Leno).

### Sub-Clustering for Largest Cluster
The largest cluster was further divided into four sub-clusters:
1. Alisson, Donnarumma, Forster, etc.
2. Arrizabalaga, Carnesecchi, etc.
3. Audero, Gollini, etc.
4. Courtois, Ederson, etc.

### Similarity Analysis
- **Manuel Neuer**: Iñaki Peña, Yann Sommer, Mike Maignan, Ederson, Gregor Kobel.
- **Thibaut Courtois**: Gerónimo Rulli, Paulo Gazzaniga, Bart Verbruggen, Bernd Leno, Rui Silva.
- **Gianluigi Donnarumma**: Alisson, Péter Gulácsi, Philipp Köhn, Alex Meret, Michele Di Gregorio.

---

## Visualizations
- **PCA Biplots**: Visualize the relationship between components and variables.
- **Dendrograms**: Show hierarchical relationships between clusters and sub-clusters.

---

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/goalkeeper-clustering.git
