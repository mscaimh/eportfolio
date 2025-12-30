## R-ticulate: A Beginner’s Guide to Data Analysis for Natural Scientists

Bader, Martin. and Leuzinger, Sebastian. (2024) *R-ticulate : a beginner’s guide to data analysis for natural scientists*. John Wiley & Sons, Inc.

[Continous and descrete distributions](img/continuous-and-discrete-distributions.png)

```
      sample mean - assumed population mean
      -------------------------------------
            sample standard deviation
  t =		-------------------------
			         /-----
                    v   n
```
```
                 /-------------
  Variance =    /  p - (1 - p)
               /   -----------
              v         n
```

`fitdistrplus::fitdist()` - `dnorm`, `dpois`, `dgamma`

`> quantile(x = 0:10, probs = 0.5)`

quartiles - 4 parts
deciles - 10 parts
percentiles - 100 parts

`> quantile(x = 0:10, probs = seq(0.01, 0.99, by = 0.01))` - Percentiles calculation

The null hypothesis (H0) assumes no effect, no difference between groups or no relationship between variables.

The alternative hypothesis (HA) assumes an effect, a difference of some sort or a relationship between variables.

## Types of Sampling Methods (4.1)

Simple Learning Pro (2015) *Types of Sampling Methods (4.1)*. Available at: https://www.youtube.com/watch?v=pTuj57uXWlk (Accessed: December 8, 2025).

* Biased samples
  - Convenience sample - only includes people who are easy to reach
	- Voluntary response sample - consists of people that have chosen to include themselves

* Unbiased sample
	- Simple random sampling
	- Stratified random sampling - devide the population into "strata" (group of similar people) and then sample from those strata.
	- Multistage sampling
