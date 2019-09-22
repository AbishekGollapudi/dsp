[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

~~~python
arr = np.random.random(1000)

pmf = thinkstats2.Pmf(arr)

thinkplot.Pmf(pmf, linewidth=0.1)
thinkplot.Config(xlabel='Random variate', ylabel='PMF')

rand_cdf = thinkstats2.Cdf(arr)
thinkplot.Cdf(rand_cdf)
thinkplot.Show(xlabel='percentile rank', ylabel='CDF')
~~~

![](https://github.com/AbishekGollapudi/dsp/blob/master/img/pmf_ch4.png)
