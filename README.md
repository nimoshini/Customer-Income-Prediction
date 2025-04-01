📊 CENSUS INCOME PREDICTION ANALYSIS
📌 Dataset Overview
The Census Income Dataset contains demographic and employment details of individuals. The goal is to predict whether a person earns more than $50K per year based on given attributes.

🔹 Target Variable:
✅ <=50K (Encoded as 0)
✅ >50K (Encoded as 1)

DATASET FEATURES
🔢 Numerical Features
age: Individual’s age.

fnlwgt: Final weight assigned to observation.

education-num: Number of years of education.

capital-gain: Capital gain in income.

capital-loss: Capital loss in income.

hours-per-week: Weekly working hours.

🔠 Categorical Features
workclass: Type of employer (e.g., Private, Government).

education: Education level (e.g., Bachelors, HS-grad).

marital-status: Marital status (e.g., Married, Single).

occupation: Type of job (e.g., Tech-support, Sales).

relationship: Family role (e.g., Husband, Wife).

race: Ethnicity of the individual.

sex: Gender of the individual.

native-country: Country of origin.

📌 Note: All categorical features were label-encoded before training the models.

🚀 MODEL PERFORMANCE SUMMARY

Implemented three machine learning models for classification:

📉 Logistic Regression	              82.79%
🌳 Decision Tree	              86.00%
🌲 Random Forest	              86.44%

🔬 MODEL ANALYSIS

📉 Logistic Regression
📌 Description:

A linear model using the sigmoid function to estimate class probabilities.

It is highly interpretable, making it easy to see feature impacts.

📉 Limitations:

Assumes a linear relationship between features and target variable.

Struggles with complex patterns in data.

✔ Accuracy: 82.79% (Lowest among models)

🌳 Decision Tree Classifier (Optimized max_depth)
📌 Description:

Splits data based on feature conditions.

Captures non-linear relationships and is easy to interpret.

📌 Optimization:

Tested max_depth from 1 to 20 using brute force to find the best value.

⚠️ Limitations:

Overfitting risk if depth is too high.

Sensitive to small changes in data.

✔ Best max_depth: Found through brute force.
✔ Accuracy: 86.00%

🌲 Random Forest Classifier (Using GridSearchCV for Best Parameters)
📌 Description:

An ensemble model that builds multiple Decision Trees and combines outputs.

Reduces overfitting and improves accuracy.

📌 Hyperparameter Tuning (Using GridSearchCV):

n_estimators (Number of trees): 50, 100, 200

max_depth: 10, 20, 30

min_samples_split: 2, 5, 10

📌 Best Parameters Found:
✔ n_estimators: 200
✔ max_depth: 20
✔ min_samples_split: 5

🚀 Advantages:
✅ More robust than a single Decision Tree.
✅ Handles imbalanced data well.

⚠️ Limitations:

Computationally expensive for large datasets.

Less interpretable than a single Decision Tree.

✔ Accuracy: 86.44% (Highest Performance)

🏆 CONCLUSION: Best Model Selection
✅ Random Forest is the best-performing model with an accuracy of 86.44%.
✅ It effectively captures complex data patterns and prevents overfitting.
✅ GridSearchCV optimized hyperparameters improved performance.

🚀 Final Recommendation: Use Random Forest for the best accuracy.
