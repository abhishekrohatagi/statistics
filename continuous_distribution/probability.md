
---

## **1. What is Probability?**

* Probability measures the **chance of an event happening**.
* Formula:

[
P(\text{event}) = \frac{\text{Number of ways event can happen}}{\text{Total possible outcomes}}
]

* Examples:

  * Coin flip → P(Heads) = 1/2 = 50%
  * Impossible event → P = 0
  * Certain event → P = 1 (100%)

---

## **2. Random Selection / Sampling**

* Example: Pick a salesperson for a client meeting:

  * 4 salespeople → probability of picking Brian = 1/4 = 25%

* **Python example:**

```python
import pandas as pd
import numpy as np

# Sample sales team
sales_team = pd.DataFrame({'name': ['Brian', 'Claire', 'David', 'Emma']})

# Randomly pick one
picked = sales_team.sample()
print(picked)
```

---

## **3. Setting a Random Seed**

* To get **reproducible results**, use a random seed.

```python
np.random.seed(42)
picked = sales_team.sample()
print(picked)
```

> Running this multiple times gives the **same person** every time.

---

## **4. Sampling Without Replacement**

* Once someone is picked, they **cannot be picked again**.

* Example: Two meetings at the same time → pick 2 people from 4:

  * Probability for 2nd person depends on who was picked first.

* **Python example:**

```python
picked_two = sales_team.sample(n=2, replace=False)
print(picked_two)
```

---

## **5. Sampling With Replacement**

* If events happen at **different times**, the same person **can be picked again**.

* Probability stays the same each time → independent events.

* **Python example:**

```python
picked_two_replace = sales_team.sample(n=2, replace=True)
print(picked_two_replace)
```

---

## **6. Independent vs Dependent Events**

* **Independent events:** Outcome of first event **doesn’t affect** the second.

  * Example: Sampling **with replacement**.

* **Dependent events:** Outcome of first event **affects** the probability of the second.

  * Example: Sampling **without replacement**.

---

## ✅ **Python Summary**

```python
# Set random seed
np.random.seed(101)

# Sampling one person
one_pick = sales_team.sample()
print("Pick 1:\n", one_pick)

# Sampling 2 people without replacement (dependent)
two_pick = sales_team.sample(n=2, replace=False)
print("Pick 2 without replacement:\n", two_pick)

# Sampling 2 people with replacement (independent)
two_pick_replace = sales_team.sample(n=2, replace=True)
print("Pick 2 with replacement:\n", two_pick_replace)
```

---

