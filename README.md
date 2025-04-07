# Expresso Churn Prediction - ML Prediction App.
## 🎯 What You're Aiming For.
This project demonstrates how to predict which clients are most likely to churn using the 'Expresso churn' dataset provided as part of the Expresso Churn Prediction Challenge hosted by Zindi platform.

## ➡️ Dataset Link.
Dataset Link

## ➡️ Columns Explanation.
Columns Explanation Link

# ℹ️ Instructions.
Install the necessary packages:
Import your data and perform basic data exploration:
Display general information about the dataset:
Create a pandas profiling report to gain insights into the dataset:
Handle missing and corrupted values:
Remove duplicates, if they exist:
Handle outliers, if they exist:
Encode categorical features:
Based on the previous data exploration, train and test a machine learning classifier:
Create a Streamlit application (locally) and add input fields for your features and a validation button at the end of the form:
Deploy your application on Streamlit share:
Create a GitHub and a Streamlit Share account.
Create a new git repository.
Upload your local code to the newly created git repository.
Log in to your Streamlit account and deploy your application from the git repository.
🛠️ Tools Used.
Anaconda
Jupyter Nootbook.
Python.
VSCode.
GitHub.
Google Chrome.
Streamlit.
Example Code.
```python
pip install pandas scikit-learn streamlit
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.preprocessing import LabelEncoder

data = pd.read_csv('path_to_your_dataset.csv')
print(data.head())
print(data.info())
le = LabelEncoder()
data['encoded_column'] = le.fit_transform(data['categorical_column'])
features = data.drop('target_column', axis=1)
label = data['target_column']
x_train, x_test, y_train, y_test = train_test_split(features, label, test_size=0.2, random_state=42)
model = RandomForestClassifier()
model.fit(X_train, y_train)
