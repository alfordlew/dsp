[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> # # Chapter 3 Excercise 1
>> (note: See included jupyter notebook Chap3_ex1.ipynb)

 
 

from __future__ import print_function, division

get_ipython().run_line_magic('matplotlib', 'inline')

import numpy as np

import nsfg
import first
import thinkstats2
import thinkplot

resp = nsfg.ReadFemResp()

# This prints the mean for actual responses
pmf = thinkstats2.Pmf(resp.numkdhh, label ='actual')
print('mean',pmf.Mean())


# Plot the pmf
thinkplot.pmf(pmf)
thinkplot.Config(xlabel='# of Children',ylabel='pmf')

# Create the BiasPmf Function
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)
    
    for x, p in pmf.Items():
        new_pmf.Mult(x,x)
        
    new_pmf.Normalize()
    return new_pmf


# Print the mean for the Biased Distribution
bias_pmf = BiasPmf(pmf,'Biased')
print('mean',bias_pmf.Mean())

# Plot the biased distribution
thinkplot.pmf(bias_pmf)
thinkplot.Config(xlabel='# of Children', ylabel = 'Biased pmf')

# Plot both distributions
thinkplot.PrePlot(2)
thinkplot.pmfs([pmf, bias_pmf])
thinkplot.Show(xlabel = '# of Children',ylabel = 'pmf')

