[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

# Chapter 5 Exercise 1
>> See Chap05ex1.ipynb

from __future__ import print_function, division

%matplotlib inline

import numpy as np

import nsfg
import first
import analytic

import thinkstats2
import thinkplot

# Exercise
Exercise: In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.

In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

scipy.stats contains objects that represent analytic distributions

import scipy.stats
How many people are between 5'10" and 6'1"?

# Calculate the difference in cdf between 5'10" and 6'1"
Lower = scipy.stats.norm.cdf(70*2.54, loc = 178, scale = 7.7)

higher = scipy.stats.norm.cdf(73*2.54, loc = 178, scale = 7.7)

prob = higher - Lower

print(prob)
0.34274683763147457
