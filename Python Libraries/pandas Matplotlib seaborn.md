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
df.Geography.value_counts().plot.bar(grid=True)
df['label'].shape[index]

df['new_label'] = df.label.replace({old: new})
p = df.groupby('label')['label'].agg(HeartDisease=lambda x: np.sum(x == value), Size='size') # not taught
p = df.groupby('label')['label'].agg([lambda x: np.sum(x == value), 'size'])
p.columns = ['labels']
df['target'].replace({1:'Yes', 0:'No'}, inplace=True)
table_df = pd.crosstab(df.rlabel, df.clabel, margins=True)
loc_df = df.loc[df["label"] == value]

np_arr = df.label.values.reshape(nrows,ncols) #(-1,1) -1 means auto
np_arr = df.iloc[rslice, cslice].values
Predict = pd.DataFrame(index=degree).T #Transpose
df = pd.DataFrame(data=list)
df = pd.DataFrame(index=range(num_reps), data={'Pct_To_Target': pct_to_target, 'Sales_Target': sales_target})
df['Sales'] = df['Pct_To_Target'] * df['Sales_Target']
df['Pct_To_Target'].plot(kind='hist', title='Percent to Target Distribution')
df['Commission_Rate'] = df['Pct_To_Target'].apply(calc_commission_rate)
results_df = pd.DataFrame.from_records(all_stats, columns=['Sales', 'Commission_Amount', 'Sales_Target'])
results_df.describe().style.format('{:, .2f}')
```

Importing Matplotlib
```python
import matplotlib.pyplot as plt               # Pyplot interface for plotting
import matplotlib.figure as mfigure           # Figure management
import matplotlib.axes as maxes               # Axes management
import matplotlib.lines as mlines             # Line objects
import matplotlib.patches as mpatches         # Shapes (patches)
import matplotlib.collections as mcollections # Collections of objects
import matplotlib.gridspec as mgridspec       # Flexible subplot arrangement
import matplotlib.animation as animation      # Animation support
import matplotlib.colorbar as mcolorbar       # Color bar management
import matplotlib.cm as cm                    # Colormaps
import matplotlib.ticker as mticker           # Tick formatting and control
import matplotlib.style as mstyle             # Style management
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

plot = sns.scatterplot(x="Trials", y="Pi", s=30, marker="o", data=df)
plot.set(title='Monte Carlo Simulation to Estimate Value of Pi', xlabel="Number of Trials", ylabel="Value of Pi")
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
```