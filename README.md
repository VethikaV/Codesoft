# CREDIT-CARD-FRAUD-DETECTION
import numpy as np
import pandas as pd
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
#loading the data set to the pandas Dataframe
credit_card_data=pd.read_csv('/content/fraudTrain.csv')
#first five rows of the dataset
print(credit_card_data.head())
#last five rows of the dataset
print(credit_card_data.tail())
#Dataset description
print(credit_card_data.describe())
#Dataset information
print(credit_card_data.info())
#checking the number of missing value in each column
print(credit_card_data.isnull().sum())
credit_card_data.dropna(inplace=True)
#checking the number of missing value in each column
credit_card_data.isnull().sum()
X = credit_card_data.drop(columns=['is_fraud'])
y = credit_card_data['is_fraud']
