

## **Topic**: Descriptive Statistics (Introduction + Mean)

### **1. What is Descriptive Statistics?**

* It’s a part of mathematics that helps us **summarize and describe data**.
* Example: An **average** is a descriptive statistic — it gives a single number to describe a whole dataset.

---

### **2. What You’ll Learn in This Chapter**

We’ll study different descriptive measures:

1. **Mean** (average) – how to calculate, limitations, when to use.
2. **Median** – another type of average.
3. **Mode** – the most common value.
4. **Range & Interquartile Range (IQR)** – measure of spread.
5. **Standard Deviation & Variance** – more advanced spread measures.
6. **Coefficient of Variation** – compares spread relative to the mean.
7. **Skew & Kurtosis** – tells us about shape of data distribution.
8. **Correlation** – measures relationship between two variables.

---

### **3. Mean (Average)**

* **Formula**:

  $$
  \text{Mean} = \frac{\text{Sum of all data points}}{\text{Number of data points}}
  $$
* Example:
  If you have 7 numbers, add them up and divide by 7.
* In **Excel**: Use `=AVERAGE(range)`.

---

### **4. Notation**

* **μ (mu)** = population mean (when you have *all* data).
* **x̄ (x bar)** = sample mean (when you have only a subset of data).
* **N** = population size.
* **n** = sample size.

---

### **5. Population vs. Sample**

* **Population** = the entire group (e.g., all workers in a factory).
* **Sample** = a part of the population (e.g., 7 randomly chosen workers).
* Most times, we only have a **sample**, not the whole population.

---

### **6. Calculating Mean from a Frequency Table**

Sometimes data is summarized like this:

| Age | Frequency |
| --- | --------- |
| 14  | 76        |
| 15  | 121       |

Steps:

1. Multiply each **value** by its **frequency** (`f × x`).
2. Add up these products → **Σ(fx)**.
3. Add up all frequencies → **Σf**.
4. Mean = **Σ(fx) ÷ Σf**.

* **Excel shortcut**: Use `=SUMPRODUCT(values, frequencies) / SUM(frequencies)`.

---

### **7. Estimating the Mean from Grouped Data**

If data is grouped into ranges (e.g., 5–7 kg, 7–8 kg), we **don’t know exact values**.

* Use **midpoints**:

  * For 5–7 → midpoint = 6.
  * For 7–8 → midpoint = 7.5.
* Assume all data in that group is at the midpoint.
* Then, calculate the mean the same way as with frequency tables.

---

### **8. Warning About Grouped Data**

* Midpoint method **assumes data is evenly spread** in the range.
* Sometimes that’s not true.
* Example: Rainfall days (0–2 mm range) → most days might actually be 0 mm, so midpoint 1 mm will overestimate the mean.

---

### **9. Key Takeaways**

* Mean is simple but can be **misleading** if:

  * Data is skewed.
  * Data is grouped with uneven distribution.
* Always think about **context** before using it.





