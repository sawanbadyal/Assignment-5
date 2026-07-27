**Name: Sawanpreet Singh Badyal**\
**Reg No: 23BAI10793**\
**Application no: IN26010801**\
**Batch Number: 1(A)**\
**Email: sawanpreet.23bai10793@vitbhopal.ac.in**

# AI-ML-Assignment-5
Employee Attrition Prediction using Decision Tree and Random Forest Classification

# IBM HR Analytics Employee Attrition Prediction

## Objective
The objective of this project is to identify employees who are likely to leave the organization based on their demographic, professional, and work-related attributes. To achieve this, we developed and compared two machine learning classification models: a Decision Tree and a Random Forest.

## Dataset Link
[IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

## Libraries Used
*   `pandas`: For data manipulation and loading.
*   `numpy`: For numerical operations and array manipulations.
*   `scikit-learn` (`sklearn`): For machine learning model building, preprocessing, and evaluation metrics.
*   `matplotlib`: For creating static, basic data visualizations.
*   `seaborn`: For generating attractive statistical graphics (like confusion matrices).

## Methodology
1.  **Data Understanding:** Loaded the dataset, identified the target variable (`Attrition`), and separated the features into numerical and categorical lists. Explored the basic structure and summary statistics.
2.  **Data Preprocessing:** 
    *   Checked for missing values (none found).
    *   Removed redundant and zero-variance columns (`EmployeeCount`, `StandardHours`, `Over18`, `EmployeeNumber`).
    *   Encoded the target variable (`Yes` -> 1, `No` -> 0) and used one-hot encoding for the remaining categorical features.
    *   Split the data into training (80%) and testing (20%) sets using stratified sampling to maintain class proportions.
3.  **Model Development:** Trained a standard Decision Tree Classifier and an ensemble Random Forest Classifier (using 100 estimators).
4.  **Model Evaluation:** Evaluated both models on the testing set using Accuracy, Precision, Recall, and F1-Score. Generated confusion matrices for error analysis and a feature importance plot for the Random Forest model.

## Results
*   The models successfully identified key predictors of attrition. Financial and tenure-based metrics—specifically **Monthly Income**, **Age**, and **Total Working Years**—emerged as the strongest predictors of employee turnover.
*   Both models face challenges with Recall for the "Yes" (attrition) class due to the highly imbalanced nature of the dataset (~84% retention, 16% attrition), naturally biasing toward "No" predictions.

## Model Comparison
*   **Accuracy & Precision:** The Random Forest model consistently demonstrated higher overall accuracy and precision than the Decision Tree.
*   **Error Rates:** The Decision Tree produced a higher rate of False Positives (predicting an employee will leave when they actually stay), making it less reliable for targeted HR interventions.
*   **Generalization:** The Random Forest effectively reduced the variance and overfitting that single trees are prone to.

## Conclusion
The **Random Forest** model performed better than the single Decision Tree across most key evaluation criteria. 

Random Forest often outperforms single Decision Trees because it utilizes an ensemble learning technique. By creating multiple different trees based on random subsets of the data and averaging their predictions, Random Forest successfully neutralizes the variance and noise that often throw off single trees.
