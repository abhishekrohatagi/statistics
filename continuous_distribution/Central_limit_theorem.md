
---

# **Central Limit Theorem (CLT) – Structured Notes**

## **1. Theory**

* The **Central Limit Theorem** states:

> The sampling distribution of a sample statistic (like the mean) approaches a **normal distribution** as the number of random samples increases, **regardless of the shape** of the original population distribution.

* **Key Points:**

  1. Samples must be **random** and **independent**.
  2. Larger sample size or more samples → sampling distribution approaches **normal shape**.
  3. CLT applies to **means, proportions, and other summary statistics**.
  4. Useful when population is **large**, and collecting all data is impractical.

* **Why it matters:**
  Even if the original data is **not normal**, CLT allows us to:

  * Estimate **population mean, standard deviation, or proportion** using **sample data**.
  * Use smaller, random samples to approximate the characteristics of the full population.

---

## **2. Example 1 – Original Distribution**

**Dataset:** `amir_deals['num_users']` – number of users per deal.

```python
# Simple histogram of num_users
amir_deals['num_users'].hist()
plt.show()
```

* Shows the **original distribution** of `num_users`.
* Could be skewed or non-normal.

---

## **3. Example 2 – Single Sample Mean**

**Task:** Take a sample of size 20 and calculate its mean.

```python
np.random.seed(104)
samp_20 = amir_deals['num_users'].sample(20, replace=True)
print(samp_20.mean())
```

* Random sample → one estimate of mean.
* Each sample gives **different mean** due to randomness.

---

## **4. Example 3 – Repeating Samples (100 times)**

**Goal:** See the CLT in action by creating a **sampling distribution of the mean**.

```python
np.random.seed(104)
sample_means = []

for i in range(100):
    samp_20 = amir_deals['num_users'].sample(20, replace=True)
    samp_20_mean = samp_20.mean()
    sample_means.append(samp_20_mean)

# Convert to Series and plot histogram
sample_means_series = pd.Series(sample_means)
sample_means_series.hist()
plt.show()
```

* **Histogram of sample means** starts to look like a **normal distribution**.
* Illustrates **Central Limit Theorem**.

---

## **5. Example 4 – Estimate Company-Wide Mean**

**Scenario:** Too many deals to check all (10,000+).
**Solution:** Take multiple small samples from full company dataset `all_deals`.

```python
np.random.seed(321)
sample_means = []

for i in range(30):
    cur_sample = all_deals['num_users'].sample(20, replace=True)
    cur_mean = cur_sample.mean()
    sample_means.append(cur_mean)

# Estimated company mean
print(np.mean(sample_means))

# Amir's deals mean
print(amir_deals['num_users'].mean())
```

* **Mean of sample means** ≈ estimated company-wide average.
* Compare with Amir’s deals mean to see if they are **above or below average**.

---

## **6. Key Takeaways**

1. The **original distribution** can be any shape.
2. The **sampling distribution of the mean** becomes **normal** with enough samples.
3. CLT allows estimation of population metrics using **smaller samples**.
4. Works for **mean, standard deviation, and proportion**.
5. Essential for **data analysis, hypothesis testing, and confidence intervals**.

---

## **7. Summary Flow (Notebook Diagram)**

```
Population Data (any shape)
       ↓
Take many random samples
       ↓
Calculate mean (or std/proportion) of each sample
       ↓
Plot these values → Sampling Distribution
       ↓
As number of samples ↑ → Sampling Distribution → Normal
```

---


