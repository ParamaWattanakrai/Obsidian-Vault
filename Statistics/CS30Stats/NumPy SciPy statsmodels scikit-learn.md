Importing NumPy
```python
import numpy as np
```

Dump NumPy
```python
np_arr = np.array([])

np_arr.shape #(nrow, ncolumn)
reshaped = np_arr.reshape(nrows, ncols) #(-1,1) -1 means auto

np.random.normal(avg, std_dev, num_reps).round(2)
np.random.choice(sales_target_values, num_reps, p=sales_target_prob)
sales_target = np.random.choice(sales_target_values, num_reps, p=sales_target_prob)
pct_to_target = np.random.normal(avg, std_dev, num_reps).round(2)
```

Importing SciPy
```python
import scipy.stats as stats
```

Dump SciPy
```python
stat, p_value = stats.ttest_ind(a=A, b=B, equal_var=boolean)
stat, p_value = stats.ttest_rel(a=A, b=B) #Positionally ordered
chi2, p, dof, expected = stats.chi2_contingency(df, correction=False) #correction for 2x2
```

Importing statsmodels
```python
from statsmodels.stats.proportion import proportions_ztest
```

Dump statsmodels
```python
stat, p_value = proportions_ztest(count=np_counts, nobs=np_samples, alternative='two-sided') #two-sided, smaller, larger
```

Importing scikit-learn
```python
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures
from sklearn.metrics import mean_squared_error, mean_absolute_error

from sklearn.preprocessing import LabelEncoder
from sklearn.naive_bayes import CategoricalNB
```

Dump scikit-learn
```python
#Linear
model = LinearRegression()
model.fit(x, y) #could be np_arr or df
model.intercept_
model.coef_
x_input=[[x1_1, x2_1, x3_1], [x1_2, x2_2, x3_2], [x1_3, x2_3, x3_3]]
model.predict([[x1], [x2], [x3]])
mae = mean_absolute_error(y, y_predict)
mse = mean_squared_error(y, y_predict)
model.score() #R^2
#Polynomial
poly_features = PolynomialFeatures(degree=degree)
x_poly = poly_features.fit_transform(x)
model = LinearRegression()
model.fit(x_poly, y)

#NaiveBayes
df['label_'] = LabelEncoder().fit_transform(data[i])
model = CategoricalNB()
model.fit(X1, y1) #Encode first
model.category_count_
model.feature_log_prob_
model.predict_proba(new_input)
y_le = LabelEncoder() #creates an instance of encoder
y_le.classes_[model.predict()[i]] #decode from an instance of encoder
```

#DataScience
#ProgrammingLanguages/Python/Libraries
#CS30KMITL/Year1/Term1/ProbabilityStatistics