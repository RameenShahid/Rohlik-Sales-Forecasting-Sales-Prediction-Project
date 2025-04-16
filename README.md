# Optimizing Sales Prediction for Rohlik with Machine Learning and Weighted MAE Evaluation
### Libraries Used

#### Data Handling & Computation:
- **pandas**: Used for data manipulation and preprocessing.
- **numpy**: Provides numerical computing capabilities, especially for handling arrays and mathematical functions.

#### Visualization:
- **matplotlib**: Used for creating static, animated, and interactive visualizations.
- **seaborn**: Built on top of Matplotlib, provides enhanced data visualization features.

#### Machine Learning:
- **scikit-learn**: Includes tools for machine learning models, preprocessing, feature selection, and evaluation metrics.

#### Model Serialization:
- **joblib**: Utilized for saving and loading trained models efficiently.

#### APIs & Deployment:
- **Flask**: Used for building APIs to serve machine learning predictions.
- **Docker**: A containerization tool used for deploying the API in a scalable and reproducible environment.

---

### Workflow Summary

#### Data Preparation

**Handling Missing Values:**
- Filled NaN values in `holiday_name` with "No Holiday" to ensure continuity in data.

**Feature Engineering:**
- Extracted date-related features such as **year, month, day, weekday, and weekend indicators**.
- Created **lag and rolling features** like `lag_1` and `rolling_mean_7` to incorporate past trends.
- Added **holiday indicators** to account for special dates impacting sales.

---

### Model Training & Evaluation

#### Regression Models:
- **Linear Regression**: Evaluated using MAE, MSE, and RMSE.

#### Classification Models:
- **Logistic Regression**: Assessed based on accuracy and confusion matrix.

#### Key Metrics:
- **MAE (Mean Absolute Error)**: Measures the average magnitude of errors in predictions.
- **MSE/RMSE (Mean Squared Error & Root Mean Squared Error)**: Penalizes large errors more significantly.
- **MAPE/SMAPE (Mean Absolute Percentage Error & Symmetric MAPE)**: Useful for percentage-based errors.
- **R-squared**: Indicates how well the model explains variability in the data.
- **WMAE (Weighted Mean Absolute Error)**: Assigns more importance to specific observations, like holiday sales.

---

### Optimization

**Hyperparameter Tuning:**
- Applied **GridSearchCV** and **RandomizedSearchCV** for optimal parameter selection.

**Feature Selection:**
- Techniques included **Recursive Feature Elimination (RFE)**, **SelectKBest**, and correlation analysis.

**Ensemble Methods:**
- Utilized **RandomForest** and **GradientBoosting** for improving model performance.

**Regularization:**
- Applied **L1/L2 regularization** to prevent overfitting.

---

### Deployment

**Model Saving:**
- Serialized models using **joblib** for easy reusability.

**API Creation:**
- Developed a **Flask API** to serve predictions efficiently.

**Containerization:**
- Packaged the application into a **Docker container** for deployment.

**Cloud Deployment:**
- Hosted the API on cloud platforms like **Heroku** to enable accessibility.


### Visualization Techniques

- **Actual vs. Predicted Plots:** Bubble charts where size/color represents weights.
- **Error Distribution:** Visualized using **bar plots** and **boxplots**.
- **Residual Analysis:** Scatter plots showing residuals vs. actuals.
- **Metric Comparison:** Comparative bar plots for **MAE vs. WMAE**.

---

### Key Takeaways

- **Focus on WMAE:** Prioritizes key observations such as holiday sales.
- **Optimization Matters:** Feature selection and hyperparameter tuning enhance model accuracy.
- **Deployment Readiness:** APIs and Docker ensure scalability and accessibility.



