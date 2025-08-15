
---

## 🔍 **What is Correlation?**

* Until now, we looked at **descriptive statistics for one variable (univariate)** like mean, variance, skewness, etc.
* Now we move to **bivariate data** — where **each observation has two values (X and Y)**.
* **Correlation** tells us how **strongly and in what direction** *two variables move together*.
* It is measured by a number ***R* between -1 and +1**.

| Value of R       | Interpretation                             |
| ---------------- | ------------------------------------------ |
| +1               | Perfect positive linear relationship       |
| Between 0 and +1 | Positive correlation (higher X → higher Y) |
| 0                | No linear relationship                     |
| Between 0 and -1 | Negative correlation (higher X → lower Y)  |
| -1               | Perfect negative linear relationship       |

---

## 📈 **Understanding Correlation Visually**

* Plotting data on a **scatter plot** helps us understand correlation.

  * Points going up diagonally → **Positive correlation**
  * Points going down diagonally → **Negative correlation**
  * No visible pattern → **No correlation**

---

## 🧮 **Formula (Not Important to Memorize!)**

* Formula for correlation involves comparing how far each point is from the mean of X and Y and combining those differences.
* **Outliers (extreme values)** can have a big effect on correlation — they can inflate or deflate R heavily.

---

## ⚠️ **Why Visualizing is Important — Anscombe’s Quartet**

* **Anscombe’s Quartet**: Four very different datasets that **look completely different on scatter plots**, yet all have:

  * Same mean of X and Y
  * Same variance
  * Same correlation (0.82)
  * Same regression line (line of best fit)

👉 Moral: **Don’t rely only on the number (R)** — always **plot your data**.

---

## ❌ **When Correlation is Misleading / Not Appropriate**

Even if R is high (like 0.8+), correlation can still be misleading when:

* Data comes from **multiple different groups/populations**.
* The relationship is **non-linear** (e.g., curved).
* There are **big gaps** or **clusters** in the data instead of a single continuous cloud.

---

## ✅ **When Can You Use Correlation Properly?**

* When the scatter plot looks roughly like an **ellipse (oval-shaped cloud)** — meaning:

  * Data is from a single population
  * Points are spread continuously without gaps
  * Relationship is roughly linear

If that’s true → **Correlation is meaningful**.

---

## 📌 **Conclusion**

* Correlation is a powerful descriptive statistic for relationships between two variables — **but only when used carefully**.
* **Always visualize your data first** before trusting the value of R.
* This wraps up the descriptive statistics chapter — you'll keep using concepts like variance, skew, correlation, etc. throughout the course.

---

