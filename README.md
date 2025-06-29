# Sound Clustering Project

# capstone idea
[link to document](https://docs.google.com/document/d/1_DTJGhGrq1_dWkwI4sEaZtTH0HgXbFEl5fiGv7QOTYk/edit?usp=sharing)


Unsupervised clustering of 3000 unlabeled audio files using machine learning techniques.

## Overview
This project analyzes audio data to discover natural sound groupings without manual labeling. Uses MFCC features, dimensionality reduction, and clustering algorithms to identify 4 distinct sound categories.

## Dataset
- **3000 WAV files** in `unlabelled_sounds/` directory
- Audio features: 13 MFCCs + spectral centroid + zero-crossing rate
- Standardized 15-dimensional feature space

## Methods
- **Feature Extraction**: librosa for audio processing
- **Dimensionality Reduction**: PCA and t-SNE
- **Clustering**: K-Means vs DBSCAN comparison
- **Evaluation**: Silhouette score, Davies-Bouldin index

## Key Results
- **Optimal clusters**: 4 (determined by elbow method)
- **Best algorithm**: K-Means (good silhouette >0.3, DB index <1.5)
- **DBSCAN**: Poor performance in standardized feature space

## Usage
```bash
pip install librosa scikit-learn matplotlib seaborn pandas numpy
jupyter notebook template_clustering_assignment.ipynb
```

## Files
- `template_clustering_assignment.ipynb` - Main analysis notebook
- `unlabelled_sounds/` - Audio dataset (3000 WAV files)
- `README.md` - This file

## Applications
Automatic sound categorization for audio content analysis, smart home systems, or hearing aid environments.