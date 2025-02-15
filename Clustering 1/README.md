# Clsutering Project 1 

## Overview 
The data is hard to interpreet by human eye since it is just numbers with slightly high dimensionality. 
We need to cluster this data with the best clustering method using k means algorithhm 
data shape (98000, 30)

---

## Key Steps

### 1. infering meaning from our data
describe() method expalins the data and i see that our data points are close with a std of raning between 1 -4 but this does not mean that  the actual feature values do not differ significantly in magnitude. Since i am planning to apply umap, i need to scale my data, since UMAP (and many clustering algorithms) rely on distance metrics, scaling can help maintain the integrity of the clustering process by ensuring that the distances reflect the true relationships between data points.

Clustering alogrithms may be snesitive to differnet scales in the data and we plan to feeed our data to k means alogirthm  scaling beforehand can help maintain consistency across your workflow.

---

### 2. Data Visualization
- **Matplotlib & Seaborn**: We created various plots (e.g., histograms, pair plots, correlation heatmaps) using `plt.subplots()` and Seaborn functions.
- **Insights**: These visualizations provided a clearer picture of feature distributions and relationships within the data.

![Plots](screenshots/plot_w_sns_plt.png)

---

### 3. Grid Search for Model Tuning
- **Model Selection**: We experimented with multiple classification algorithms (e.g., Logistic Regression, SVM, Random Forest). Random Forest gave the most promising initial results.
- **Hyperparameter Optimization**: We used Grid Search to fine-tune parameters such as `n_estimators`, `max_depth`, and more.
  
  ![Parameters](screenshots/parameters.png)

---

### 4. Results
- **Final Model**: After applying the optimized hyperparameters to the entire dataset, our Random Forest model achieved an accuracy of **~80%** on the private leaderboard of Kaggle.
- **Significance**: This performance is notable given the high dimensionality and relatively small sample size.

---

## Conclusion

By combining **correlation-based feature filtering**, **comprehensive data visualization**, and a **hyperparameter-tuned Random Forest**, we effectively tackled a complex, high-dimensional dataset to predict Schizophrenia with solid accuracy. 

**Potential Next Steps**  
- **Further Dimensionality Reduction**: Techniques like PCA or autoencoders may uncover more compact representations.  
- **Advanced Models**: Exploring deep learning architectures could improve performance further.  
- **Data Expansion**: Collecting additional samples or leveraging domain knowledge may help refine model accuracy and interpretability.


