## Discriptive and inferencial statistics

[Reference image](img/image.png)

## Scales of measurement
* Nominal scales - Gender, colour, relegion
* Ordinal - Customer satisfaction
* Interval - Temperature
* Ratio - Money
    - Has a "true zero" point

## Measures of location

* Mean - Average that describes the center of the frequency description.

* Mode - The number that occurs most frequently.

* Median - Middle number in a list of numbers that has been ordered.

## Measures of variability

* Range
    - Used in conjunction with the Median
    - Largest Value - smallest Value.

* Interquartile Range (IQR)
    - Used in conjunction with the Median
    - Range of the middle 50% of numbers in a distribution
    - 75th percentile - 25th percentile.

* Variance
    - Used in conjunction with the Mean.
    - [Population variance formula](img/image-1.png)
    - [Sample variance formula](img/image-2.png)

* Standard Deviation;
    - Used in conjunction with the Mean.
    - 68% within +/- 1 SD of mean
    - 95% within +/- 2 SD of mean

## Probabilities

Probabilities can be drawn from symmetrical outcomes or in terms of relative frequencies.
* Symmetrical - Coin toss, dice throw. If there are `N` symmetrical outcomes, the probability of any given one of them occurring is taken to be `1/N`.
* Relative frequencies - If we tossed a coin millions of times, we would expect the proportion of tosses that came up heads to be pretty close to 1/2. As the number of tosses increases, the proportion of heads still approaches 1/2. Therefore, we can say that the probability of a head is 1/2.

* In case of **independent events**
    - `P(A and B) = P(A) x P(B)`
    - `P(A or B) = P(A) + P(B) - P(A and B)`

### Discrete & Continuous Distribution
* A discrete distribution means that X can assume one of a countable (usually finite) number of values.
    - Number of children in a household.
    - Binomial, Poisson, and Hypergeometric
* A continuous distribution means that X can assume one of an infinite (uncountable) number of different values.
    - Time to respond to a question.
    - Probabilities of continuous random variables (x) are defined as the area under the curve of its Probability Distribution Function.

#### Descrete probability distribution

##### Binomial
* Fixed number of events, e.g. yes or no, 'success' and 'failure'.
* Events are independent.
* Events can be repeated using identical conditions.

<img width="1680" height="390" alt="image" src="https://github.com/user-attachments/assets/11c98af3-4e1c-4a9d-aaff-b4937ce98d72" />

##### Poisson
The Poisson distribution can be used to calculate the probabilities of various number of "successes" based on the mean number of successes.

* The Poisson distribution can be used to calculate the probabilities of various number of "successes" based on the mean number of successes.
    - Independent Random Events could include calls coming to a Call Centre or cars coming to a roundabout.

    <img width="1680" height="390" alt="image" src="https://github.com/user-attachments/assets/7285b614-36b0-46cd-9d59-f78351d78dd3" />

##### Hypergeometric
The hypergeometric distribution is used to calculate probabilities when sampling without replacement.

<img width="1680" height="444" alt="image" src="https://github.com/user-attachments/assets/0e5ebbbb-5b15-4fae-9f6d-d49f731b5989" />

p is the probability of obtaining k successes. k is the number of "successes" in the population. x is the number of "successes" in the sample. Uppercase N is the size of the population. Lowercase n is the number sampled. kCx is the number of combinations k things taken x at a time.

#### Continuous probability distribution

##### The Uniform Distribution
Sometimes also known as a rectangular distribution, is a distribution that has constant probability or in other words, are evenly distributed over a given interval.

* parts on an assembly line that arrive at the same exact intervals.

##### The Normal Distribution
The most common probability distribution for describing a continuous random variable is the normal probability distribution, with a bell-shaped curve.

* stock returns, rolling dice, flipping a coin or the height of a population.

##### The Exponential Distribution
This is often concerned with the amount of time until some specific event occurs.

* the amount of time, in months a car battery lasts.

