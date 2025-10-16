
---

## **1. What is a Discrete Probability Distribution?**

* A **probability distribution** shows the probability of each possible outcome.
* **Discrete distributions** deal with **countable outcomes** (like dice rolls, number of sales).
* Example: Rolling a fair 6-sided die → outcomes: 1, 2, 3, 4, 5, 6

  * Probability for each = 1/6 ≈ 0.17

---

## **2. Expected Value**

* The **expected value** (mean) of a distribution = weighted average of all outcomes:

[
E[X] = \sum (\text{value} \times \text{probability})
]

* For a fair die:
  [
  E[X] = 1*(1/6) + 2*(1/6) + 3*(1/6) + 4*(1/6) + 5*(1/6) + 6*(1/6) = 3.5
  ]

---

## **3. Uneven (Biased) Die**

* If probabilities aren’t equal, expected value changes.
* Example: A die where 2 is replaced by another 3 → probability of 2 = 0, probability of 3 = 1/3

---

## **4. Calculating Probabilities**

* The **probability of an event** is the **sum of the probabilities of outcomes** in that event.
* Example: Probability of rolling ≤ 2 on a fair die = P(1) + P(2) = 1/6 + 1/6 = 1/3

---

## **5. Sampling from Discrete Distributions**

* We can **simulate rolls** by sampling from a DataFrame or list.

* **With replacement** → independent events (like real dice rolls)

* **Without replacement** → each pick affects the next

* **Law of Large Numbers:** As the number of rolls increases, the **sample mean approaches the theoretical mean**.

---

## **6. Python Examples**

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Create a fair die DataFrame
die = pd.DataFrame({
    'value': [1,2,3,4,5,6],
    'prob': [1/6]*6
})

# Expected value
expected_value = (die['value'] * die['prob']).sum()
print("Expected value of fair die:", expected_value)

# Simulate 10 rolls (with replacement)
sample_10 = die.sample(n=10, replace=True, weights='prob')
print("10 simulated rolls:\n", sample_10)

# Histogram of outcomes
plt.hist(sample_10['value'], bins=np.linspace(0.5,6.5,7), edgecolor='black')
plt.title("Simulated 10 Rolls of a Fair Die")
plt.xlabel("Die Value")
plt.ylabel("Frequency")
plt.show()

# Simulate 1000 rolls to see Law of Large Numbers
sample_1000 = die.sample(n=1000, replace=True, weights='prob')
print("Sample mean of 1000 rolls:", sample_1000['value'].mean())

plt.hist(sample_1000['value'], bins=np.linspace(0.5,6.5,7), edgecolor='black')
plt.title("Simulated 1000 Rolls of a Fair Die")
plt.xlabel("Die Value")
plt.ylabel("Frequency")
plt.show()
```

---

### **7. Key Takeaways**

* Discrete distributions = countable outcomes
* Expected value = mean of the distribution
* Probabilities can be visualized as bar plots
* **Larger sample → closer to theoretical probabilities** (Law of Large Numbers)

---


