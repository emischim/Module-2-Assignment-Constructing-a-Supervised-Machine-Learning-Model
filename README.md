# Project Title
**Constructing a Supervised Machine Learning Model**

## Project Overview
This project focuses on predicting sales using a **Random Forest Regression model**. We started with basic modeling, evaluated its performance, and progressively optimized the model. This involved dataset augmentation, feature selection, and hyperparameter tuning to improve prediction accuracy.

## Using Google Colab, and uploading the notebook attached in this repo, the below summary can be gotten

## Workflow Summary
The following steps were carried out to achieve the final optimized results:

### 1. **Initial Model Setup (Linear Regression)**
- **Purpose:** Establish a baseline for performance.
- **Model:** Simple Linear Regression.
- **Results:**
  - **MAE:** 2560.17
  - **MSE:** 8,972,062.42
  - **R²:** -0.14
- **Observations:** The linear regression model performed poorly, indicating the need for a non-linear model to capture complex relationships.

### 2. **Switch to Random Forest Regression**
- **Purpose:** Use a more robust, non-linear model.
- **Initial Random Forest Results:**
  - **MAE:** 2321.11
  - **MSE:** 7,540,268.12
  - **R²:** 0.12
- **Observations:** While performance improved over linear regression, the model was still underperforming due to overfitting and lack of optimization.

### 3. **Model Optimization**
We performed the following optimizations:
- **Dataset Augmentation:** Increased the dataset size to provide more training examples for the model.
- **Hyperparameter Tuning:** Optimized key Random Forest parameters (e.g., `n_estimators`, `max_depth`, `min_samples_split`) using GridSearchCV.

#### Results After Optimization (Augmented Data):
- **MAE:** 1555.47
- **MSE:** 3,622,391.86
- **R²:** 0.47
- **Observations:** Significant improvement in model performance; however, further analysis showed that redundant features were impacting accuracy.

### 4. **Feature Selection**
- **Purpose:** Reduce noise and simplify the model by selecting the most relevant features.
- **Method:** Recursive Feature Elimination (RFE) was used to identify the top 2 features.
- **Results After Feature Selection:**
  - **MAE:** 785.98
  - **MSE:** 1,393,549.29
  - **R²:** 0.80

---

## Final Results Summary
The table below shows the comparison of results at each stage:

| Model/Stage                     | MAE       | MSE          | R²    |
|---------------------------------|-----------|--------------|-------|
| **Linear Regression**           | 2560.17   | 8,972,062.42 | -0.14 |
| **Initial Random Forest**       | 2321.11   | 7,540,268.12 | 0.12  |
| **Optimized Random Forest**     | 1555.47   | 3,622,391.86 | 0.47  |
| **Random Forest + Feature Selection** | 785.98    | 1,393,549.29 | 0.80  |

---

## Key Improvements
1. **Dataset Augmentation:** Increased data size to improve generalization.
2. **Hyperparameter Tuning:** Optimized Random Forest parameters for better fit.
3. **Feature Selection:** Reduced the model complexity by focusing on the top 2 predictive features.

---

## Visualizations
The final scatter plot below shows the alignment of the predictions with the actual values after optimization and feature selection:

- **Blue Dots:** Model predictions.
- **Red Line:** Perfect prediction line (ideal case).

---

## Conclusion
By optimizing the Random Forest model and applying feature selection, the prediction performance improved significantly. The final model achieves:
- **MAE:** 785.98
- **MSE:** 1,393,549.29
- **R²:** 0.80

This demonstrates a robust predictive performance with minimal error and high explanatory power.

---

## Next Steps
To further enhance the model:
1. **Model Stacking:** Combine Random Forest with other models (e.g., XGBoost).
2. **Advanced Feature Engineering:** Derive new features (e.g., polynomial or interaction terms).
3. **Address Low Prediction Accuracy for Smaller Sales:** Weight the model to handle smaller sales values.

---

## Project Structure
- **data/**: Contains the dataset used for training and testing.
- **scripts/**: Python scripts for data preprocessing, modeling, and optimization.
- **results/**: Output results, visualizations, and performance metrics.
- **README.md**: Project summary and workflow documentation.

---

## Author
[Your Name]  
**Date:** [Today's Date]
