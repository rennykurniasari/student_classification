# Students Classification using Machine Learning

## Business Overview
Machine learning's numerous implications include improving business decision-making. This project provides a practical illustration of this use case. It focuses on predicting the likelihood of a student enrolled for a free plan purchasing a subscription on an online course platform. The decision is based on students' activities on the platform—viewing lectures and participating in exams.

This project is inspired by an initiative of an online course platform in 2022 to predict student purchases before the Black Friday campaign. I wanted to create a list of students likelier to purchase and retarget them with unique ads on social media. But as it turned out, this was no easy task due to the extreme imbalance of the data—the number of students who had never purchased a subscription was much higher than the number of students who had. The primary reason for that was the free campaign that ran before the Black Friday one, where the platform was unlocked for free to all students.

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

## Confusion Matrices Result
|Logistic Regression                       |Precision	     |Recall	 |F1-Score	 |
|:------------------------------|:---------|:-----------|:-----------|
Class 0       |0.97	|0.99	|0.98	
Class 1       |0.83	|0.66	|0.74

|K-Nearest Neighbors                      |	     |	     |	     |
|:------------------------------|:---------|:-----------|:-----------|
Class 0       |0.97	|0.98	|0.98	
Class 1       |0.79	|0.71	|0.75
|Support Vector Machines                      |	     |	     |	     |
Class 0       |0.97	|0.98	|0.98	
Class 1       |0.81	|0.68	|0.74
|Decision Trees                      |	     |	     |	     |
Class 0       |0.98	|0.98	|0.98	
Class 1       |0.81	|0.76	|0.78
|Random Forests                     |	     |	     |	     |
Class 0       |0.97	|0.98	|0.98	
Class 1       |0.82	|0.74	|0.78

## Result Interpretation
Throughout this project, I've developed multiple classification models with the aim of identifying the one that most precisely categorizes students into **'potential purchasers'** and **'unlikely purchasers'** based on their platform activity. When accurate, such predictions are highly crucial for a business, enabling the marketing team to focus resources on promoting the product to the demographic most likely to express interest and benefit from a subscription.

The objective was to sift through registered students likely to take advantage of a discounted subscription price. However, a significant challenge arose.

The dataset obtained for the Black Friday analysis shared a notable drawback with this project: extreme imbalance. In simple terms, the number of instances in one class (students who haven’t purchased a subscription) substantially exceeded that in the second class (users who have).

This outcome is to be expected, as many users sign up primarily to explore the product and skim through the pages. Some of them, however, engage with the platform to access the free content, displaying behavior similar to that of students who eventually subscribe. This overlap makes it challenging to exclusively isolate the latter group. It also leads to the conclusion that the features included in this database are insufficient, necessitating a deeper understanding of users' behavior and background.
