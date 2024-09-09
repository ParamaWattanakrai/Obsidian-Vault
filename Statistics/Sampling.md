# Formulas

|                                      | Mean                                | Variance                                        | Standard Variation                                   | Standard Variation          |
| ------------------------------------ | ----------------------------------- | ----------------------------------------------- | ---------------------------------------------------- | --------------------------- |
| Population<br>Parameters             | $$\mu=\sum_{i=1}^N\frac{x_i}N$$     | $$\sigma^2=\sum_{i=1}^N\frac{(x_i-\mu)^2}N$$    | $$\sigma^=\sqrt{\sum_{i=1}^N\frac{(x_i-\mu)^2}N}$$   | $$\sigma^=\sqrt{\sigma^2}$$ |
| Sample<br>Statistics<br>(Estimators) | $$\bar{x}=\sum_{i=1}^N\frac{x_i}n$$ | $$S^2=\sum_{i=1}^N\frac{(x_i-\bar{x})^2}{n-1}$$ | $$S=\sqrt{\sum_{i=1}^N\frac{(x_i-\bar{x})^2}{n-1}}$$ | $$S=\sqrt{S^2}$$            |
The difference of the data point and mean is squared to prevent negative errors from cancelling out the positive ones.
The sample's $n-1$ came from [[Bessel's Correction]].

|                     | Mean                                | Median | Frequency                                          |
| ------------------- | ----------------------------------- | ------ | -------------------------------------------------- |
| Estimate $\sigma^2$ | $$\bar{x}=\sum_{i=1}^N\frac{x_i}n$$ |        | $$\sigma^=\sqrt{\sum_{i=1}^N\frac{(x_i-\mu)^2}N}$$ |

---
# Population
Is the total elements within a set.

## Parameters
Parameters are numbers describing a whole population.
$N$ = population size
Population mean formula:
$$
\begin{flalign}
\mu=\sum_{i=1}^N\frac{x_i}N&&
\end{flalign}
$$
Population variance formula:
$$
\begin{flalign}
\sigma^2=\sum_{i=1}^N\frac{(x_i-\mu)^2}N&&
\end{flalign}
$$
Population standard deviation formula:
$$
\begin{flalign}
\sigma^=\sqrt{\sigma^2}=\sqrt{\sum_{i=1}^N\frac{(x_i-\mu)^2}N}&&
\end{flalign}
$$

---
# Sample
Is a selection of a subset of members within a population to estimate the characteristics of the whole population.
## Statistics
Statistics, sometimes called point estimators are numbers describing a sample.
$n$ = sample size

### Estimating $\mu$ (Population mean)
1. Mean ($\bar{x}$)
Sample mean formula:
$$
\begin{flalign}
\bar{x}=\sum_{i=1}^N\frac{x_i}n&&
\end{flalign}
$$
2. Median ($\tilde{x}$)
Median is the value separating the higher half from the lower half of the sample.
3. Mode
Mode is the value that has the most frequency in a sample.

### Estimating $\sigma^2$ (Population variance)
1. Sample Variance ($S^2$)
Sample variance formula:
$$
\begin{flalign}
S^2=\sum_{i=1}^N\frac{(x_i-\bar{x})^2}{n-1}&&
\end{flalign}
$$
2. Coefficient of Variation (CV)
Also known as normalized root-mean-square deviation (NRMSD), percent RMS, and relative standard deviation (RSD)
$$
\begin{flalign}
CV=\frac{S}{\bar{x}}&&
\end{flalign}
$$

### Estimating $\sigma$ (Population SD)
Sample standard deviation formula:
$$
\begin{flalign}
S=\sqrt{S^2}=\sqrt{\sum_{i=1}^N\frac{(x_i-\bar{x})^2}{n-1}}&&
\end{flalign}
$$
---
# Skewness
$$
\begin{flalign}
SK=\frac{3(\bar{x}-\tilde{x})}S&&
\end{flalign}
$$

![[Skewness.png]]

---

#Mathematics/Statistics
#CS30KMITL/Year1/Term1/ProbabilityStatistics