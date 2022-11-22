import pandas as pd

from collections import Counter

from imblearn.over_sampling import RandomOverSampler

from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.preprocessing import OneHotEncoder
from sklearn.preprocessing import LabelEncoder

from sklearn.model_selection import train_test_split

from sklearn.feature_selection import SequentialFeatureSelector
from sklearn.feature_selection import RFE

from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier

from sklearn.metrics import confusion_matrix
from sklearn.metrics import accuracy_score
from sklearn.metrics import f1_score

data = pd.read_excel('Dry_Bean_Dataset.xlsx')

X = data.iloc[:, 0:16]
y = data.iloc[:, 16]

o1 = data.iloc[:, 1:3]
o2 = data.iloc[:, 7:16]

#X = pd.concat([o1, o2], axis=1)

# print(X.head())

ros = RandomOverSampler()

X_over, y_over = ros.fit_resample(X, y)

#print(data.head())
#print(data.info())

le = LabelEncoder()
y = le.fit_transform(y)

X_train, X_test, y_train, y_test = train_test_split(X_over, y_over, test_size=0.2, random_state=123)

sc = StandardScaler()

X_train = sc.fit_transform(X_train)
X_test = sc.fit_transform(X_test)

model = RandomForestClassifier()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

fs = RFE(model)
fs.fit(X_train, y_train)

print(fs.get_support())
print(fs.ranking_)

cm = confusion_matrix(y_test, y_pred)
print(cm)

acc = accuracy_score(y_test, y_pred)
print('\n', acc)

f1 = f1_score(y_test, y_pred, average='macro')
print('\n', f1)
