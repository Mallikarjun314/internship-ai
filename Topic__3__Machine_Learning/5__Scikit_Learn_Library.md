# Sckit-Learn

1. ### Supervised Learning
   1. Regression
      1. `Linear Regression`
   2. Classification
      1. `Decision Trees`
      2. `Logistic Regression`
      3. `K - Nearest Neighbours`
2. ### Unsupervised Learning
   1. Clustering
      1. `K - Means Clustering`

\
\
\
\
\
\
## Importing Libraries

```python
# ML - Algorithms
from sklearn.linear_model import LogisticRegression # Logistic Regression
from sklearn.linear_model import LinearRegression # Linear Regression
from sklearn.tree import DecisionTreeClassifier # Decision Trees
from sklearn.neighbors import NearestNeighbors # K - Nearest Neighbours
from sklearn.cluster import KMeans # K - Means CLustering
# Pre-Processing
from sklearn.preprocessing import PolynomialFeatures
from sklearn.model_selection import train_test_split
# Pandas
import pandas as pd
```

\
\
\
\
\
\

## Loading and Splitting Dataset
```python

# Loading Dataset
df = pd.read_csv("/.../.../_____.csv")
target_column_name = "..."
df = df.dropna()

# Splitting ----- Features & Target
X = df.drop(target_column_name, axis=1)
Y = df[target_column_name]

X_train, Y_train, X_test, Y_test = train_test_split(X, y)
```
\
\
\
\
\
\
\

## Model Training 
```python
# Model Instantiation
model = LinearRegression()

# Model Training
model.fit(X, y)
```

# Prediction
```python

```