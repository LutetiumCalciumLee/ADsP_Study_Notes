<details>
<summary>ENG (English Version)</summary>  

# ADsP III. Data Analysis

## 1. R Basics

* R is an object-oriented programming language and statistical programming environment.

## 2. R Packages

* Install: `install.packages("package_name")`

* Load: `library(package_name)`

## 3. R Data Structures

### (1) Overview

* Vector, matrix, array, data frame, list

### (2) Vector

* A vector stores values of the same data type.

* Mixing characters and numbers converts the numbers to characters.

### (3) Matrix

* `nrow`: number of rows

* `ncol`: number of columns

* `byrow = TRUE`: fill by rows; default `FALSE` fills by columns

* `cbind()`: combine by columns

* `rbind()`: combine by rows

### (4) Data Frame

* Similar to a matrix, but columns may have different data types.

* Create: `data.frame()`

### (5) List

* Create: `list()`

## 4. Data Mart

### (1) Data Mart

* A small-scale data warehouse designed for a specific department or user group.

### (2) Summary and Derived Variables

* Summary variable: calculated or summarized statistical variable with high reusability.

* Derived variable: created according to conditions or functions; logical validity is required.

## 5. Missing Value Treatment

* Missing values are represented by `NA` in R.

* `is.na()`: checks for missing values

* `na.rm = TRUE`: excludes `NA` from calculations

* `na.omit()`: removes rows containing `NA`

* `complete.cases()`: identifies complete cases

* Methods: complete-case analysis, mean imputation, hot-deck/nearest-neighbor imputation, multiple imputation

## 6. Outlier Treatment

* IQR: $IQR=Q3-Q1$

* Typical range: $Q1-1.5IQR < x < Q3+1.5IQR$

* ESD repeatedly tests extreme observations.

* Mean/SD rule: approximately $\mu-2.5\sigma < x < \mu+2.5\sigma$

* Treatment: removal, replacement, transformation

## 7. Overview of Statistical Analysis

* Population: entire group of interest

* Sample: subset of the population

* Sampling error: error from observing a sample instead of the whole population

* Non-sampling error: error during survey/data collection

* Sampling bias: systematic distortion caused by sampling

## 8. Probability Sampling Methods

* Simple random sampling: equal-probability random selection

* Systematic sampling: select at regular intervals after a random start

* Cluster sampling: randomly select clusters

* Stratified sampling: sample from each stratum

## 9. Levels of Measurement

* Nominal: categories without order

* Ordinal: ordered categories

* Interval: equal intervals, no true zero

* Ratio: equal intervals with a true zero

## 10. Probability

* Sample space $\Omega$: all possible outcomes

* Conditional probability: $P(A|B)=\frac{P(A\cap B)}{P(B)}$

* Independence: $P(A\cap B)=P(A)P(B)$

## 11. Random Variables

### (1) Random Variables

* Discrete examples: binomial, Poisson, geometric, hypergeometric

* Continuous examples: normal, exponential, uniform, t, F, chi-square

### (2) Probability Distributions

#### Poisson Distribution

* Models counts of relatively rare events in a fixed interval or area.

#### Continuous Uniform Distribution

* $X \sim U(a,b)$

* $E(X)=\frac{a+b}{2}$

#### Normal Distribution

* $X \sim N(\mu,\sigma^2)$

#### t-Distribution

* Used especially when population variance is unknown and samples are small.

* $t=\frac{\bar{x}-\mu_0}{s/\sqrt{n}}$

#### Chi-Square Distribution

* Used for goodness-of-fit, independence, and variance inference.

* Variance test: $\chi^2=\frac{(n-1)s^2}{\sigma_0^2}$

* Goodness-of-fit/independence: $\chi^2=\sum\frac{(O_i-E_i)^2}{E_i}$

#### F-Distribution

* Used in ANOVA and regression.

* $F=\frac{V_1}{V_2}$

## 12. Expected Value and Variance

* Discrete: $E(X)=\sum xf(x)$

* Continuous: $E(X)=\int xf(x)\,dx$

* Standard error: $\sigma_{\bar{x}}=\frac{\sigma}{\sqrt{n}}$

## 13. Descriptive and Inferential Statistics

* Descriptive statistics summarize observed data.

* Inferential statistics use samples to infer population characteristics.

* `head()`: first 6 rows

* `tail()`: last 6 rows

* `summary()`: min, Q1, median, mean, Q3, max

## 14. Statistical Data Summary

* Central tendency: mean, median, mode

* Dispersion: variance, standard deviation, IQR, coefficient of variation

* $CV=\frac{s}{\bar{x}}$

* Skewness: asymmetry

* Kurtosis: peakedness/tail heaviness

## 15. Graphical Data Summary

* Histogram: intervals vs. frequency

* Bar chart: categorical data

* Stem-and-leaf plot: preserves individual values

* Scatter plot: relationship between quantitative variables

* Mosaic plot: relationships among categorical variables

## 16. Estimation

* Good estimator criteria: unbiasedness, efficiency, consistency, sufficiency

* Point estimation: single-value estimate

* Large sample/known variance: $\bar{x}-z_{\alpha/2}\frac{\sigma}{\sqrt{n}}\leq\mu\leq\bar{x}+z_{\alpha/2}\frac{\sigma}{\sqrt{n}}$

* Small sample/unknown variance: $\bar{x}-t_{\alpha/2}\frac{s}{\sqrt{n}}\leq\mu\leq\bar{x}+t_{\alpha/2}\frac{s}{\sqrt{n}}$

## 17. Hypothesis Testing

* Procedure: hypotheses → significance level → rejection region → test statistic → decision

* $H_0$: null hypothesis

* $H_1$: alternative hypothesis

* Type I error $\alpha$: reject a true $H_0$

* Type II error $\beta$: fail to reject a false $H_0$

* Power: $1-\beta$

* At $\alpha=0.05$, $p<0.05$ leads to rejection of $H_0$

## 18. Parametric and Nonparametric Tests

* Parametric: assumes a population distribution and uses parameters such as mean/variance.

* Nonparametric: fewer distributional assumptions; often uses ranks or signs.

## 19. Tests for Means

* One-sample t-test: compare one mean with a specified value

* Independent t-test: compare two independent means

* Paired t-test: compare paired measurements

* R `t.test()`: `mu`, `alternative`, `conf.level`, `paired = TRUE`

## 20. Correlation Analysis

* Covariance indicates direction of joint variation.

* Correlation: $-1\leq r\leq1$

* Pearson: linear, parametric correlation

* Spearman: rank-based, nonparametric correlation

## 21. Linear Regression

* Simple: $y=\beta_0+\beta_1x+\epsilon$

* Multiple: $y=\beta_0+\beta_1x_1+\cdots+\beta_kx_k+\epsilon$

* Linear regression: continuous dependent variable

* Logistic regression: categorical dependent variable

* Assumptions: linearity, independence, homoscedasticity, normality

## 22. Regression Coefficient Estimation and Testing

* Coefficients: least squares estimation

* Overall significance: F-test and p-value

* Individual coefficients: coefficient tests and p-values

* $R^2$: proportion of dependent-variable variation explained by the model

* $0\leq R^2\leq1$

* $SST=SSR+SSE$

## 23. Interpretation of Linear Regression

* Simple regression: one explanatory variable

* Multiple regression: multiple explanatory variables

### Regression ANOVA

| Source     |      df | Sum of Squares |   Mean Square |         F |
| ---------- | ------: | -------------: | ------------: | --------: |
| Regression |     $k$ |          $SSR$ |       $SSR/k$ | $MSR/MSE$ |
| Residual   | $n-k-1$ |          $SSE$ | $SSE/(n-k-1)$ |    <br /> |
| Total      |   $n-1$ |          $SST$ |        <br /> |    <br /> |

## 24. Selecting an Optimal Regression Equation

* Multicollinearity: $VIF_i=\frac{1}{1-R_i^2}$

* Larger VIF means stronger multicollinearity; common thresholds are 5 or 10.

* Model selection: smaller AIC/BIC is generally preferred among comparable models.

* Forward selection: add variables

* Backward elimination: remove variables

* Stepwise selection: repeatedly add/remove variables

* Lasso: L1 penalty; coefficients can become exactly 0

* Ridge: L2 penalty; coefficients shrink toward 0

* Elastic Net: combines L1 and L2

## 25. Multidimensional Scaling (MDS)

* Reduces dimensions while preserving distances/similarities.

* Metric MDS: interval/ratio-scale dissimilarities

* Nonmetric MDS: preserves rank order of dissimilarities

## 26. Principal Component Analysis (PCA)

* Converts correlated variables into fewer uncorrelated principal components.

* PC1 explains the greatest variance; later PCs explain remaining variance under orthogonality.

* Covariance matrix preserves original scales.

* Correlation matrix standardizes scale effects.

* Selection: cumulative explained variance, eigenvalue criterion, scree plot

## 27. Overview of Time Series Analysis

* Time series: observations ordered over time.

* Stationarity: mean/variance stable and autocovariance depends on lag.

* Differencing can stabilize mean.

* Log/variance-stabilizing transformations can help unstable variance.

## 28. Time Series Models

* AR($p$): current value depends on $p$ past values.

* $y_t=c+\phi_1y_{t-1}+\cdots+\phi_py_{t-p}+\epsilon_t$

* AR: PACF often cuts off; ACF decays.

* MA($q$): current value depends on current/past errors.

* $y_t=c+\epsilon_t+\theta_1\epsilon_{t-1}+\cdots+\theta_q\epsilon_{t-q}$

* MA: ACF often cuts off; PACF decays.

* ARMA($p,q$): AR + MA

* ARIMA($p,d,q$): AR order, differencing order, MA order

## 29. Time Series Decomposition

* Trend

* Seasonal

* Cyclical

* Irregular

## 30. Data Mining

* Classification: categorical outcomes

* Prediction/regression: continuous outcomes

* Association analysis

* Cluster analysis

* Description

* Process: objective → preparation → processing → modeling → validation

## 31. Supervised and Unsupervised Learning

* Supervised classification: logistic regression, Naive Bayes

* Supervised regression: linear, Lasso, Ridge, Elastic Net

* Both: decision tree, SVM, KNN, neural networks

* Unsupervised clustering: hierarchical, K-Means, K-Medoids, GMM, density-based, SOM

* Association: Apriori, FP-Growth

## 32. Logistic Regression

* Odds: $\frac{p}{1-p}$

* Logit: $\log\left(\frac{p}{1-p}\right)$

* Sigmoid: $p=\frac{1}{1+e^{-z}}$

## 33. Decision Trees

* Classification tree: categorical target

* Regression tree: continuous target

* Structure: root, parent, child, terminal node, split, pruning

* Chi-square: larger observed/expected differences increase $\chi^2$ and reduce p-values.

* Gini: $G=1-\sum p_i^2$

* Entropy: $E=-\sum p_i\log_2(p_i)$

* Regression trees use variance-reduction criteria.

## 34. Ensemble Models

* Bagging: bootstrap samples + aggregation

* Boosting: sequential learning emphasizing previous errors

* Random forest: bagging + random feature selection

* Stacking: base-model predictions feed a meta-model

## 35. Artificial Neural Networks

* Perceptron: basic single-layer neural model

* Multilayer network: hidden layers + backpropagation

* Softmax: $z_i=\frac{e^{x_i}}{\sum_j e^{x_j}}$

* ReLU: $f(x)=\max(0,x)$

* tanh: output between $-1$ and $1$

* Gradient descent minimizes a loss function.

* Vanishing gradients are common with saturating activations; ReLU-family functions can mitigate them.

## 36. Deep Learning

* Characteristics: multilayer structures, automatic feature learning, nonlinear problem solving

* CNN, RNN, LSTM, AE, GAN, reinforcement learning

## 37. Self-Organizing Map (SOM)

* Unsupervised neural-network method for clustering, dimensionality reduction, competitive learning, and visualization.

## 38. K-Nearest Neighbors (KNN)

* Supervised method for classification and regression.

* Lazy learning: most computation occurs when new data arrive.

* Uses nearby observations according to a distance measure.

## 39. Other Classification Methods

* SVM: supervised classification/regression; kernels handle nonlinear boundaries.

* Naive Bayes: based on Bayes' theorem.

* $P(A|B)=\frac{P(B|A)P(A)}{P(B)}$

## 40. Cluster Analysis

* Euclidean: $d(x,y)=\sqrt{\sum_i(x_i-y_i)^2}$

* Manhattan: $d(x,y)=\sum_i|x_i-y_i|$

* Standardized distance adjusts for scale.

* Mahalanobis distance accounts for covariance.

* Minkowski: $d(x,y)=\left(\sum|x_j-y_j|^r\right)^{1/r}$

* Jaccard similarity: $\frac{|A\cap B|}{|A\cup B|}$

* Jaccard distance: $1-J(A,B)$

* Cosine similarity: $\frac{A\cdot B}{\|A\|\|B\|}$

* Cosine distance: $1-$ cosine similarity

## 41. Hierarchical Clustering

* Produces a dendrogram; cluster count need not be fixed in advance.

* Single linkage: minimum distance; chaining can occur

* Complete linkage: maximum distance

* Centroid linkage: centroid distance

* Average linkage: average pairwise distance

* Ward's method: minimizes increase in within-cluster sum of squares

## 42. Non-Hierarchical Clustering

* K-Means: choose $k$ centroids → assign observations → recompute centroids → repeat

* K-Medoids: uses actual observations as centers; more robust to outliers

* Density-based clustering: forms clusters from dense regions; useful for irregular shapes

* Gaussian mixture models: commonly estimated with EM

## 43. Association Analysis

* Support: $P(A\cap B)$

* Confidence: $P(B|A)$

* Lift: $\frac{P(B|A)}{P(B)}$

* Lift $=1$: independence; $>1$: positive association; $<1$: negative association

* Apriori: generates candidate itemsets and removes those below minimum support.

* Sequential analysis: analyzes ordered event patterns.

## 44. Data Partitioning

* Training, validation, test data

* Holdout: separate training/evaluation subsets

* LOOCV: one validation observation, $n-1$ training observations

* k-fold: rotate validation across $k$ folds

* Bootstrap: repeated sampling with replacement

## 45. Model Evaluation

### Classification

| <br />          | Predicted Positive | Predicted Negative |
| --------------- | -----------------: | -----------------: |
| Actual Positive |                 TP |                 FN |
| Actual Negative |                 FP |                 TN |

* Accuracy: $\frac{TP+TN}{TP+TN+FP+FN}$

* Error rate: $\frac{FP+FN}{TP+TN+FP+FN}$

* Recall: $\frac{TP}{TP+FN}$

* Specificity: $\frac{TN}{TN+FP}$

* Precision: $\frac{TP}{TP+FP}$

* F1: $\frac{2\cdot Precision\cdot Recall}{Precision+Recall}$

* ROC x-axis: $1-\text{Specificity}$; y-axis: Recall

* AUC closer to 1 generally means better discrimination.

### Regression

* MSE: $\frac{1}{n}\sum(y_i-\hat{y}_i)^2$

* RMSE: $\sqrt{\frac{1}{n}\sum(y_i-\hat{y}_i)^2}$

* MAE: $\frac{1}{n}\sum|y_i-\hat{y}_i|$

* MAPE: $\frac{100}{n}\sum\left|\frac{y_i-\hat{y}_i}{y_i}\right|$

### Clustering

* Silhouette coefficient

* Dunn index

## 46. Bias and Variance

* Bias and variance have a trade-off.

* High bias + low variance: underfitting

* Low bias + high variance: overfitting

## 47. Overfitting and Underfitting

* Causes of overfitting: excessive complexity, insufficient data, noisy data, excessive training

* Prevention: L1/L2 regularization, dropout, cross-validation, more/better data, appropriate complexity


</details>

<details open>
<summary>KOR (한국어 버전) </summary>

# ADsP - III 과목. 데이터 분석
<img width="1807" height="2528" alt="image" src="https://github.com/user-attachments/assets/9d37009a-72c7-4e45-8a78-53e36120f2b6" />
<img width="1822" height="2545" alt="image" src="https://github.com/user-attachments/assets/e191c2f8-42ea-4f2a-8a3b-f5a01c18d0d1" />
<img width="1778" height="2486" alt="image" src="https://github.com/user-attachments/assets/4ac1d375-ff79-42c7-a026-c679d2193a81" />
<img width="1815" height="2524" alt="image" src="https://github.com/user-attachments/assets/e118f3af-e61c-415c-8186-038e2aa7e801" />
<img width="1771" height="2480" alt="image" src="https://github.com/user-attachments/assets/7771af75-35ab-4c60-91b5-f6000e6ea12b" />
<img width="1912" height="2662" alt="image" src="https://github.com/user-attachments/assets/def4a4cb-a28a-4441-9044-5c9548ac3033" />
<img width="1891" height="2652" alt="image" src="https://github.com/user-attachments/assets/1c570f7e-0974-4608-ada6-748217477ef8" />
<img width="1914" height="2663" alt="image" src="https://github.com/user-attachments/assets/936f9939-09d4-4654-96e6-4f9e17e93beb" />
<img width="1907" height="2672" alt="image" src="https://github.com/user-attachments/assets/e25a4dc3-a99e-4555-a63e-6f8e6b9e1790" />
<img width="1855" height="2586" alt="image" src="https://github.com/user-attachments/assets/b5332961-862b-4196-9f52-68ccf2fb0736" />
<img width="1984" height="2771" alt="image" src="https://github.com/user-attachments/assets/0d9e9f68-8c2f-4470-8fb8-e39963c44f9a" />
<img width="1859" height="2585" alt="image" src="https://github.com/user-attachments/assets/e0558316-0507-4e96-942c-2493b1b315b5" />
<img width="1807" height="2527" alt="image" src="https://github.com/user-attachments/assets/e13560be-d739-4763-9490-d5aea55d14ab" />
<img width="1825" height="2551" alt="image" src="https://github.com/user-attachments/assets/a7ecdf32-7b00-4e16-ba73-be362e90911c" />
<img width="1827" height="2561" alt="image" src="https://github.com/user-attachments/assets/a959872a-5c45-4eea-b4b7-50e1795ba441" />
<img width="1812" height="2532" alt="image" src="https://github.com/user-attachments/assets/a75dcd8e-5cf4-4942-a735-86c0c19b62d1" />
<img width="1804" height="2519" alt="image" src="https://github.com/user-attachments/assets/0eec9538-4a8f-44e7-af50-f8f63965f8e4" />
<img width="1922" height="2665" alt="image" src="https://github.com/user-attachments/assets/b49da931-29bf-4eaa-b6d0-e08276802d81" />


</details>
