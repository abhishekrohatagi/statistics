
---

### **What kurtosis is**

* **Definition**: A descriptive statistic that measures how much the tails of a distribution contribute compared to the center.
* **Key difference from skewness**: Skewness is about asymmetry; kurtosis is about tail *weight* (and, indirectly, the influence of outliers).
* **Main insight**: For a long time, people thought kurtosis measured “peakedness,” but in reality, it’s about **fat tails** — how extreme values affect the shape.

---

### **Why it matters**

* Two distributions can have:

  * Same mean
  * Same standard deviation
  * Same skewness
    …and still look very different because of tail heaviness.
* **Example**:

  * *Dataset A*: Values evenly spread out (uniform shape) — less in tails.
  * *Dataset B*: Most values bunched in the center, but with a few extreme outliers — fat tails.

---

### **The formula (conceptually)**

* Kurtosis is the **fourth standardized moment**:

$$
\text{kurtosis} = \frac{\frac{1}{n} \sum_{i=1}^n (x_i - \bar{x})^4}{s^4}
$$

* The **power of 4** means extreme values have a *huge* influence (much more than in skewness, which uses power of 3).

---

### **Scales**

1. **Kurtosis** (raw):

   * **Normal distribution** → kurtosis = **3**
   * Less than 3 → tails are lighter than normal (less outlier influence)
   * More than 3 → heavier tails than normal
2. **Excess kurtosis**:

   * Simply $\text{kurtosis} - 3$
   * Normal distribution → 0
   * Positive → heavy tails
   * Negative → light tails
   * **Excel’s `KURT()` function** gives **excess kurtosis**.

---

### **Interpretation example**

* Dataset A: kurtosis 1.8 → excess kurtosis = −1.2 → lighter tails than normal.
* Dataset B: kurtosis 7.5 → excess kurtosis = 4.5 → much heavier tails, big outlier influence.

---

### **Practical use**

* Often used as a **risk measure** in finance.
* High kurtosis means rare events, when they happen, have a **disproportionate impact** on results.
* Example:

  * In a financial return series, one massive price swing could account for most of the kurtosis.
  * Taleb’s work on “fat tails” emphasizes that a single event can dominate outcomes.

---

### **Key takeaway**

* Kurtosis isn’t “how pointy” a distribution is.
* It’s “how much the tails matter” — especially whether extreme values dominate the spread.

---

