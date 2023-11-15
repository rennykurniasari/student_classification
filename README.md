# Student Classification and Forecasting using Machine Learning

## Business Overview
Machine learning has transformative implications for enhancing business decision-making, particularly in predicting user behavior. This project serves as a practical example, focusing on forecasting the likelihood of a student, initially registered for a free plan, upgrading to a paid subscription on an online learning platform. The decision-making process leverages student activities on the platform, such as watching lectures and engaging in exams.

The initiative stems from the 2022 goal to predict student purchases before the Black Friday campaign, with the aim of creating a targeted list for advertisement retargeting on social media. However, the project faced challenges due to a significant imbalance in the dataset, primarily resulting from a preceding free campaign that unlocked the platform for all students.

## Business Objective
1.   **Predictive Advertising**
<br>Forecasting potential customer behavior to target advertisements effectively.

2.  **Subscription Conversion**
<br>Identifying students likely to upgrade from a free plan to a paid subscription.

## Business Impact
This analysis is crucial for online learning platform companies, allowing for strategic budget allocation towards potential customers, leading to increased revenue through targeted advertising and exclusive offers.

---

## Project Highlights
1.   **Machine Learning Models**
<br>Utilizing various models, including logistic regression, k-nearest neighbors, support vector machines, decision trees, and random forests.

2.   **Data Imbalance Challenge:**
<br>Addressing the imbalance in the dataset where the number of students retaining the free plan exceeds those predicted to make a purchase.

3.   **Data Resampling Research**
<br>Encouraging exploration of different data resampling methods, such as oversampling, undersampling, and SMOTE.

## Methodology
This project follows a comprehensive methodology that involves data preprocessing and the application of various machine learning models to achieve the objective of predicting student subscription upgrades.

## Key Components
1.   **Data Preprocessing**
    *   **Removing Outliers:** Identify and eliminate data points that deviate significantly from the norm to ensure model accuracy and reliability.
    *   **Checking for Multicollinearity:** Assess and address multicollinearity issues among predictor variables to enhance model interpretability.
    *   **Dealing with NaN Values:** Handle missing data through imputation or removal to maintain the integrity of the dataset.
    *   **Splitting the Data:** Divide the dataset into training and testing sets to evaluate model performance effectively.
    *   **Encoding the Data:** Convert categorical variables into a numerical format, ensuring compatibility with machine learning algorithms.

2.   **Logistic Regression Model**
<br>Apply logistic regression, a widely-used classification algorithm, to predict the likelihood of students upgrading to a paid subscription.

3.   **K-Nearest Neighbors Model**
<br>Implement the k-nearest neighbors algorithm to classify students based on their similarity to others in the dataset.

4.   **Support Vector Machines Model**
<br>Utilize support vector machines, a powerful classification method, to separate and classify students into subscription upgrade categories.

5.   **Decision Trees Model**
<br>Employ decision tree modeling to create a predictive model based on hierarchical decision rules.

6.   **Random Forests Model**
<br>Develop a random forests model, an ensemble learning technique, to improve prediction accuracy through the aggregation of multiple decision trees.

## Data Dictionary
|variable                       |class     |description |
|:------------------------------|:---------|:-----------|
student_country        |object| country of the student
days_on_platform       |int64 | number of days the student has been on the platform
minutes_watched        |float64 | total minutes the student spent watching content
courses_started        |int64 | number of courses the student initiated
practice_exams_started  |int64 | number of practice exams the student began
practice_exams_passed   |int64 | number of practice exams the student passed
minutes_spent_on_exams  |float64 | total minutes the student spent on exams
purchased              |int64 | indicator of whether the student made a purchase (1 for yes, 0 for no)

## Dependencies
*   `pip install pandas`
*   `pip install matplotlib`
*   `pip install statsmodels`
*   `pip install scikit-learn`
*   `pip install numpy`
*   `pip install seaborn`

---

## Result Interpretation
Throughout this project, multiple classification models were developed to accurately categorize students as **'potential purchasers'** and **'unlikely purchasers'** based on their platform activity. The goal was to enhance marketing strategies, concentrating resources on the demographic most likely to benefit from a subscription. Despite the impressive overall accuracy of approximately 0.96, a significant hurdle arose due to an extreme class imbalance in the dataset.

### Observations from Confusion Matrices
|Logistic Regression                       |Precision	     |Recall	 |F1-Score	 |
|:------------------------------|:---------|:-----------|:-----------|
Class 0       |0.97	|0.99	|0.98	|
Class 1       |0.83	|0.66	|0.74   |
|**K-Nearest Neighbors**                      |	     |	     |	     |  
Class 0       |0.97	|0.98	|0.98	|
Class 1       |0.79	|0.71	|0.75   |
|**Support Vector Machines**                       |	     |	     |	     | 
Class 0       |0.97	|0.98	|0.98	|
Class 1       |0.81	|0.68	|0.74   |
|**Decision Trees**                       |	     |	     |	     |
Class 0       |0.98	|0.98	|0.98	|
Class 1       |0.81	|0.76	|0.78   |
|**Random Forests**                       |	     |	     |	     |
Class 0       |0.97	|0.98	|0.98	|
Class 1       |0.82	|0.74	|0.78   |

Observing the confusion matrices and classification reports, the models demonstrated high accuracy primarily because many students were correctly predicted to retain their free plan. However, precision and recall metrics for the second class (users likely to purchase) were not as high. Notably, decision trees and random forests models exhibited the highest F1 scores for both classes.

### Utilizing Model Results
The models, despite their high accuracy, serve as valuable tools for the marketing team to optimize campaign budgets and target potential subscribers through paid social media advertisements and exclusive offers. However, it's essential to acknowledge that these predictions, based solely on platform activity, do not guarantee a 100% success rate. Purchasing decisions are influenced by various factors beyond platform behavior, such as demographics, financial status, and daily workload.

### Improving Model Performance
1.  **Addressing Imbalanced Data**
<br>Techniques like oversampling, undersampling, and hybrid methods (e.g., SMOTE) can be employed to balance the dataset. Care must be taken to avoid information loss or introduction of artificial data.

2.  **Exploring Additional Variables**
<br>Including more independent variables (e.g., participation in the Q&A hub, number of logins, price page visits) could enhance model performance.

3.  **Grid Searches and Fine-Tuning**
<br>Conduct more exhaustive grid searches and fine-tuning to optimize model hyperparameters.

4.  **Implementing Neural Networks**
<br>Beyond traditional machine learning, consider implementing neural network models to capture patterns that might be missed by conventional models.

Despite the challenges posed by imbalanced datasets, careful management and thoughtful application of these techniques can yield reliable and insightful results, contributing to the ongoing improvement of predictive models.


---

## How to Contribute
Feel free to contribute to the Student Classification and Forecasting using Machine Learning project by providing additional insights, expanding analyses, or improving code efficiency. Simply fork the repository, make your changes, and submit a pull request. Your contributions are highly valued and play a crucial role in enhancing the project. Thank you for contributing!
