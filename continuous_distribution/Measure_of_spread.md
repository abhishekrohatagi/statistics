
---

## **1. What is Spread?**

Spread tells us **how close or far apart data points are**.

* High spread → data points are far apart
* Low spread → data points are close together

---

## **2. Variance**

* Variance measures the **average squared distance from the mean**.
* Formula (sample variance):

[
s^2 = \frac{\sum (x_i - \bar{x})^2}{n-1}
]

* **Units are squared**, so harder to interpret.
* **Python:**

```python
import numpy as np

sleep_hours = [2, 4, 4, 5, 6, 7, 8, 10, 12.5, 12.5]
variance = np.var(sleep_hours, ddof=1)  # ddof=1 for sample variance
print("Variance:", variance)
```

---

## **3. Standard Deviation (SD)**

* SD = **square root of variance**
* Easier to understand because units are the same as original data.
* **Python:**

```python
std_dev = np.std(sleep_hours, ddof=1)
print("Standard Deviation:", std_dev)
```

---

## **4. Mean Absolute Deviation (MAD)**

* MAD = **average of absolute distances from mean**
* Treats all deviations equally, unlike SD which penalizes larger deviations more.
* **Python:**

```python
mad = np.mean(np.abs(sleep_hours - np.mean(sleep_hours)))
print("Mean Absolute Deviation:", mad)
```

---

## **5. Quantiles / Percentiles**

* **Quantiles** split data into equal parts.
* 50th percentile = median
* Quartiles = 25%, 50%, 75%
* **Python:**

```python
q1 = np.quantile(sleep_hours, 0.25)  # 1st quartile
q2 = np.quantile(sleep_hours, 0.5)   # 2nd quartile (median)
q3 = np.quantile(sleep_hours, 0.75)  # 3rd quartile
print("Q1, Median(Q2), Q3:", q1, q2, q3)
```

---

## **6. Interquartile Range (IQR)**

* IQR = **Q3 - Q1**
* Measures spread of the **middle 50% of data**
* **Python:**

```python
from scipy.stats import iqr

iqr_value = iqr(sleep_hours)
print("Interquartile Range (IQR):", iqr_value)
```

---

## **7. Outliers**

* Outliers are data points **much smaller or larger than others**
* Rule of thumb:

  * Lower threshold = Q1 - 1.5 × IQR
  * Upper threshold = Q3 + 1.5 × IQR
* **Python:**

```python
lower_bound = q1 - 1.5 * iqr_value
upper_bound = q3 + 1.5 * iqr_value

outliers = [x for x in sleep_hours if x < lower_bound or x > upper_bound]
print("Outliers:", outliers)
```

---

## **8. Summary in One Line**

* Pandas `.describe()` gives **count, mean, std, min, Q1, median, Q3, max** all at once:

```python
import pandas as pd

df = pd.DataFrame({'sleep_hours': sleep_hours})
print(df.describe())
```

---

✅ **Python Concepts Covered:**

* Variance, standard deviation, MAD
* Quantiles, quartiles, IQR
* Detecting outliers
* Quick summary with `.describe()`

---


