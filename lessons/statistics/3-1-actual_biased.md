[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

~~~python

resp = nsfg.ReadFemResp()

pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

bias_pmf = pmf.Copy(label='biased')

for x, p in pmf.Items():
    bias_pmf.Mult(x,x)

bias_pmf.Normalize()
    
print('Actual mean :', pmf.Mean())
print('Observed mean :', bias_pmf.Mean())

#Plotting the distributions

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, bias_pmf])
thinkplot.Show(xlabel='Number of Children', ylabel='PMF')

~~~
