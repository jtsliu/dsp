[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

``` Python
# Solution goes here
import numpy as np
import thinkstats2
import thinkplot

array = np.random.random(1000)
random_pmf = thinkstats2.Pmf(array, label='random_pdf')
random_cdf = thinkstats2.Cdf(array, label='random_cdf')

thinkplot.PrePlot(2)
thinkplot.Cdfs([random_pmf, random_cdf])
thinkplot.Config(xlabel='Numbers', ylabel='PDF/CDF')

# It's easier to tell from the pdf that the distribution is uniform over testing 1000 
# randomized values, since CDF accumulates the values it is a straight diagonal line
```
