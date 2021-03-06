[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> See Chap04ex2.ipynb

Chapter 4 Exercise 2

from __future__ import print_function, division

%matplotlib inline

import numpy as np

import nsfg
import first
import thinkstats2
import thinkplot

# Exercise: 
The numbers generated by numpy.random.random are supposed to be uniform between 0 and 1; that is, every value in the range should have the same probability.

Generate 1000 numbers from numpy.random.random and plot their PMF. What goes wrong?

Now plot the CDF. Is the distribution uniform?

# Generate 1000 numbers
numbers = np.random.random(1000)

# plot pmf
pmf = thinkstats2.Pmf(numbers, label = 'random numbers')
thinkplot.pmf(pmf,linewidth = .1)
thinkplot.Config(xlabel='numbers',ylabel='pmf')

The distribution is hard to see because there are so many spaces in between and hard to compare.

# plot cdf
cdf = thinkstats2.Cdf(numbers, label = 'random numbers')
thinkplot.Cdf(cdf)
thinkplot.Show(xlabel='numbers',ylabel = 'CDF')

<Figure size 576x432 with 0 Axes>
Since the CDF distribution is approximately a straight line, so the random numbers are uniformly distributed.
