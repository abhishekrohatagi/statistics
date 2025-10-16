
---

# 📚 **Normal Distribution – Consolidated Notes**

---

## 1. **Theory**

### 🔹 Definition

The **Normal Distribution** is a continuous probability distribution that is **bell-shaped and symmetrical** around its mean.

* **Mean (μ):** Center of the distribution.
* **Standard Deviation (σ):** Spread of the data (how much values deviate from the mean).

---

### 🔹 Key Properties

1. **Symmetry:** Left = Right
2. **Total area under the curve = 1** → represents 100% probability
3. **Tails never touch zero:** Extreme values are possible but rare
4. **68–95–99.7 Rule:**

   * 68% within 1σ of mean
   * 95% within 2σ
   * 99.7% within 3σ
5. **Standard Normal Distribution:** μ = 0, σ = 1

---

### 🔹 Python Functions (`scipy.stats.norm`)

| Function           | Purpose                             |
| ------------------ | ----------------------------------- |
| `cdf(x, μ, σ)`     | Probability X ≤ x                   |
| `1 - cdf(x, μ, σ)` | Probability X > x                   |
| `ppf(p, μ, σ)`     | Value corresponding to percentile p |
| `rvs(μ, σ, n)`     | Generate n random samples           |

---

## 2. **Business Example Context: Amir’s Sales**

* Amir’s current sales: μ = $5000, σ = $2000
* Next quarter predicted market: μ = $6000, σ = $2600
* Key metric: Percent of sales over $1000

---

## 3. **Examples**

### **Example 1: Probability of a sale < $7500**

```python
prob_less_7500 = norm.cdf(7500, loc=5000, scale=2000)
print(prob_less_7500)  # ≈ 0.8944
```

✅ About **89% of sales** are below $7500.

---

### **Example 2: Probability of a sale > $1000**

```python
prob_greater_1000 = 1 - norm.cdf(1000, loc=5000, scale=2000)
print(prob_greater_1000)  # ≈ 0.9772
```

✅ About **97.7% of sales** are above $1000.

---

### **Example 3: Probability of a sale between $3000 and $7000**

```python
prob_between_3000_7000 = norm.cdf(7000, 5000, 2000) - norm.cdf(3000, 5000, 2000)
print(prob_between_3000_7000)  # ≈ 0.6826
```

✅ About **68% of sales** are within one standard deviation.

---

### **Example 4: Sale amount below which 25% of deals fall**

```python
amount_25 = norm.ppf(0.25, loc=5000, scale=2000)
print(amount_25)  # ≈ 3603
```

✅ **25% of deals are below $3603**.

---

### **Example 5: Simulate 36 new sales (after 20% mean increase and 30% SD increase)**

```python
new_mean = 5000 * 1.2   # 6000
new_sd = 2000 * 1.3     # 2600
new_sales = norm.rvs(loc=new_mean, scale=new_sd, size=36)

# Plot histogram
plt.hist(new_sales, bins=10, edgecolor='black')
plt.title('Distribution of New Sales Amounts')
plt.xlabel('Sale Amount')
plt.ylabel('Frequency')
plt.show()
```

✅ Visualizes how **sales spread changes** in predicted market.

---

### **Example 6: Comparing performance metric (sales > $1000)**

```python
# Current market
prob_current = 1 - norm.cdf(1000, 5000, 2000)

# Predicted market
prob_predicted = 1 - norm.cdf(1000, 6000, 2600)

print(prob_current, prob_predicted)  # ≈ 0.9772, 0.9938
```

✅ Amir performs **better in next quarter’s predicted market**.

---

## 4. **Summary Table**

| Metric          | Current Market | Predicted Market |
| --------------- | -------------- | ---------------- |
| Mean (μ)        | 5000           | 6000             |
| SD (σ)          | 2000           | 2600             |
| P(sale > 1000)  | 97.7%          | 99.4%            |
| 25th percentile | 3603           | 3950 (approx)    |

---

