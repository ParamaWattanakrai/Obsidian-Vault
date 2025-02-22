```python
import pandas as pd
```
# DataFrame
Is a table

## Creating
```python
df = pd.DataFrame({'attribute': [values]}, index=['indexes'])
#Example
df = pd.DataFrame({'Bob': ['I liked it.', 'It was awful.'], 
              'Sue': ['Pretty good.', 'Bland.']},
             index=['Product A', 'Product B'])
```

|           | Bob           | Sue          |
| --------- | ------------- | ------------ |
| Product A | I liked it.   | Pretty good. |
| Product B | It was awful. | Bland.       |
### Reading
```python
df = pd.read_csv('path', index_col=indexcol_idx)
```

```python
df.shape
```

You can view the first samples by
```python
df.head(n_sample) #default is 5
```

## Accessing

```python
#Through names
df.feature
df['attribute'] #Has syntax advantage
#Returns a Series

df.loc['sample', 'attribute']

#Through indexes
df.iloc[sample_idx, attribute_idx]
df[idx] #Not preferred

#loc is very versatile
df.loc[[samples], [attributes]] #data type is not fixed
```

`loc` vs `iloc`
>`iloc` uses the Python stdlib indexing scheme, where the first element of the range is included and the last one excluded. `loc`, meanwhile, indexes inclusively.
>
>This is particularly confusing when the DataFrame index is a simple numerical list, e.g. `0,...,1000`. In this case `df.iloc[0:1000]` will return 1000 entries, while `df.loc[0:1000]` return 1001 of them! To get 1000 elements using `loc`, you will need to go one lower and ask for `df.iloc[0:999]`.
### Conditional Selection
```python
df['attribute'] == value

df.loc[df['attribute'] == value]
df.loc[df['attribute'].isin([values])]
#Could be specified further with boolean algebra

#Example
top_oceania_wines = reviews.loc[(reviews['points'] >= 95) & ((reviews['country'] == 'Australia') | (reviews['country'] == 'New Zealand'))]

df.loc[df['attribute'].notnull()]
```

## Summarizing
```python
df.describe(include=['dtypes'], exclude=['dtypes'])
df['attribute'].mean()
df['attribute'].median()
df['attribute'].unique()
df['attribute'].value_counts()
df['attribute'].idxmax()

#Example
bargain_wine = reviews['title'][(reviews['points'] / reviews['price']).idxmax()]
```

## Mapping

Using `map` and `apply`
```python
df['attribute'].map(lambda value: expression) #expression, usually operations on the value
df.apply(func, axis=axis) #0(default) or ‘index’, 1 or ‘columns’

#Example
def remean_points(row):
    row.points = row.points - review_points_mean
    return row

reviews.apply(remean_points, axis='columns')
```
>`axis=0` (rows): Operate **down** each column.
>`axis=1` (columns): Operate **across** each row.

## Grouping
```python
df.groupby('attribute')['attribute'].describe()
```

Using built in operations (faster)
```python
#Example 1, arithmetical operations
mean = df.mean()
df['attribute'] - mean

#Example 2, string operation
df['attribute'] + ' - ' + df['attribute']
```
## Assigning
```python
df['attribute'] = value #Will assign all, can also use iterable values

#Example
df['index_backwards'] = range(len(df), 0, -1)
```
## Exporting
```python
df.to_csv('filename')
```
# Series
## Creating
```python
df = pd.Series([values], index=['indexes'], name='name')
#Example
pd.Series([30, 35, 40],
		  index=['2015 Sales', '2016 Sales', '2017 Sales'],
		  name='Product A')
```

# Sources
https://pandas.pydata.org/docs/reference/index.html

#DataScience
#ProgrammingLanguages/Python/Libraries