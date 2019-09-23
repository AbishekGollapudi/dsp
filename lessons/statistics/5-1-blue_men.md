[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

~~~python
import scipy.stats
mu = 178
sigma = 7.7
male_dist = scipy.stats.norm(loc=mu, scale=sigma)
print(male_dist.cdf(185.4) - male_dist.cdf(177.8))
~~~

Using the code above, I was able to conclude that about 34% of the U.S. male population is in the height range necessary to join Blue Man Group. An alternative to the method used above is to calculate the number of people that are one standard deviation above the mean and subtract the number of people that are at least at the mean height of 178cm. This approach is a little more error prone since I am not using the exact cm values to calculate the CDF but I find it useful to know that males who are one standard deviation above the mean height are the ones eligible to join the group.
