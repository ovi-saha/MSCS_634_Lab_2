# MSCS_634_Lab_2 – Classification Using KNN and RNN
This Repo is Lab 2: Classification Using KNN and RNN for MSCS 634
## Purpose
This lab explores and compares the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classifiers using the Wine dataset from sklearn. The goal is to understand how different parameter values (k for KNN and radius for RNN) affect classification accuracy and to analyze which model is better suited for various data scenarios.

## Key Insights
- **KNN Performance:** The K-Nearest Neighbors classifier achieved consistently high and stable accuracy across moderate k values. Accuracy improved from k = 1 to k = 5, then remained stable at higher values, indicating that tiny k can lead to overfitting (relying too much on a single neighbor). In contrast, moderate k values provide a balance between overfitting and underfitting. This shows that KNN generalizes well for the Wine dataset and is less affected by local fluctuations in data density or outliers.  

- **RNN Performance:** The Radius Neighbors classifier showed more variability in performance depending on the radius parameter. Small radii sometimes led to test samples having too few or no neighbors, resulting in lower accuracy. Large radii included neighbors from different classes, potentially reducing the classifier's ability to distinguish between them. Moderate radius values captured enough neighbors for reliable classification, demonstrating that RNN is highly sensitive to distance thresholds and local data density.  

- **Comparison:** Overall, KNN provided more consistent and reliable results for this dataset, while RNN performance depended heavily on parameter tuning. Visualization of accuracy trends clearly shows that KNN's stability makes it suitable for datasets with relatively uniform feature scales. In contrast, RNN may be preferable for datasets with varying density, provided the radius is carefully chosen.

- Visualization of accuracy trends helped illustrate the differences between the two methods.

## Challenges and Decisions
- Selecting appropriate radius values for RNN required trial and error to ensure each test sample had enough neighbors.  
- Stratified sampling was used during the train-test split to maintain the original class distribution in both sets.  
- Accuracy was chosen as the primary metric to evaluate model performance, though other metrics like precision or recall could provide additional insight.  
- Decisions on parameter selection (k for KNN, radius for RNN) were made to balance overfitting and underfitting and ensure fair comparison.

