# Machine Learning Foundations Course
Official curriculum for the Machine Learning Foundations course in Zindua's Data Science Core Program.

- **Course Description:** A 5-week course that takes learners from their first model to an evaluated, deployable machine learning solution. Learners build progressively — data cleaning, preprocessing and feature engineering, then linear and regularised regression models, then non-linear classifiers and ensembles, then rigorous model evaluation and diagnosis — before completing a capstone project.

- **Course Objective:** Equip learners to prepare data, train, tune and evaluate supervised machine learning models with scikit-learn, and to justify model choices with appropriate metrics, validation and error analysis.

- **Skills to be learned:** Scikit-learn, data cleaning & preprocessing, feature engineering, imbalanced data (SMOTE), linear & polynomial regression, regularisation (Lasso, Ridge, Elastic Net), logistic regression, KNN, Naive Bayes, SVMs, decision trees, random forests, ensemble methods, cross-validation, hyperparameter tuning, Streamlit


## Curriculum Breakdown
### Week 1: Introduction
> **Objective:** Prepare data for modelling: learners will be able to distinguish supervised from unsupervised learning, clean data by handling missing values and outliers, encode and scale features, engineer features from text, image and imbalanced data, and set up sound train-test and cross-validation splits.
- **Intro to Machine Learning:** What is ML, Supervised vs Unsupervised Learning, Intro to Scikit Learn
- **Data Cleaning:** Missing Values, Outlier Handling, Exploratory Data Analysis (Data Quality)
- **Data Preprocessing:** Categorical Encoding, Feature Scaling, Model Selection (Train-Test vs Cross Val)
- **Feature Engineering:** Text Data, Image Data, Imbalanced Data (SMOTE)
- **Project:** [The Chip Dataset Cleaning Project](https://www.kaggle.com/code/wilkersonsalisi/cpu-gpu-advancements-exploratory-data-analysis)

### Week 2: Regression (Linear Models)
> **Objective:** Model continuous outcomes: learners will be able to fit linear regression with OLS and gradient descent, manage the bias-variance trade-off with polynomial features and pipelines, regularise models with Lasso, Ridge and Elastic Net, and apply generalised linear models including logistic regression.
- **Ordinary Least Squares:** Linear Regression, Gradient Descent, Regression Model Results
- **Polynomial Regression:** Bias-Variance Trade-Off, Polynomial/Functional Transformation, SkLearn Pipelines
- **Regularisation:** Lasso Regression, Ridge Regression, Elastic Net Regression
- **Generalised Linear Models:** Gauss Markov Assumptions, Twidie Regressor, Logistic Regression
- **Project:** [Blueberry Yield Prediction](https://www.kaggle.com/t/e21666c9c8934f1b89f598f5868a2878)

### Week 3: Classification (Non-Linear Models)
> **Objective:** Model categorical outcomes: learners will be able to train and compare KNN, Naive Bayes, support vector machines and tree-based classifiers, and improve performance with bagging, boosting and stacking ensembles.
- K-Nearest Neightbours & Naive Bayes
- Support Vector Machines
- **Tree Classifiers:** Decision Trees, Random Forests, Visualising Trees
- **Advanced Ensemble Methods:** Stacking, Bagging, Boosting
- **Project:** [Credit Risk Modelling](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

### Week 4: Model Evaluation
> **Objective:** Prove a model works before trusting it: learners will be able to evaluate regression and classification models with the right metrics, tune hyperparameters with grid and randomised search, diagnose models with learning curves and error analysis, calibrate predictions, and deploy a model with Streamlit.
- **Regression Model Evaluation:** Regression Metrics, Grid Search CV, Randomised Search CV
- **Classification Model Evaluation:** Confusion Matrix, ROC-AUC Curve, Visualising Grid Search Results
- **Applied Machine Learning:** Error Analysis, Bias-Variance Analysis, End-to-end ML Project
- **Diagnosing ML Models:** Learning Curves, Calibration & Discretisation, Streamlit Deployment
- **Project:** [Loan Default Prediction](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)(Handle Imbalances, Discretise, & Calibrate)
  
### Week 5: Conclusion
> **Objective:** Deliver an end-to-end ML project: learners will be able to frame a real-world problem, build and evaluate a model pipeline, and communicate its performance and limitations.
- **Capstone Projects:**  Choose from an assortment of projects
- **Optional Bonus Lessons:** Deploy ML Models with Streamlit, XGBoost ML Library, OpenCV Image Processing
- **Further Resources:** Scikit Learn Documentation, Andrew NG Official ML Notes, StatQuest YouTube Channel

### Pushed to the Advanced ML Course
The following are gaps from the foundations course that will be covered in the Advanced Machine Learning Course:
- **Anomaly Detection (Outliers):** Ideally covered when going through clustering
- **Advanced Feature Engineering:** Feature Selection, Dimensionality Reduction, and Discriminant Analysis

Here are some projects pushed to Advanced ML course since they require the three concepts above:
- [Brain Tumor Classification](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri) (Involves image processing)
- [Advanced House Price Regression](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) (Involves advanced feature engineering)

**Note:** There's quite a number of machine learning projects across all level on [this blog by Project Pro](https://www.projectpro.io/article/top-10-machine-learning-projects-for-beginners-in-2021/397)

## Contributors & Acknowledgements
### Course Owner(s)
This course has been curated :
- [Cyril Michino](https://github.com/cyrilmichino), Co-founder at Zindua School and previously a Data Science technical mentor
- [Victor Nduti]

### Acknowledgements
Here are the different sources used to compile this Machine Learning course:
1. [Cornell Tech Applied Machine Learning](https://www.youtube.com/playlist?list=PL2UML_KCiC0UlY7iCQDSiGDMovaupqc83) by Volodymyr Kuleshov
2. [Stanford Machine Learning Course](https://youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&si=9eUStpAJJXNbv65p) by Andrew NG
2. [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) by Jake VanderPlas
5. [Deeplearning.ai Machine Learning Specialisation](https://www.deeplearning.ai/courses/machine-learning-specialization/) by Andrew NG, Eddy Shyu, Aarti Bagul, Geoff Ladwig
5. [Hole House Andrew NG Notes](https://www.holehouse.org/mlclass/index.html)
