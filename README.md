### scipy-statistical-analysis


- Scipy: Scipy is a Python library used for scientific and technical computing, including mathematics, science, and engineering. It provides many useful functions for optimization, signal processing, statistics, and more. The Scipy library is a popular open-source Python library used for scientific and technical computing. It provides modules for optimization, integration, interpolation, linear algebra, statistics, signal and image processing, and much more. The library is built on top of the NumPy library, which provides support for arrays and matrices, and therefore, Scipy is extensively used in data science, machine learning, and scientific research.

- Format Setting: This description is too vague to provide a clear answer, as there are many different contexts in which "format setting" could be used. Without further context, it is difficult to determine what this description is referring to.

- Statistical Analysis: This section of the tutorial aims to illustrate how to use Python to build statistical models and perform data analysis. It covers topics such as estimation, fitting data to probability distributions, and working with discrete and continuous random variables.

- Statistical Data Modeling: This section of the tutorial discusses the limitations of traditional statistical hypothesis testing and introduces a more powerful approach to statistical analysis that involves building flexible models to estimate quantities of interest. The tutorial provides examples of how to use Python to build statistical models from scratch and extract estimates and measures of uncertainty.

- This code describes how to calculate the likelihood function of a Poisson distribution for a given value of lambda, λ, and a set of observed values, y. It then shows how the likelihood function can be used to estimate the unknown value of the parameter λ for a set of observed rainfall data. The likelihood function is defined as the probability of observing the data given the parameter value. In this case, the data are assumed to be drawn from a Poisson distribution with parameter λ=5. 

- The script then shows how the likelihood function can be plotted for different values of λ, and how it differs from the probability distribution function (PDF), which gives the probability of observing a particular value of y for a given λ. 

- The code then goes on to describe how the likelihood function can be used to estimate the values of α and β for a gamma distribution that models rainfall data. It explains how to use the Newton-Raphson algorithm, available through SciPy, to numerically optimize the likelihood function and estimate the values of α and β.

Please find a code:
https://github.com/Harrypatria/scipy-statistical-analysis/blob/main/Scipy%20Statistical%20Analysis.ipynb

While dataset also can be found here:
https://github.com/Harrypatria/scipy-statistical-analysis

The material provided in the given Github link is a Jupyter notebook that demonstrates the usage of Scipy for statistical analysis. It covers various statistical tests like t-test, chi-square test, ANOVA, etc., and their implementation using Scipy. The notebook also explains the interpretation of the test results and provides practical examples to illustrate the concepts.
