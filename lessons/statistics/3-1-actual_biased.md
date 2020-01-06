[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

``` Python
# Solution goes here
# print(resp.numkdhh)
actual_18pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')

# Actual distribution of children under 18 from responses
'''
hist = thinkstats2.Hist(actual_18pmf, label='number of children')
thinkplot.Hist(hist)
thinkplot.Config(xlabel='# children under 18', ylabel='Count')
'''

# BiasPMF function provided by textbook
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf

biased_18pmf = BiasPmf(actual_18pmf, label='biased')
thinkplot.PrePlot(2)
thinkplot.Pmfs([actual_18pmf, biased_18pmf])
thinkplot.Config(xlabel='# children under 18', ylabel='PMF')

print('Actual mean', actual_18pmf.Mean())
print('Observed mean', biased_18pmf.Mean())

'''
Actual mean 1.024205155043831
Observed mean 2.403679100664282
'''
```


