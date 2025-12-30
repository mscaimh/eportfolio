Probabilities can be drawn from symmetrical outcomes or in terms of relative frequencies.
* Symmetrical - Coin toss, dice throw. If there are `N` symmetrical outcomes, the probability of any given one of them occurring is taken to be `1/N`.
* Relative frequencies - If we tossed a coin millions of times, we would expect the proportion of tosses that came up heads to be pretty close to 1/2. As the number of tosses increases, the proportion of heads still approaches 1/2. Therefore, we can say that the probability of a head is 1/2.

* In case of **independent events**
    - `P(A and B) = P(A) x P(B)` - indepednent events
    - `P(A and B) = P(B|A) x P(A)` - dependent events
    - `P(A or B) = P(A) + P(B) - P(A and B)`
    - `P(A|B) = P(A and B) / P(B)`

## Discrete & Continuous Distribution
* A discrete distribution means that X can assume one of a countable (usually finite) number of values.
    - Number of children in a household.
    - Binomial, Poisson, and Hypergeometric
* A continuous distribution means that X can assume one of an infinite (uncountable) number of different values.
    - Time to respond to a question.
    - Probabilities of continuous random variables (x) are defined as the area under the curve of its Probability Distribution Function.

## Descrete probability distribution

### Binomial
* Fixed number of events, e.g. yes or no, 'success' and 'failure'.
* Events are independent.
* Events are repeated using identical conditions (because they are independent, the outcome of one event does not help predict the outcome of the other event).

$P(x) = \frac{N!}{x!(N - x)!} \pi^x (1 - \pi)^{N-x}$

### Poisson
The Poisson distribution can be used to calculate the probabilities of various number of "successes" based on the mean number of successes.

* The Poisson distribution can be used to calculate the probabilities of various number of "successes" based on the mean number of successes.
    - Independent Random Events could include calls coming to a Call Centre or cars coming to a roundabout.

$p = \frac{e^{-\mu} \mu^x}{x!}$

e is the base of natural logarithms (2.7183). $\mu$ is the mean number of "successes", events or occurences. x is the number of "successes", events or occurences in question.

### Hypergeometric
The hypergeometric distribution is used to calculate probabilities when sampling **without replacement**.

$p = \frac{(_kC_x) ( _{(N-k)}C _{(n-x)})}{_NC_n}$

p is the probability of obtaining k successes. k is the number of "successes" in the population. x is the number of "successes" in the sample. Uppercase N is the size of the population. Lowercase n is the number sampled. kCx is the number of combinations k things taken x at a time.

## Continuous probability distribution

### The Uniform Distribution
Sometimes also known as a rectangular distribution, is a distribution that has constant probability or in other words, are evenly distributed over a given interval.

* parts on an assembly line that arrive at the same exact intervals.

### The Normal Distribution
The most common probability distribution for describing a continuous random variable is the normal probability distribution, with a bell-shaped curve.

* stock returns, rolling dice, flipping a coin or the height of a population.

### The Exponential Distribution
This is often concerned with the amount of time until some specific event occurs.

* the amount of time, in months a car battery lasts.
