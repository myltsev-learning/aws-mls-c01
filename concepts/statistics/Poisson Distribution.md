The Poisson distribution <mark style="background: #FFF3A3A6;">is a discrete probability distribution that predicts the likelihood of a certain number of events occurring in a fixed interval of time or space</mark>, given that the events occur with a known average rate and independently of the time since the last event.

![[Pasted image 20240212103550.jpg]]

It is widely used in various fields, including:

- **Finance:** Predicting the number of customer arrivals at a bank or the number of stock trades in a given period.
- **Insurance:** Assessing the risk of claims in a specific category.
- **Healthcare:** Modeling the occurrence of rare diseases or hospital admissions.
- **Biology:** Analyzing the distribution of mutations in a DNA sequence or the number of individuals of a particular species in a given area.

Here are the key characteristics of the Poisson distribution:

- **Discrete:** It deals with countable outcomes, such as the number of events, which can only take on whole number values (0, 1, 2, 3, etc.).
- **Single parameter:** It is characterized by a single parameter, denoted by λ (lambda), which represents the average rate of occurrence of the event within the specified interval.
- **Independent events:** The events are assumed to be independent, meaning that the occurrence of one event does not affect the probability of another event occurring.
- **No fixed time between events:** The time between events is not fixed, but the average rate of occurrence remains constant throughout the interval.

The probability of observing exactly k events within the interval is given by the following formula:

```
P(k) = (e^(-λ) * λ^k) / k!
```

where:

- k is the number of events (0, 1, 2, ...)
- λ is the average rate of occurrence
- e is the base of the natural logarithm (approximately 2.71828)
- k! is the factorial of k (k multiplied by all positive integers less than k)

The Poisson distribution can be visualized as a bell-shaped curve, with the exact shape depending on the value of λ. As λ increases, the curve becomes more spread out, indicating a higher probability of observing a wider range of event counts.

For example:
![[Bard_Chart_Image (1).png]]

This graph shows the probability of the number of guests for different hours of the day. e.g. we see that there is a 80% probability that in 17:00 we will have **1 guest.** (red) Or 13% chance that we will serve 4 guests in 13:00 (yellow)

Here is the code to play with:
```python
import matplotlib.pyplot as plt
import numpy as np

# Define average arrival rates per hour (lambda) based on typical customer patterns
lambda_per_hour = np.array([0.2, 0.5, 1.0, 1.5, 3.0, 2.5, 1.5, 1.0, 0.5, 0.2])

# Create an array of hours (8:00 AM - 5:00 PM)
hours = np.arange(8, 18) * 60  # Convert to minutes for clarity

# Calculate the probability of each number of guests using the Poisson formula
guests_per_hour = np.zeros((len(hours), 24))
for i in range(len(hours)):
    for j in range(24):
        guests_per_hour[i, j] += (np.exp(-lambda_per_hour[i]) * (lambda_per_hour[i]**j)) / np.math.factorial(j)

# Normalize the probabilities for each hour to sum to 1
guests_per_hour /= guests_per_hour.sum(axis=1, keepdims=True)

# Plot the distribution for each hour
colors = ['b', 'g', 'r', 'c', 'm', 'y', 'k', 'b', 'g', 'r']
for i in range(len(hours)):
    plt.plot(np.arange(24), guests_per_hour[i], label="{}:00".format(hours[i] // 60), color=colors[i])

# Customize the plot
plt.xlabel("Number of Guests")
plt.ylabel("Probability")
plt.title("Distribution of Restaurant Guests by Hour (Poisson)")
plt.legend(title="Hour of the Day")
plt.xticks(np.arange(24))  # Ensure x-axis ticks are integers (0-23)
plt.grid(True)
plt.show()

```