
---

## **1. What Skewness Is**

* **Skewness** describes the **shape** of your data distribution — specifically, whether it’s symmetrical or lopsided.
* It looks at where the data is *clumped* versus where there are *outliers* (the “tail” of the distribution).

---

## **2. Positive vs Negative Skew**

* **Positive skew**

  * Data is clumped at lower values, with a tail stretching to the higher side.
  * Mean > Median > Mode.
  * Example: ages of people in a young startup — most are in their 20s, but there are a few older founders in their 50s/60s.
* **Negative skew**

  * Data is clumped at higher values, with a tail stretching to the lower side.
  * Mean < Median < Mode.
  * Example: retirement ages — most people retire in their mid-to-late 60s, but a few retire early at 30–40.

---

## **3. Why the Formula Uses Cubes**

* Skew is calculated from the **third standardized moment**.
* That means you take each value’s distance from the mean, **cube** it, and scale it by the standard deviation cubed.
* **Cubing** massively amplifies the effect of outliers:

  * A point 10 units from the mean becomes $10^3 = 1000$ in the formula.
  * So one extreme outlier can dominate the skew value.

---

## **4. How to Interpret the Skew Value**

* **0 (or very close)** → nearly symmetrical.
* **Positive number** → positive skew (tail to the right).
* **Negative number** → negative skew (tail to the left).
* Magnitude matters:

  * |Skew| < \~0.5 → fairly symmetrical.
  * |Skew|  > 3 → suggests big outliers or heavy tail.

---

## **5. Why Skewness Is Useful**

* It helps detect **asymmetry** in the data’s shape.
* Large skew values flag **outliers** that could distort averages and standard deviations.
* Especially handy for large datasets where you can’t just “eyeball” a histogram.

---

## **6. In Excel**

* Use `SKEW(data_range)` for a **sample**.
* Use `SKEW.P(data_range)` if you actually have the **full population** (rare).
* Example:

  * Bitcoin 2021 prices → skew ≈ **0.14** (slightly right-tailed).
  * Ethereum 2021 prices → skew ≈ **0.24** (slightly more right-tailed).

---


