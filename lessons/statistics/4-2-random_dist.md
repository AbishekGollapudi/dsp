[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

~~~python
arr = np.random.random(1000)

pmf = thinkstats2.Pmf(arr)

thinkplot.Pmf(pmf, linewidth=0.1)
thinkplot.Config(xlabel='Random Value', ylabel='PMF')

rand_cdf = thinkstats2.Cdf(arr)
thinkplot.Cdf(rand_cdf)
thinkplot.Show(xlabel='Percentile Rank', ylabel='CDF')
~~~

![](https://github.com/AbishekGollapudi/dsp/blob/master/img/pmf_ch4.png)

![](https://github.com/AbishekGollapudi/dsp/blob/master/img/cdf_ch4.png)


The CDF is approximately a straight line so this suggests that the distribution is uniform. In addition, looking at the pmf, it is clear that each value in the array of random numbers has a pmf of 0.001 which is to expected given that 1000 random values were generated.
