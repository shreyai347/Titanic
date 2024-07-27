# Titanic

Titanic Survivors - Binary Classification

This notebook aims to predict the survival of Titanic passengers using a binary classification model. The key steps include exploring the dataset, preparing the data, training a model, and evaluating its performance.


Dataset Overview:
The dataset contains several columns:
SibSp: Number of siblings and spouses aboard.
Pclass: Ticket class (1st, 2nd, 3rd).
Parch: Number of parents and children aboard.
Fare: Passenger fare.
Cabin: Cabin number.
Embarked: Port of embarkation.

Initial Observations:
The dataset shows that only females survived, leading to a 100% accuracy during initial trials.
Non-numeric columns (Sex, Name, Embarked) need to be converted for model training.
Some columns have null values and require handling.

Data Exploration:
The dataset reveals that all survivors are women, aged between 18 and 50.

Plots indicate:
Only females survived.
A correlation between fewer family members aboard and higher survival chances.
Higher fares correlate with higher survival rates, typically indicating first-class passengers.

Data Preparation:
Fill missing values in Age and Fare columns with median values.
Drop non-essential columns (Name, Cabin, Ticket) for simplicity.
Encode categorical columns (Sex, Embarked) to numeric values.

Data Splitting:
Split the dataset into training and testing sets using an 80-20 ratio.

Model Training:
Use a Random Forest Classifier for training.
Apply cross_val_predict and predict_proba to get predicted probabilities for each class, avoiding data leaks and providing better model evaluation.

Model Evaluation:
Plot the ROC curve to assess model performance, aiming for an area under the curve (AUC) close to 1.

Model Testing:
Evaluate the model on the test set.
The perfect AUC score of 1.0 suggests potential overfitting due to dataset peculiarities (only females surviving).

Key Points:

Data Cleaning: Handle missing values, drop irrelevant columns, and encode categorical variables.

Model Selection: Use Random Forest Classifier due to its robustness and interpretability.

Cross-Validation: Apply cross-validation to ensure the model's performance generalizes well.

ROC Curve: Use the ROC curve and AUC score to evaluate model performance.

Overfitting Concern: A perfect AUC score indicates a potential overfit, especially given the dataset's peculiarity (only female survivors).
