[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

``` Python
print('The mean of the firsts total weight is:', firsts.totalwgt_lb.mean())
print('The mean of the others total weight is:', others.totalwgt_lb.mean())

'''
The mean of the firsts total weight is: 7.201094430437772
The mean of the others total weight is: 7.325855614973262
'''
# It appears that the firstborn child is marginally expected weigh slightly less than the children born afterwards

print('The mean of the firsts pregnancy length is:', firsts.prglngth.mean())
print('The mean of the others pregnancy length is:', others.prglngth.mean())
'''
The mean of the firsts pregnancy length is: 38.60095173351461
The mean of the others pregnancy length is: 38.52291446673706
'''
# The firstborn child is expected to have a slightly longer pregnancy length than the children born after

print('The Cohen\'s effect size for pregnancy length is:', CohenEffectSize(firsts.prglngth, others.prglngth))
print('The Cohen\'s effect size for total weight length is:', CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb))
'''
The Cohen's effect size for pregnancy length is: 0.028879044654449883
The Cohen's effect size for total weight length is: -0.088672927072602
'''
# As expected since the numbers are both marginally smalled in both pregnancy length and total weight, 
# the Cohen's effect size is small. Since the pregnancy length is slightly longer, the Cohen's value is positive, whereas
# because the total weight for the firstborn is smaller, the Cohen's value is negative.
```
