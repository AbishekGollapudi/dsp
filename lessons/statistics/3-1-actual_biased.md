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

Inline-style: 
![alt text](https://github.com/AbishekGollapudi/dsp/blob/master/lessons/statistics/tplot.png "Plots")
