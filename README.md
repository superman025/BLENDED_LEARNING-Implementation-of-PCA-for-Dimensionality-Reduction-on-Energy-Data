# BLENDED LEARNING
# Implementation of Principal Component Analysis (PCA) for Dimensionality Reduction on Energy Data

## AIM:
To implement Principal Component Analysis (PCA) to reduce the dimensionality of the energy data.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Data Import the dataset to begin the dimensionality reduction process.
2. Explore the Data Perform an initial analysis to understand data characteristics, distributions, and potential patterns.
3. Preprocess the Data (Feature Scaling) Scale features to ensure consistency, preparing the data for principal component analysis (PCA).
4. Apply PCA for Dimensionality Reduction Use PCA to reduce the dataset’s dimensionality while retaining the most significant features.
5. Analyze Explained Variance Assess the variance explained by each principal component to determine the effectiveness of dimensionality reduction.
6. Visualize Principal Components Create visualizations of the principal components to interpret patterns and clusters in reduced dimensions.




## Program:
```
/*
Program to implement Principal Component Analysis (PCA) for dimensionality reduction on the energy data.
Developed by: sri jai.v
RegisterNumber:  25018437
*/
/*
Program to implement Principal Component Analysis (PCA) for dimensionality reduction on the energy data.
Developed by: SRIJAI V
RegisterNumber:  25018437

import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv('HeightsWeights.csv')

print(data.head())
print(data.columns)

X = data[['Height(Inches)', 'Weight(Pounds)']]

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

explained_variance = pca.explained_variance_ratio_
print("Explained Variance Ratio for each Principal Component:", explained_variance)
print("Total Explained Variance:", sum(explained_variance))
print("\nName: DEEPAK B")
print("Reg. No: 25018314\n")

pca_df = pd.DataFrame(X_pca, columns=['PC1', 'PC2'])

plt.figure(figsize=(8, 6))
sns.scatterplot(x='PC1', y='PC2', data=pca_df, alpha=0.7)
plt.xlabel("Principal Component 1")
plt.ylabel("Principal Component 2")
plt.title("PCA - Heights and Weights Dataset")
plt.show()
*/
```

## Output:
<img width="915" height="706" alt="Screenshot 2026-03-28 020426" src="https://github.com/user-attachments/assets/79cec710-07f8-45f5-b8ff-7c6a831fb100" />




## Result:
Thus, Principal Component Analysis (PCA) was successfully implemented to reduce the dimensionality of the energy dataset.
