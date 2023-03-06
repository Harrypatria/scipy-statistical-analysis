### scipy-statistical-analysis


Scipy: Scipy is a Python library used for scientific and technical computing, including mathematics, science, and engineering. It provides many useful functions for optimization, signal processing, statistics, and more. The Scipy library is a popular open-source Python library used for scientific and technical computing. It provides modules for optimization, integration, interpolation, linear algebra, statistics, signal and image processing, and much more. The library is built on top of the NumPy library, which provides support for arrays and matrices, and therefore, Scipy is extensively used in data science, machine learning, and scientific research.

There are over 20 distinct data distributions that are utilized to model a wide range of phenomena in both continuous and discrete spaces. These distributions exhibit interconnectivity and can be classified into a family of distributions. To avoid plagiarism, it's important to note that the visualization below is a helpful tool proposed by a blog post, which displays exact relationships (special cases, transformations, or sums) as continuous lines and limit relationships as dashed lines. A detailed explanation of these relationships can be found in the same post, while this paper offers a comprehensive analysis of the interactions between distributions.

Types of common distribution and the relationships: ![Alt Text](https://miro.medium.com/max/1400/1*NhLlwFMzN0yWSvhipqMgfw.jpeg)

In probability theory, probability density function is a continuous approximation of the probability distribution, expressed in terms of integrals of the density of a distribution or a smooth version of histograms. Cumulative distribution function, on the other hand, is a function that gives the probability that a random variable takes on a value less than or equal to a given value. It can be expressed as F(x) = P(X ≤ x), where X is a random variable and x is a value in its domain. For discrete domains, probability mass function (PMF) is used to give the probability that a discrete random variable is exactly equal to some value.

In data science, there are various types of distributions that are commonly used to model different types of phenomena. Each distribution has its own probability distribution/mass function and a typical shape in visualization.

### Discrete distributions

- Bernoulli distribution is a discrete distribution consisting of only one trial with 2 outcomes (success/failure). It constitutes the basis for defining other more complex distributions, which analyze more than one trial, such as the next 3 distributions.

Bernoulli distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1400/1*nf510NwMhfKhjTxC38yWHA.png)

- Binomial distribution computes the probability of k successes within n trials. Like the Bernoulli distribution, trials are independent and have 2 outcomes. Examples of using this distribution are for estimating the number of heads given a series of n coin tosses or how many winning lottery tickets we can expect given the total number of tickets bought. This distribution has 2 parameters, n the total number of trials and p the probability of success:

Binomial distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1290/1*oCZUoAVYp1GFUww3VG8Zpg.png)

- Geometric distribution computes the number of trials before the first success occurs. The number of trials is not fixed, so the probability of success is the same throughout the independent trials, and the experiment continues until the first success. This distribution has one parameter, the probability of success p.

Geometric distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1236/1*FHNknHTX3eYvvsMEyqrzZA.png)

- Hypergeometric distribution measures the number of successes in n trial (similar to binomial) but it doesn’t rely on an assumption of independence between trials. Thus, the trials are performed without replacement, and each trial changes the probability of success. Examples are the probability of drawing a certain combination of cards from a deck without replacement or selecting defective light bulbs from a crate having both defective and working light bulbs. This distribution depends on the number of items in the population (N), the number of trials sampled (n), and the number of items in the population having the successful trait Nx. x represents the number of successful trials.

Hypergeometric distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1314/1*JmnJo-rEEouyeUyWNmEOPw.png)

- Negative binomial computes the number of trials until reaching r successful events. It is a superdistribution of the geometric distribution and can be used to model situations like the number of sales calls to be performed in order to close r deals. The parameters used by this distribution are the probability of success p and the number of required successes r.

Negative binomial: ![Alt Text](https://miro.medium.com/v2/resize:fit:1316/1*0ddVk5UAc2Tpw2UiVxk1kA.png)

- Poisson distribution approximates the number of times an event occurs in a given interval, knowing that the occurrences are independent, there is no upper limit to the the number of events and the average number of occurrences must remain the same if we extended the analysis form one interval to another. This distribution has one parameter, lambda, being the average number of events per interval.

Poisson distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1282/1*-8eqxbJbuN3QbxItN9EMdQ.png)

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


Scipy cheatsheet: ![Alt Text](https://ugoproto.github.io/ugo_py_doc/img/scipy_cs/Python_SciPy_Cheat_Sheet_Linear_Algebra.png)

