# SVM Optimization Experiment

## Overview
This repository contains an implementation of a Support Vector Machine (SVM) optimization experiment for multi-class classification. The experiment uses a synthetic dataset to evaluate SVM performance across multiple samples with different parameters.

## Features
- Generation of synthetic multi-class dataset with 5000 samples and 10 features
- Automated SVM hyperparameter optimization
- Multiple sample evaluation (15 different train/test splits)
- Comprehensive visualization of results
- Detailed performance metrics and convergence analysis

## Dataset
The experiment uses a synthetic dataset with the following properties:
- 10000 samples
- 15 features (10 informative, 5 redundant)
- 6 classes with equal distribution
- Standardized preprocessing

## Methodology
1. A synthetic multi-class dataset is generated using scikit-learn's `make_classification`
2. Basic exploratory data analysis is performed (class distribution, feature statistics, correlations)
3. The dataset is split into 10 different train/test samples (80%/20% split)
4. For each sample, SVM optimization is performed with various kernel configurations:
   - Linear kernel with different C values (0.1, 1.0, 10.0)
   - RBF kernel with different C values and gamma parameters
5. Accuracy is tracked across iterations to generate convergence history
6. Results are compiled and visualized

## Results
The experiment identified optimal SVM parameters across 15 different samples:

| Sample | Best Accuracy | Best SVM Parameters   |
|--------|----------------|------------------------|
| S1     | 0.865          | rbf, 1.000, 0.100      |
| S2     | 0.863          | rbf, 1.000, 0.100      |
| S3     | 0.859          | rbf, 1.000, 0.100      |
| S4     | 0.858          | rbf, 1.000, 0.100      |
| S5     | 0.852          | rbf, 1.000, 0.100      |
| S6     | 0.871          | rbf, 1.000, 0.100      |
| S7     | 0.860          | rbf, 1.000, 0.100      |
| S8     | 0.853          | rbf, 1.000, 0.100      |
| S9     | 0.852          | rbf, 1.000, 0.100      |
| S10    | 0.863          | rbf, 1.000, 0.100      |
| S11    | 0.864          | rbf, 1.000, 0.100      |
| S12    | 0.859          | rbf, 1.000, 0.100      |
| S13    | 0.859          | rbf, 1.000, 0.100      |
| S14    | 0.862          | rbf, 1.000, 0.100      |
| S15    | 0.860          | rbf, 1.000, 0.100      |

SVM Optimization Experiment Summary:
-----------------------------------
Dataset: Multi-class Synthetic Dataset
Samples: 10000
Features: 15
Classes: 6

Training/Testing Split: 80/20
Number of Different Samples: 15
Iterations per Sample: 300

Best Sample: S6
Best Accuracy: 0.871
(kernel - rbf, C - 1.000, gamma - 0.100)

## Visualizations
The experiment generates several visualizations:
- Convergence graph for the best-performing SVM
- Class distribution visualization
- Feature correlation heatmap

## Dependencies
- Python 3.x
- NumPy
- pandas
- scikit-learn
- Matplotlib
- seaborn

## Output Files
- `svm_optimization_results.csv`: Complete results table
- `best_svm_convergence.png`: Convergence graph for the best SVM
- `class_distribution.png`: Visualization of class distribution
- `feature_correlation.png`: Heatmap of feature correlations

## License
[MIT License](LICENSE)

## Colab Link
[Colab-Link](https://colab.research.google.com/drive/1XnJhK4-uHWzyb58cIKNzgNPx9e386HTd?usp=sharing)

## Owner
Samdeep Sharma
102217183
