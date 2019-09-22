[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

~~~python

resp = nsfg.ReadFemResp()

pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

bias_pmf = pmf.Copy(label='biased')

for x, p in pmf.Items():
    bias_pmf.Mult(x,x)

bias_pmf.Normalize()
    
print('Actual mean :', pmf.Mean())   #1.02
print('Observed mean :', bias_pmf.Mean())    #2.40

#Plotting the distributions

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, bias_pmf])
thinkplot.Show(xlabel='Number of Children', ylabel='PMF')

~~~
 
![](https://github.com/AbishekGollapudi/dsp/blob/master/lessons/statistics/tplot.png)

As expected, families with no children have no chance to be in the biased distribution and this is reflected in the plot above. The mean of the biased distribution is over double the mean of the actual distribution and by comparing the two distributions, its easy to see that families with more children are more likely to appear in this sample.
