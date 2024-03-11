# Statistical Tests: Are there interactions between environmental factors?

**2024.02.27, 2024.03.05**

## Lecture outline

### Basics 

Random variable: A **value** that follows a probability distribution. Are the following quantities random variables?
- The number of apples in a basket
- Your height
- The height of a person sitting here who I randomly pick up
- Today’s temperature
- The number I get by rolling a die

What is a probability density function (PDF)? How is it different from a probability distribution?

Now let's revisit expectation, variance, and their mathematical expressions (cont. Q2 in Quiz #1): Derive the expectation and the variance of the Bernoulli distribution $Ber(x|p) = p^x(1-p)^{1-x}$.

### Data skills

Here are things we don't primarily focus on during the class but are essential for building up your data skills for reproducible science.

- Programming
- Collaboration and version control (Git & GitHub) (Check out Q4 in Quiz #1)
- Jupyter (incl. Google Colab)
- Data import and wrangling
- Visualization

### More about probability distributions

- Gaussian: many distributions converge to this thanks to the central limit theory
- Poisson distribution (let's check Q5 in worksheet #1)
- Student t-distribution: Bounded to the mean
- Chi-squared ($\chi^2$) distribution: Bounded to the square of the Gaussians

### Hypothesis testing

When to use hypothesis testing?

#### Five general steps
1. Set up $H_0$ (null hypothesis)
2. Set up $H_1$ (alternative hypothesis)
3. Set up test statistic and significance level ($\alpha$)
4. Find the null distribution for the test statistic; calculate the $p$-value
5. Reject or not reject $H_0$ by comparing $p$ with $\alpha$

#### Case study
**One-sample t-test** (Section 4.2.1): Is the mean weight of a fish species from two lakes different? 

We already know this species' population mean ($\mu_0$) in the large lake. And we have a sample mean ($\bar{x}$) from 20 fish in the small lake.

Test statstic $t = \frac{\bar{x} - \mu_0}{s / \sqrt{N}}$

#### Type I vs Type II errors 

aka False positive vs False negative

How do we design $\alpha$ and $N$ while keeping both types of errors in mind?

#### In-depth topics about t-tests

**Two-sample t-test**: Assumption towards the samples matters
- Are both variances the same?
- Are two samples potentially dependent?

T-tests can also test the correlation with the null hypothesis $\rho = 0$.

#### Non-parametric tests

Parametric vs non-parametric tests: which should I use?

Here are tests we may mention during the class lecture:
- Wilcoxon–Mann–Whitney test: Location (mean) difference 
- Kolmogorov–Smirnov test: Goodness of fit for continuous data
- Pearson's chi-squared test: Goodness of fit for categorical data

#### Bootstrapping

How do we do bootstrapping? 

As we have the traditional method (Section 4.4) for estimating the CI, what is the point of using bootstrapping?


<!-- Do you think an inflated die is fair? How to test it?

Histogram and statistical distributions -->

<!-- List at least one random variable in environmental science and remote sensing that fit each statistical distribution:
- Gaussian distribution (aka normal distribution)
- Gamma distribution
- Beta distribution
- Binomial distribution -->

<!-- Suppose Yushan measures 3952.43 m by a satellite altimeter. And the maximum measurement error of this altimeter is 0.2 m according to its documentation. What is the uncertainty of Yushan’s height? What is the 95% confidence interval of Yushan’s height? -->

## Group discussion & demo topics

1. Load an Exercise data set using Jupyter Notebook (hosted by [Google Colaboratory](https://colab.google/), [Callysto Hub](https://www.callysto.ca/), or your local machine)
2. Any questions about the first problem set?