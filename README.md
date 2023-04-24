### Scipy Statistical Analysis

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

### Continuous distributions
 
- Beta distribution is commonly used to represent variability over a fixed range. For instance, to model the behavior of random variables limited to intervals of finite length. It is also a suitable choice to model percentage or proportions. In Bayesian inference, it is used to model the conjugate prior for Bernoulli, Binomial, Negative binomial and geometric distributions. More simply put, the beta distribution is a good proposal for the priors (the initial knowledge of success) for different applications from the Bernoulli family, such as the number of heads on coin tossing trials or any other dual outcome event. It takes 2 parameters, alpha and beta, and the uncertain variable is a random value between 0 and a positive value. Different combinations of alpha and beta lead to the following shapes of the distribution:

alpha == beta => symmetrical distribution
if (alpha == 1 and beta > 1) or (beta== 1 and alpha> 1) => J shaped distribution
alpha < beta => positive skew
alpha >beta => negative skew

Beta distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1240/1*WhlyL1-jGk5TU28O8_vL9g.png)

- Dirichlet distribution is a multivariate generalization of beta distributions, for which reason it is also known as Multivariate Beta distributions. It is used as prior distribution in Bayesian statistics, where it is the conjugate prior of the categorical and multinomial distribution. It is parameterized by a vector alpha of positive reals, and it samples over a probability simplex. A probability simplex is a set of k numbers adding up to 1 and which correspond to the probabilities of k classes. A k-dimensional Dirichlet distribution has k parameters.

- Cauchy distribution is employed in mechanical and electrical theory, physical anthropology and measurement, and calibration problems. In physics, it describes the distribution of the energy of an unstable state in quantum mechanics under the name Lorentzian distribution. Another application is to model the points of impact of a fixed straight line of particles emitted from a point source or in robustness studies. The Cauchy distribution is known to be a pathological distribution as both its mean and variance are undefined. It takes two parameters. In Bayesian statistics, Cauchy distribution can be used to model the priors for the regression coefficients in logistic regression.

The distribution takes two parameters, the mode m (corresponding to the peak) and the scale gamma (half-width at half maximum of the distribution). Cauchy distribution is the Student’s T distribution with 1 degree of freedom.

Cauchy distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1256/1*_8_AHmtNOhP9yHdsWsgiEw.png)

- Chi-Square distribution is predominantly used in hypothesis testing, in the construction of confidence intervals, in the evaluation of the goodness of fit of an observed distribution to a theoretical one. Chi-Square (with one degree of freedom) variable is the square of a standard normal variable, and Chi-Square distribution has additive property (Sum of two independent Chi-Square distributions is also a Chi-Square variable). The sum of k independent normal distributions is distributed as a chi-square with k degrees of freedom. The chi-square distribution can also be modeled using a gamma distribution with the shape parameter as k/2 and scale as 2S².

The chi-squared distribution has one parameter: k, the number of degrees of freedom.

The chi-squared distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1154/1*GddVH8UqEU6zFAi5RFjJSQ.png)

- Exponential distribution describes the amount of time between events occurring at random moments. It is considered that time has no effect on future outcomes (the future lifetime of an object has the same distribution, regardless of the time it existed) which makes the exponential “memoryless”. It can be used to model situations such as: how long do we have to wait at a crossroads until we see a car running on the red light or how long it will take until someone receives the next phone call? How long will a product function before breaking down?

The exponential distribution is related to Poisson, which doesn’t describe the time lapsed but the number of occurrences of an event in a given time frame. The exponential distribution is parametrized only by lambda, the success rate.

The exponential distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1186/1*WQadkW_17iA_Yl1go9pXCw.png)

- Extreme value distribution, or the Gumbel distribution, models the distribution of the maximum (or the minimum) of a number of samples of various distributions. Examples of this distribution are the breaking strengths of materials, the maximum load for an aircraft, tolerance studies, the maximum level of a river, or of an earthquake in a given year. This distribution has 2 parameters, the mode m corresponding to the most likely point (or the PDF’s highest peak) and a scale parameter, beta, which is > 0 and governs the variance.

Types of distribution: ![Alt Text](https://miro.medium.com/v2/resize:fit:1016/1*hbVgUuwmhNaYA7FXjaLHUA.png)

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


