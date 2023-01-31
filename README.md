<p align="center">
  <a href="https://erdogant.github.io/pca/">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/logo.png" width="600" />
  </a>
</p>

[![Python](https://img.shields.io/pypi/pyversions/distfit)](https://img.shields.io/pypi/pyversions/distfit)
[![Pypi](https://img.shields.io/pypi/v/distfit)](https://pypi.org/project/distfit/)
[![Docs](https://img.shields.io/badge/Sphinx-Docs-Green)](https://erdogant.github.io/distfit/)
[![LOC](https://sloc.xyz/github/erdogant/distfit/?category=code)](https://github.com/erdogant/distfit/)
[![Downloads](https://static.pepy.tech/personalized-badge/distfit?period=month&units=international_system&left_color=grey&right_color=brightgreen&left_text=PyPI%20downloads/month)](https://pepy.tech/project/distfit)
[![Downloads](https://static.pepy.tech/personalized-badge/distfit?period=total&units=international_system&left_color=grey&right_color=brightgreen&left_text=Downloads)](https://pepy.tech/project/distfit)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/erdogant/distfit/blob/master/LICENSE)
[![Forks](https://img.shields.io/github/forks/erdogant/distfit.svg)](https://github.com/erdogant/distfit/network)
[![Issues](https://img.shields.io/github/issues/erdogant/distfit.svg)](https://github.com/erdogant/distfit/issues)
[![Project Status](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![DOI](https://zenodo.org/badge/231843440.svg)](https://zenodo.org/badge/latestdoi/231843440)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg?logo=github%20sponsors)](https://erdogant.github.io/distfit/pages/html/Documentation.html#colab-notebook)
[![Donate](https://img.shields.io/badge/Support%20this%20project-grey.svg?logo=github%20sponsors)](https://erdogant.github.io/distfit/pages/html/Documentation.html#)
<!---[![BuyMeCoffee](https://img.shields.io/badge/buymea-coffee-yellow.svg)](https://www.buymeacoffee.com/erdogant)-->
<!---[![Coffee](https://img.shields.io/badge/coffee-black-grey.svg)](https://erdogant.github.io/donate/?currency=USD&amount=5)-->


``distfit`` is a python package for probability density fitting of univariate distributions for random variables.
With the random variable as an input, distfit can find the best fit for parametric, non-parametric, and discrete distributions.

* For the parametric approach, the distfit library can determine the best fit across 89 theoretical distributions.
  To score the fit, one of the scoring statistics for the good-of-fitness test can be used used, such as RSS/SSE, Wasserstein,
  Kolmogorov-Smirnov (KS), or Energy. After finding the best-fitted theoretical distribution, the loc, scale,
  and arg parameters are returned, such as mean and standard deviation for normal distribution.

* For the non-parametric approach, the distfit library contains two methods, the quantile and percentile method.
  Both methods assume that the data does not follow a specific probability distribution. In the case of the quantile method,
  the quantiles of the data are modeled whereas for the percentile method, the percentiles are modeled.

* In case the dataset contains discrete values, the distift library contains the option for discrete fitting.
  The best fit is then derived using the binomial distribution.

# 
**⭐️ Star this repo if you like it ⭐️**
# 

### [Documentation pages](https://erdogant.github.io/distfit/)

On the [documentation pages](https://erdogant.github.io/distfit/) you can find detailed information about the ``distfit`` library with many examples. 

# 


### Installation

##### Install distfit from PyPI
```bash
pip install distfit
```

##### Install from github source (beta version)
```bash
 install git+https://github.com/erdogant/distfit
```  

##### Check version
```python
import distfit
print(distfit.__version__)
```

##### The following functions are available after installation:

```python
# Import library
from distfit import distfit

dfit = distfit()        # Initialize 
dfit.fit_transform(X)   # Fit distributions on empirical data X
dfit.predict(y)         # Predict the probability of the resonse variables
dfit.plot()             # Plot the best fitted distribution (y is included if prediction is made)
```

<hr>

### Examples

# 

##### [Example: Quick start to find best fit for your input data](https://erdogant.github.io/distfit/pages/html/Examples.html#)

```python

# Prints the screen:
# [distfit] >fit..
# [distfit] >transform..
# [distfit] >[norm      ] [RSS: 0.0133619] [loc=-0.059 scale=2.031] 
# [distfit] >[expon     ] [RSS: 0.3911576] [loc=-6.213 scale=6.154] 
# [distfit] >[pareto    ] [RSS: 0.6755185] [loc=-7.965 scale=1.752] 
# [distfit] >[dweibull  ] [RSS: 0.0183543] [loc=-0.053 scale=1.726] 
# [distfit] >[t         ] [RSS: 0.0133619] [loc=-0.059 scale=2.031] 
# [distfit] >[genextreme] [RSS: 0.0115116] [loc=-0.830 scale=1.964] 
# [distfit] >[gamma     ] [RSS: 0.0111372] [loc=-19.843 scale=0.209] 
# [distfit] >[lognorm   ] [RSS: 0.0111236] [loc=-29.689 scale=29.561] 
# [distfit] >[beta      ] [RSS: 0.0113012] [loc=-12.340 scale=41.781] 
# [distfit] >[uniform   ] [RSS: 0.2481737] [loc=-6.213 scale=12.281] 
```

<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Examples.html#make-predictions">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/fig1.png" width="450" />
  </a>
</p>


# 

##### [Example: Plot summary of the tested distributions](https://erdogant.github.io/distfit/pages/html/Examples.html#plot-rss)

After we have a fitted model, we can make some predictions using the theoretical distributions. 
After making some predictions, we can plot again but now the predictions are automatically included.

<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Examples.html#plot-rss">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/fig1_summary.png" width="450" />
  </a>
</p>

# 

##### [Example: Make predictions using the fitted distribution](https://erdogant.github.io/distfit/pages/html/Examples.html#make-predictions)


<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Examples.html#make-predictions">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/fig1_prediction.png" width="450" />
  </a>
</p>



# 

##### [Example: Test for one specific distributions](https://erdogant.github.io/distfit/pages/html/Examples.html#fit-for-one-specific-distribution)

The full list of distributions is listed here: https://erdogant.github.io/distfit/pages/html/Parametric.html

<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Examples.html#fit-for-one-specific-distribution">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/fig1_prediction.png" width="450" />
  </a>
</p>


# 

##### [Example: Test for multiple distributions](https://erdogant.github.io/distfit/pages/html/Examples.html#fit-for-multiple-distributions)

The full list of distributions is listed here: https://erdogant.github.io/distfit/pages/html/Parametric.html

<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Examples.html#fit-for-multiple-distributions">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/fig1_prediction.png" width="450" />
  </a>
</p>


# 


##### [Example: Fit discrete distribution](https://erdogant.github.io/distfit/pages/html/Discrete.html)


```python
from scipy.stats import binom
# Generate random numbers

# Set parameters for the test-case
n = 8
p = 0.5

# Generate 10000 samples of the distribution of (n, p)
X = binom(n, p).rvs(10000)
print(X)

# [5 1 4 5 5 6 2 4 6 5 4 4 4 7 3 4 4 2 3 3 4 4 5 1 3 2 7 4 5 2 3 4 3 3 2 3 5
#  4 6 7 6 2 4 3 3 5 3 5 3 4 4 4 7 5 4 5 3 4 3 3 4 3 3 6 3 3 5 4 4 2 3 2 5 7
#  5 4 8 3 4 3 5 4 3 5 5 2 5 6 7 4 5 5 5 4 4 3 4 5 6 2...]

# Import distfit
from distfit import distfit

# Initialize for discrete distribution fitting
dfit = distfit(method='discrete')

# Run distfit to and determine whether we can find the parameters from the data.
dfit.fit_transform(X)

# [distfit] >fit..
# [distfit] >transform..
# [distfit] >Fit using binomial distribution..
# [distfit] >[binomial] [SSE: 7.79] [n: 8] [p: 0.499959] [chi^2: 1.11]
# [distfit] >Compute confidence interval [discrete]

```
<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Discrete.html">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/binomial_plot.png" width="450" />
  </a>
</p>

# 

##### [Example: Make predictions on unseen data for discrete distribution](https://erdogant.github.io/distfit/pages/html/Discrete.html#make-predictions)


<p align="left">
  <a href="https://erdogant.github.io/distfit/pages/html/Discrete.html#make-predictions">
  <img src="https://github.com/erdogant/distfit/blob/master/docs/figs/binomial_plot_predict.png" width="450" />
  </a>
</p>


# 


##### [Example: Generate samples based on the fitted distribution](https://erdogant.github.io/distfit/pages/html/Generate.html)

<hr>

### Contributors
Setting up and maintaining distfit has been possible thanks to users and contributors. Thanks:

<p align="left">
  <a href="https://github.com/erdogant/distfit/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=erdogant/distfit" />
  </a>
</p>


### Citation
Please cite ``distfit`` in your publications if this is useful for your research. See column right for citation information.

### Maintainer
* Erdogan Taskesen, github: [erdogant](https://github.com/erdogant)
* Contributions are welcome.
* If you wish to buy me a <a href="https://erdogant.github.io/donate/?currency=USD&amount=5">Coffee</a> for this work, it is very appreciated :)
