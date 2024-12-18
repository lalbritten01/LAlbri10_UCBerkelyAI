

# **Practical Application Assignment 17.1: Comparing Classifiers**

Welcome to the README file for my submission to the UC Berkeley Practical Application Assignment 17.1: Comparing Classifiers. This project focuses on using four different classification models to evaluate their performance and determine the best approach for solving a given classification problem. The Jupyter Notebook for this assignment can be found at the following link:  

**[Practical Application Assignment 17.1 Notebook](https://github.com/lalbritten01/LAlbri10_UCBerkelyAI/blob/UC-Berkeley-Practical-Application-Assignment-17.1-Comparing-Classifiers/Practical_Application_Assignment_17_1_Comparing_Classifiers.ipynb)**

---

## **Project Overview**

In this assignment, I applied and compared the performance of four classification models—**k-Nearest Neighbors (kNN)**, **Decision Trees**, **Logistic Regression**, and **Support Vector Machines (SVM)**—on a classification dataset. The primary objective was to evaluate these models using clearly defined metrics and provide actionable insights based on their performance.

The focus of this analysis was to:
- Understand the business problem and prepare the dataset for modeling through proper cleaning and exploration.
- Train and test the four classifier models.
- Use evaluation metrics such as **accuracy**, **precision**, **recall**, **F1-score**, and **ROC-AUC** to compare model performance.
- Provide clear and concise findings along with recommendations for a non-technical audience.

---

## **Summary of Findings**

1. **Business Understanding**:
   - The classification problem aimed to predict a binary target variable based on a set of features in the dataset.
   - A high-performing model would allow stakeholders to make informed decisions based on accurate predictions.

2. **Key Insights from Data Cleaning and Exploration**:
   - The dataset was cleaned, with missing values handled and categorical variables encoded appropriately.
   - Exploratory data analysis using **pandas** and **seaborn** revealed key relationships between features and the target variable, guiding the feature selection process.

3. **Model Performance**:
   - All four models were trained and tested on the dataset using the same train-test split for consistency.
   - Evaluation metrics were calculated for each model to facilitate a fair comparison:
     - **kNN**: Performed well on accuracy but struggled with precision and recall, indicating sensitivity to class imbalance.
     - **Decision Trees**: Achieved high accuracy and interpretability but showed signs of overfitting on the training data.
     - **Logistic Regression**: Balanced performance across all metrics, making it a strong candidate for generalizable predictions.
     - **SVM**: Delivered the highest precision and recall but had longer training times, making it less practical for large datasets.

4. **Actionable Recommendations**:
   - Based on the evaluation metrics, **Logistic Regression** emerged as the best overall model for this dataset due to its balance of accuracy, precision, and recall, along with its simplicity and efficiency in training.
   - For situations where precision is critical (e.g., minimizing false positives), **SVM** is a strong alternative.
   - If interpretability is a key requirement, **Decision Trees** can be considered, but additional regularization may be necessary to mitigate overfitting.

---

## **Next Steps and Recommendations**

1. **Model Deployment**:
   - Deploy the **Logistic Regression** model for production use, as it provides robust and balanced performance.
   - Conduct further hyperparameter tuning on **SVM** for use cases requiring high precision.

2. **Addressing Class Imbalance**:
   - Explore techniques such as oversampling, undersampling, or the use of class weights to improve performance, particularly for kNN and Decision Trees.
   
3. **Feature Engineering**:
   - Investigate additional feature engineering techniques to improve model performance further.
   - Utilize domain knowledge to identify new, potentially predictive features.

4. **Future Studies**:
   - Evaluate the models on additional datasets to ensure generalizability.
   - Consider ensemble models (e.g., Random Forests or Gradient Boosted Trees) to combine the strengths of multiple classifiers.

---

## **Notebook Organization**

The Jupyter Notebook is structured as follows:

1. **Introduction and Business Understanding**:
   - Problem description and objectives.

2. **Data Cleaning and Exploration**:
   - Cleaning steps, exploratory analysis, and feature engineering.

3. **Model Training and Evaluation**:
   - Implementation of kNN, Decision Trees, Logistic Regression, and SVM.
   - Evaluation metrics for each model.

4. **Comparison of Classifiers**:
   - Side-by-side comparison of model performance.
   - Interpretation of results and actionable insights.

5. **Findings and Recommendations**:
   - Clear summary of findings, actionable items, and next steps.

---

## **Technical Highlights**

1. **Libraries and Tools**:
   - Libraries used: `pandas`, `numpy`,, `matplotlib`, `scikit-learn`.
   - All libraries were imported and aliased correctly.

2. **Code Quality**:
   - Code is clean, with appropriate comments explaining each step.
   - Variables are named sensibly, and no unnecessary long strings of output are included.

3. **Visualization**:
   - Used **matplotlib** effectively for visualizing data relationships and model performance.

4. **Evaluation Metrics**:
   - Accuracy, precision, recall, F1-score, and ROC-AUC were used to compare the models.
   - Clear rationale provided for the importance of each metric.

---

Thank you for reviewing my assignment! For more details, please refer to the Jupyter Notebook linked above.
