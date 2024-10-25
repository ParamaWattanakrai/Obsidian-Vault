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
print(df) # not taught
df.dtypes
df.describe()
df.mode()
df.groupby('label')['label'].describe()
df.mode(numeric_only = True)
df.describe(exclude=['dtypes'])
df.describe(include=['dtypes'])
df.label = df.label.astype('dtype') #'category'
df.label.value_counts()
df.Geography.value_counts().plot.bar(grid=True)
df['label']
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
plt.show() #not taught
fig = plt.figure(figsize=(w, h))
plt.annotate(label, xy=(x, y), color='color', fontweight='weight', size=17
plt.title('title')
plt.xticks([indexes], ['labels'])
plt.xlabel('xlabel')
plt.ylabel('ylabel')
fig, axarr = plt.subplots(nrows, ncols, figsize=(w, h))
```
Dump seaborn
```python
sns.setstyle('darkgrid')
sns.countplot(x='label', hue='label', data=df, palette=['colors'], ax=axarr[row][col])
sns.boxplot(y='label', x='label', hue='label', data=df)
sns.histplot(df, x="Age")
```