[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

~~~python
preg = nsfg.ReadFemPreg()

live_babies = preg[preg.outcome == 1]
first_babies = live_babies[live_babies['birthord'] == 1]
others = live_babies[live_babies['birthord'] != 1]

first_avg = first_babies['totalwgt_lb'].mean()
others_avg = others['totalwgt_lb'].mean()

print('Average weight of first babies: ', first_avg)
print('Average weight of others: ', others_avg)
print('Difference in average weight : ', first_avg - others_avg)

cohens_d = thinkstats2.CohenEffectSize(first_babies['totalwgt_lb'], others['totalwgt_lb'])

print('Cohens_D is : ', cohens_d)

~~~

