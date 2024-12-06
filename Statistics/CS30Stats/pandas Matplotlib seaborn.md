Importing pandas
```python
import pandas as pd
```

Creating DataFrame by reading .csv files
```python
df = pd.read_csv(filepath)
```

pandas
```python
print(df) #not taught
df.dtypes
df.describe(include=['dtypes'], exclude=['dtypes']) #count, mean, std, min, quartile, max
df[['labels']].describe()
df.groupby('label')['label'].describe()
df.mode(numeric_only=boolean)
df.label = df.label.astype('dtype') #'category'
df.label.value_counts() #Series
df.label.value_counts().plot.bar(grid=True)
df['label'].plot(kind='hist', title='Percent to Target Distribution')
df['label'].shape[index]

df['new_label'] = df.label.replace({old: new})
p = df.groupby('label')['label'].agg(HeartDisease=lambda x: np.sum(x == value), Size='size') # not taught
p = df.groupby('label')['label'].agg([lambda x: np.sum(x == value), 'size'])
p.columns = ['labels']
df['target'].replace({1:'Yes', 0:'No'}, inplace=True)
table_df = pd.crosstab(df.rlabel, df.clabel, margins=True)
loc_df = df.loc[df["label"] == value]

X = df.drop(['play'], axis=1)
np_arr = df.label.values.reshape(nrows,ncols) #(-1,1) -1 means auto
np_arr = df.iloc[rslice, cslice].values
Predict = pd.DataFrame(index=degree).T #Transpose
df = pd.DataFrame(data=list)
df = pd.DataFrame(index=range(num_reps), data={'Pct_To_Target': pct_to_target, 'Sales_Target': sales_target})
df['new_label'] = df['label'] * df['label']
df['new_label'] = df['label'].apply(function)
results_df = pd.DataFrame.from_records(all_stats, columns=['labels'])
results_df.describe().style.format('{:, .2f}')
```

Importing Matplotlib
```python
import matplotlib.pyplot as plt               # Pyplot interface for plotting
```

Dump Matplotlib
```python
plt.show()
fig = plt.figure(figsize=(w, h))
plt.annotate(label, xy=(x, y), color='color', fontweight='weight', size=17
plt.title('title')
plt.xticks([indexes], ['labels'])
plt.xlabel('xlabel')
plt.ylabel('ylabel')
fig, axarr = plt.subplots(nrows, ncols, figsize=(w, h)) #(fig, nparray)

plt.scatter(x, y, color='color') #df
plt.plot(x, Predict.Degree1,linewidth='3',color='g',linestyle='dotted',label='linear(degree 1)')
plt.ticklabel_format(style='plain') #'sci'/'scientific', 'plain'
plt.legend(loc='best')

plt.axhline(y=3.14, color='r', linestyle='-')
```

Dump seaborn
```python
sns.setstyle('white') #white, dark, whitegrid, darkgrid, ticks
sns.countplot(x='label', hue='label', data=df, palette=['colors'], ax=axarr[row][col])
sns.boxplot(y='label', x='label', hue='label', data=df)
sns.histplot(df, x='label', hue='label', multiple='layer') #layer, dodge, stack

sns.pairplot(df, x_vars=['labels'], y_vars='label', height=h)
sns.countplot(x='Sales_Target', data=df, palette='Set2')

plot = sns.scatterplot(x="Trials", y="Pi", s=30, marker="o", data=df)
plot.set(title='Monte Carlo Simulation to Estimate Value of Pi', xlabel="Number of Trials", ylabel="Value of Pi")
```

#DataScience
#ProgrammingLanguages/Python/Libraries
#CS30KMITL/Year1/Term1/ProbabilityStatistics