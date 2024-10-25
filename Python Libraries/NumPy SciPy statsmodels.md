Importing NumPy
```python
import numpy as np
```

Dump NumPy
```python
array = np.array([])
```

Importing SciPy
```python
import scipy.stats as stats
```

Dump SciPy
```python
stat, p_value = stats.ttest_ind(a=A, b=B, equal_var=boolean)
stat, p_value = stats.ttest_rel(group1, group2)
chi2, p, dof, expected = stats.chi2_contingency(df,correction=False)
```

Importing statsmodels
```python
from statsmodels.stats.proportion import proportions_ztest
```

Dump statsmodels
```python
stat, p_value = proportions_ztest(count=counts, nobs=samples, alternative='two-sided')
```