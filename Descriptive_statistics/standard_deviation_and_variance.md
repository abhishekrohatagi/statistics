
---

## **1. Why Standard Deviation Exists**

* We want a **measure of spread** (how spread out the data is).
* **Interquartile Range (IQR)** only looks at the middle 50% of the data.

  * If the quartiles stay the same, IQR stays the same — even if the outer data points move farther apart.
  * Example: Two datasets with the same quartiles but different spreads — IQR fails to show that difference.
* We need a measure that:

  1. Looks at **all data points**.
  2. Reflects **overall spread**.

  * **Standard deviation** does this.

---

## **2. Building Up to Standard Deviation**

Before standard deviation, think of **Mean Absolute Deviation (MAD)**:

1. Find the **mean**.
2. Find the **distance** from each point to the mean (absolute value — ignore +/− signs).
3. Take the **average** of these distances.

Example:

* Mean = 49
* One point = 32 → distance = |49 - 32| = 17
* Repeat for all points, average them → MAD = 10.6
* **Meaning**: On average, data points are 10.6 units away from the mean.

This gives **intuition** for what standard deviation measures, but isn’t the standard method used in statistics.

---

## **3. Standard Deviation (SD) Formula**

Instead of absolute differences, SD:

1. Finds the **difference** from each point to the mean.
2. **Squares** each difference (removes negative signs, and gives more weight to large differences/outliers).
3. Finds the **average squared difference**:

   * Divide by **n** (population formula)
   * Divide by **n−1** (sample formula) → called **Bessel’s correction**.
4. **Square root** the result → brings it back to original units.

**Population SD formula**:

$$
\sigma = \sqrt{\frac{\sum (x_i - \mu)^2}{n}}
$$

**Sample SD formula**:

$$
s = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n-1}}
$$

---

## **4. Why Divide by (n−1) for a Sample**

* Using the **sample mean** (instead of population mean) underestimates spread.
* The sample mean is calculated **from the sample data** → it sits perfectly in the middle, making distances look smaller than they really are.
* Dividing by **n−1** increases the SD slightly to correct this bias.
* This is called the **Bessel correction**.

---

## **5. Example Calculation (Sample SD)**

Data: 32, 49, 44, 52, etc.
Mean = 49

| Data | Difference | Squared |
| ---- | ---------- | ------- |
| 32   | -17        | 289     |
| 49   | 0          | 0       |
| 44   | -5         | 25      |
| 52   | 3          | 9       |
| ...  | ...        | ...     |

* Sum of squares = 1144
* n = 7 → divide by (n−1) = 6 → 1144 ÷ 6 = 190.67
* Square root → **SD = 13.8**

**Interpretation**: Most data points are within ±13.8 units of the mean.

---

## **6. In Excel**

* Sample SD: `=STDEV.S(range)`
* Population SD: `=STDEV.P(range)`
* Almost always use **STDEV.S** unless you have the entire population.

---

## **7. Variance**

* **Variance** = SD²
* Same calculation as SD, but **skip the square root**.
* Units are **squared** (e.g., dollars²) → not intuitive.
* Useful in formulas and theoretical work, but not as interpretable for real-world description.

In Excel:

* Sample variance: `=VAR.S(range)`
* Population variance: `=VAR.P(range)`

---

## **8. Notation**

* Population SD: **σ**
* Sample SD: **s**
* Population variance: **σ²**
* Sample variance: **s²**
* Subscripts indicate data set (e.g., σₓ = SD of dataset X).

---

## **9. Key Takeaways**

* **Standard deviation**: Average distance from the mean, based on **squared** differences.
* **MAD**: Simpler but rarely used in formal stats.
* **n−1 correction**: Avoids underestimating spread for samples.
* **Variance**: Square of SD, useful for calculations but not very intuitive.
* SD is **sensitive to outliers** because squaring large differences makes them dominate the value.

