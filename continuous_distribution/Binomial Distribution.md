
---

# 📘 Chapter: Modeling Business Success with the Binomial Distribution

## 🎯 Business Context

In business, many events have **binary outcomes** — success or failure, win or lose, yes or no.
Examples:

* A sales executive winning or losing deals
* A startup securing or failing to secure funding rounds
* A marketing email being opened or ignored

To model such outcomes, we use the **Binomial Distribution** — a key tool in data-driven business analytics.

---

## 1️⃣ Theoretical Foundation

### 🔹 Definition

A **Binomial Distribution** models the number of successes in a fixed number of independent trials, each with the same probability of success.

Mathematically:
[
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
]

Where:

* `n` = number of trials (e.g., deals worked on)
* `k` = number of successes (e.g., deals won)
* `p` = probability of success (win rate)
* `1 - p` = probability of failure

### 🔹 Conditions

Binomial distribution applies when:

1. Each trial has **two outcomes** (win/loss)
2. Trials are **independent**
3. Probability of success **remains constant**
4. Number of trials `n` is **fixed**

---

## 2️⃣ Case Study: Amir’s Weekly Sales Performance

### 🧩 Business Scenario

Amir, a sales manager, works on **3 deals per week** and has a **30% win rate** (p = 0.3).
We’ll model and simulate his performance using Python.

---

## 3️⃣ Step-by-Step Python Implementation

### Step 1: Import Libraries & Set Seed

```python
import numpy as np
from scipy.stats import binom

np.random.seed(10)
```

---

### Step 2: Simulate 1 Deal

Simulate a single deal — either **won (1)** or **lost (0)**.

```python
print(binom.rvs(n=1, p=0.3, size=1))
```

✅ Output: `[0]` or `[1]`

---

### Step 3: Simulate a Week (3 Deals)

Simulate 3 independent deals Amir works on in one week:

```python
print(binom.rvs(n=3, p=0.3, size=1))
```

✅ Output Example: `[2]` → Amir won 2 out of 3 deals this week.

---

### Step 4: Simulate a Year (52 Weeks)

Simulate his weekly performance across 52 weeks:

```python
deals = binom.rvs(n=3, p=0.3, size=52)
print(np.mean(deals))
```

✅ Output: `~0.9` → On average, Amir wins **0.9 deals per week**.

---

## 4️⃣ Probability Analysis

### (a) Probability of Winning All 3 Deals

[
P(X = 3)
]

```python
prob_3 = binom.pmf(3, n=3, p=0.3)
print(prob_3)
```

✅ Output: `0.027` → 2.7% chance of winning all 3 deals.

---

### (b) Probability of Winning 1 or Fewer Deals

[
P(X \le 1)
]

```python
prob_less_than_or_equal_1 = binom.cdf(1, n=3, p=0.3)
print(prob_less_than_or_equal_1)
```

✅ Output: `0.784` → 78.4% chance of winning 1 or fewer deals.

---

### (c) Probability of Winning More Than 1 Deal

[
P(X > 1) = 1 - P(X \le 1)
]

```python
prob_greater_than_1 = 1 - prob_less_than_or_equal_1
print(prob_greater_than_1)
```

✅ Output: `0.216` → 21.6% chance of winning 2 or 3 deals.

---

## 5️⃣ Expected Value (Mean Performance)

Expected number of wins per week:
[
E[X] = n \times p
]

```python
expected_wins_per_week = n * p
print(expected_wins_per_week)
```

✅ Output: `0.9` → Amir can expect to win **~1 deal per week** on average.

---

## 6️⃣ Business Interpretation

| Metric             | Meaning                | Business Insight                      |
| ------------------ | ---------------------- | ------------------------------------- |
| `E[X] = 0.9`       | Expected wins per week | Amir can expect ~1 deal each week     |
| `P(X = 3) = 0.027` | Probability of 3 wins  | Only 2.7% chance of perfect week      |
| `P(X ≤ 1) = 0.784` | Probability of ≤1 win  | Most weeks, Amir wins 0–1 deals       |
| `P(X > 1) = 0.216` | Probability of ≥2 wins | 21.6% chance of good performance week |

---

## 7️⃣ Strategic Business Takeaways

1. **Set Realistic Targets:** Based on the data, a target of 1 win per week is reasonable.
2. **Improve Win Rate:** If Amir improves his win rate from 30% → 50%, his expected weekly wins rise from 0.9 → 1.5.
3. **Team Forecasting:** Sales managers can forecast total team performance by scaling up binomial estimates across multiple salespeople.
4. **Performance Risk Modeling:** Use probabilities to predict best- and worst-case sales outcomes.

---

## 🧠 Summary

| Concept                 | Description                                             |
| ----------------------- | ------------------------------------------------------- |
| **Distribution Type**   | Binomial                                                |
| **Used For**            | Modeling number of successes in fixed attempts          |
| **Key Parameters**      | n (trials), p (probability of success)                  |
| **Expected Value**      | n × p                                                   |
| **Example Application** | Sales conversion, marketing success, project completion |

---

