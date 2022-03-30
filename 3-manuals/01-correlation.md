---
title: "Correlation"
parent: Manuales
has_children: false
---

# Correlation

## Assumption of Correlations

---

From [StatisticsSolutions](https://www.statisticssolutions.com/correlation-pearson-kendall-spearman/):

***Correlation** is a bivariate analysis that measures the strength of association between two variables and the direction of the relationship.  In terms of the strength of relationship, the value of the correlation coefficient varies between +1 and -1.  A value of ± 1 indicates a perfect degree of association between the two variables.  As the correlation coefficient value goes towards 0, the relationship between the two variables will be weaker.  The direction of the relationship is indicated by the sign of the coefficient; a + sign indicates a positive relationship and a – sign indicates a negative relationship.*

---

The three correlations I deal with are that one is a parametric method, Pearson correlation, and the others are a non-parametric method, Spearman and Kendall rank correlation.

**1. Pearson correlation**

$$
r = \frac{\sum(X - \overline{X})(Y - \overline{Y})}
{\sqrt{\sum(X-\overline{X})^{2}\cdot\sum(Y-\overline{Y})^{2}}}\\
~ \\
\begin{align}
    Where, ~ \overline{X} &= mean ~ of ~ X~variable\\
    \overline{Y} &= mean ~ of ~ Y ~ variable\\
\end{align}
$$

Assumptions:

- Each observation should have a pair of values.

- Each variable should be continuous.

- Each variable should be normally distributed.

- It should be an absence of outliers.

- It assumes linearity and homoscedasticity.

**2. Spearman rank correlation**

$$
\rho = \frac{\sum_{i=1}^{n}(R(x_i) - \overline{R(x)})(R(y_i) - \overline{R(y)})}
{\sqrt{\sum_{i=1}^{n}(R(x_i) - \overline{R(x)})^{2}\cdot\sum_{i=1}^{n}(R(y_i)-\overline{R(y)})^{2}}}
= 1 - \frac{6\sum_{i=1}^{n}(R(x_i) - R(y_i))^{2}}{n(n^{2} - 1)}\\
~ \\
\begin{align}
    Where, ~ R(x_i) &= rank ~ of ~ x_i\\
    R(y_i) &= rank ~ of ~ y_i\\
    \overline{R(x)} &=mean ~ rank ~ of ~ x\\
    \overline{R(y)} &=mean ~ rank ~ of ~ y\\
    n &= number ~ of ~ pairs
\end{align}
$$

Assumptions:

- Pairs of observations are independent.

- Two variables should be measured on an ordinal, interval or ratio scale.

- It assumes that there is a monotonic relationship between the two variables.


**3. Kendall rank correlation**

$$
\tau = \frac{n_c - n_d}{n_c + n_d} = \frac{n_c - n_d}{n(n-1)/2}\\ 
~ \\
\begin{align}
    Where, ~ n_c &= number ~ of ~ concordant ~ pairs\\
    n_d &= number ~ of ~ discordant ~ pairs\\
    n &= number ~ of ~ pairs
\end{align}
$$

Assumptions:

- It's the same as assumptions of Spearman rank correlation.

## Comparison of Each Correlation

**Pearson correlation vs Spearman and Kendall correlations**

- Non-parametric correlations are less powerful because they use less information in their calculations. In the case of Pearson correlation uses information about the mean and deviation from the mean, while non-parametric correlations use only the ordinal information and scores of pairs.

- In the case of non-parametric correlation, it's possible that the X and Y values can be continuous or ordinal, and approximate normal distributions for X and Y are not required. But in the case of Pearson correlation, it assumes the distributions of X and Y should be normal distribution and also be continuous.

- Correlation coefficients only measure linear (Pearson) or monotonic (Spearman and Kendall) relationships.

**Spearman correlation vs Kendall correlation**

- In the normal case, Kendall correlation is more robust and efficient than Spearman correlation. It means that Kendall correlation is preferred when there are small samples or some outliers.

- Kendall correlation has an O(n^2) computation complexity comparing with O(n logn) of Spearman correlation, where n is the sample size.

- Spearman’s rho usually is larger than Kendall’s tau.

- The interpretation of Kendall’s tau in terms of the probabilities of observing the agreeable (concordant) and non-agreeable (discordant) pairs is very direct.


## Correlation in Simulation Data
    
- In the linear relationship, all correlation coefficients are one.

- In the exponential relationship, only two non-parametric correlation coefficients are 1 or -1. In the logarithmic relationship, the results are the same as the exponential relationship.

- In the symmetric U-shaped relationship, all correlation coefficients are zero.


---

### Reference:

Croux, C. and Dehon, C. (2010). Influence functions of the Spearman and Kendall correlation measures. Statistical Methods and Applications, 19, 497-515.

Field, A. (2009). Discovering statistics using SPSS (3rd Edition). London: Sage Publications.

Correlation (Pearson, Kendall, Spearman), Statistics Solutions, <https://www.statisticssolutions.com/correlation-pearson-kendall-spearman/>

Pearson Correlation Assumptions, Statistics Solutions, <https://www.statisticssolutions.com/pearson-correlation-assumptions/>

Kendall’s Tau and Spearman’s Rank Correlation Coefficient, Statistics Solutions, <https://www.statisticssolutions.com/kendalls-tau-and-spearmans-rank-correlation-coefficient/>

Spearman's Rank-Order Correlation using SPSS Statistics, Laed statistics, <https://statistics.laerd.com/spss-tutorials/spearmans-rank-order-correlation-using-spss-statistics.php>

Non-parametric correlation and regression, InfluentialPoints.com, <https://influentialpoints.com/Training/nonparametric_correlation_and_regression-principles-properties-assumptions.htm>

A comparison of the Pearson and Spearman correlation methods, Minitab Express Supprot, <https://support.minitab.com/en-us/minitab-express/1/help-and-how-to/modeling-statistics/regression/supporting-topics/basics/a-comparison-of-the-pearson-and-spearman-correlation-methods/>

Spearman Correlation Coefficient, PeennState Eberly College of Science, <[https://newonlinecourses.science.psu.edu/stat509/node/157/](https://newonlinecourses.science.psu.edu/stat509/node/157/)>


--- 

> NOTA: Este documento es una copia del siguiente [Kaggle kernel by Rooney](https://www.kaggle.com/kiyoung1027/correlation-pearson-spearman-and-kendall/report?scriptVersionId=25999032).