🚀 Income Prediction Assistant: Census Income Analysis

📌 Overview
The Income Prediction Assistant is an AI-powered application that predicts whether an individual earns more than $50K per year based on demographic and employment data. This binary classification problem is solved using machine learning models, with Random Forest emerging as the best-performing model.

🎯 Features
✅ Predict Income Bracket: Uses AI models to determine if a person earns <=50K or >50K.
✅ Multiple ML Models: Implements Logistic Regression, Decision Tree, and Random Forest.
✅ Hyperparameter Optimization: Uses GridSearchCV for optimal Random Forest tuning.
✅ Feature Engineering: Label-encodes categorical features for effective model training.
✅ Performance Evaluation: Compares models based on accuracy and generalization ability.

📊 Dataset Structure
📌 Target Variable
<=50K (Encoded as 0)

>50K (Encoded as 1)

🔢 Numerical Features
age: Individual’s age

fnlwgt: Final weight assigned

education-num: Years of education

capital-gain: Capital gain in income

capital-loss: Capital loss in income

hours-per-week: Weekly working hours

🔠 Categorical Features
workclass: Type of employer

education: Education level

marital-status: Marital status

occupation: Job type

relationship: Family role

race: Ethnicity

sex: Gender

native-country: Country of origin

📌 All categorical features were label-encoded before training.

🛠️ Models & Performance
Model	Accuracy
📉 Logistic Regression	82.79%
🌳 Decision Tree	86.00%
🌲 Random Forest	86.44%
📉 Logistic Regression
📌 Description:

Linear classification model using the sigmoid function to estimate probabilities.

Highly interpretable, showing how features impact predictions.

⚠️ Limitations:

Assumes linear relationships, which might not always hold.

Struggles with complex data patterns.

✔ Accuracy: 82.79%

🌳 Decision Tree Classifier
📌 Description:

Splits data into branches based on feature conditions.

Captures non-linear relationships and is easy to interpret.

📌 Optimization:

Tuned max_depth from 1 to 20 to prevent overfitting.

⚠️ Limitations:

Overfits when depth is too large.

Sensitive to small data variations.

✔ Best max_depth: Found via brute-force search.
✔ Accuracy: 86.00%

🌲 Random Forest Classifier (Best Model!)
📌 Description:

An ensemble learning method that builds multiple Decision Trees and averages outputs for better accuracy.

Reduces overfitting and generalizes well.

📌 Hyperparameter Optimization (GridSearchCV):

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
✅ Captures complex data patterns effectively.

⚠️ Limitations:

Computationally expensive for large datasets.

Less interpretable than Decision Trees.

✔ Accuracy: 86.44% (Best Model!)

🏆 Conclusion: Best Model Selection
🔹 🏆 Random Forest is the best model with 86.44% accuracy.
🔹 Effectively captures complex relationships while preventing overfitting.
🔹 Optimized hyperparameters (via GridSearchCV) improve performance.

🚀 Final Recommendation: Use Random Forest for the best accuracy!
