# Advanced Machine Learning Course
Official curriculum for the Advanced Machine Learning course in Zindua' s Data Science Core Program.

- **Course Description:** A 5-week course that takes learners beyond supervised learning to unsupervised methods, time series and deep learning. Learners build progressively — reducing dimensionality and selecting features, then discovering structure with clustering, then forecasting with time-series models, then building neural networks — before completing a capstone project.

- **Course Objective:** Equip learners to apply unsupervised learning, forecasting and deep learning techniques to complex, high-dimensional data, and to choose the right method for a problem based on its structure and evaluation results.

- **Skills to be learned:** PCA, manifold learning, feature selection, anomaly detection, K-Means, Gaussian Mixture Models, kernel density estimation, hierarchical clustering, time-series analysis & forecasting, Prophet, neural networks, CNNs, sequential models, pre-trained & generative models, TensorFlow/Keras


## Curriculum Breakdown
### Week 1: Dimensionality Reduction
> **Objective:** Simplify high-dimensional data without losing signal: learners will be able to reduce dimensionality with PCA and manifold learning, select informative features, and detect anomalies before modelling.
- **PCA:** What is ML, Supervised vs Unsupervised Learning, Intro to Scikit Learn
- **Advanced PCA:** Missing Values, Outliers, Duplicate Data, Data Quality, Exploratory Data Analysis
- **Manifold Learning:** Text Data, Image Data, Feature Creation, Log Transformation, Polynomial Tranformation
- **More Manifolds:** Categorical Encoding, Feature Scaling, Test-Train Split, Cross-Validation
- **Advanced Feature Engineering:** Feature Selection, Dimensionality Reduction, and Discriminant Analysis
- **Project:** [Ecommerce Sales Data Preparation](https://www.kaggle.com/datasets/ahmedaliraja/e-commerece-sales-data-2023-24)  Anomaly Detection (Outliers): Ideally covered when going through clustering

### Week 2: Clustering
> **Objective:** Discover structure in unlabelled data: learners will be able to segment data with K-Means, Gaussian Mixture Models, kernel density estimation and hierarchical clustering, and choose and validate the number of clusters.
- K-Means Clustering    
- Gaussian Mixed Models
- **Kernel Density Estimation:** Bias-Variance Trade-Off, Polynomial Transformation, SkLearn Pipelines
- **Hierachichal Clustering:** Lasso Regression, Ridge Regression, Elastic Net Regression
- **Project:** [Car Price Regression](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)

### Week 3: Time Series Analysis
> **Objective:** Forecast values over time: learners will be able to decompose a time series into trend and seasonality, build baseline and statistical forecasting models in Python, and forecast with Prophet while evaluating accuracy on held-out periods.
- Intro-To Time Series
- Basic Models 
- **Time Series Forecasting in Python:** Decision Trees, Random Forests, Visualising Trees
- **Prophet:** Stacking, Bagging, Boosting
- **Project:** [Credit Score Classification](https://www.kaggle.com/datasets/parisrohan/credit-score-classification)

### Week 4: Deep Learning Foundations 
> **Objective:** Build and train neural networks: learners will be able to explain how neural networks learn, build convolutional networks for images and sequential models for ordered data, and apply pre-trained and generative models to new problems.
- **Intro to Neural Networks:** Regression Metrics, Grid Search CV, Randomised Search CV
- **Convolutional Neural Networks:** Classification Metrics, Confusion Matrix, ROC-AUC Curve
- **Sequential Models:** End-to-End ML Project, Optimising ML Models, Error Analysis
- **Deep Generative Models and Pre-Trained Models:** Class Imbalances, Calibration, Discretisation
- **Project:** [Loan Default Prediction](https://www.kaggle.com/datasets/yasserh/loan-default-dataset) 

### Week 5: Final Conclusion
> **Objective:** Deliver an advanced ML project: learners will be able to select and justify an unsupervised, forecasting or deep learning approach for a real-world problem, then build, evaluate and present the solution.
- **Capstone Projects:**  Choose from an assortment of projects
- **Optional Bonus Lessons:** Deploy ML Models with Streamlit, XGBoost ML Library, OpenCV Image Processing
- **Further Resources:** Scikit Learn Documentation, Andrew NG Official ML Notes, StatQuest YouTube Channel

Here are some projects pushed to Advanced ML course since they require the three concepts above:
- [Brain Tumor Classification](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri) (Involves image processing)
- [Advanced House Price Regression](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) (Involves advanced feature engineering)

**Note:** There's quite a number of machine learning projects across all level on [this blog by Project Pro](https://www.projectpro.io/article/top-10-machine-learning-projects-for-beginners-in-2021/397)

## Course Contributors
### Course Owner(s)
This course has been curated by [Cyril Michino](https://github.com/cyrilmichino), Co-founder at Zindua School, [Christopher Aloo](https://www.linkedin.com/in/christopher-aloo/) and [Victor Nduti](). 
Some of the content in the course has been sourced from multiple sources (Listed below under acknowledgements) as well as built from scratch alongside practice projects by the course owner.

### Acknowledgements
Here are the different sources used to compile this Machine Learning course:
1. [Deeplearnin.ai Machine Learning Specialisation](https://www.deeplearning.ai/courses/machine-learning-specialization/) by Andrew NG
2. [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) by Jake VanderPlas
3. [Stanford Machine Learning Notes](https://www.holehouse.org/mlclass/index.html) by Andrew NG
