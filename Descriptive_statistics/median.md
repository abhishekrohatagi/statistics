

## **Topic:** Median – An Alternative Average

### **1. What is the Median?**

* **Median** = The **middle value** in an ordered dataset.
* To find it:

  1. Arrange data from smallest to largest.
  2. Find the middle point.

**Example (odd number of items)**:
Data (7 values): 20, 25, 30, **37**, 40, 45, 50

* The 4th value = **37** → Median.

💡 **Shortcut to find position** (odd case):

$$
\text{Median position} = \frac{n + 1}{2}
$$

Where $n$ = number of data points.

---

### **2. Median with an Even Number of Data Points**

* If $n$ is even, there’s no single middle value.
* Take the **mean** of the two central values.

**Example (even number of items)**:
Data (6 values): 28, 30, 32, 37, 42, 45
Middle two values = 32 and 37
Median = $\frac{32 + 37}{2} = 34.5$

Formula still works:

$$
\frac{n + 1}{2} = \frac{6 + 1}{2} = 3.5
$$

Which means halfway between the 3rd and 4th values.

---

### **3. Median in Excel**

```excel
=MEDIAN(range)
```

* Works for both odd and even $n$.
* Example:

  * Odd list → Returns middle value.
  * Even list → Returns average of middle two.

---

### **4. Notation for Median**

* Can be written as:

  * **median**
  * **Med**
  * **M**
  * **m**
  * **Q2** (second quartile — 50% of data below, 50% above).

---

### **5. Estimating Median from Grouped Data**

Sometimes you don’t have raw data, only a **frequency table**.

**Example:**

| Age                     | Frequency |
| ----------------------- | --------- |
| 14                      | 76        |
| 15                      | 121       |
| 16                      | 118       |
| 17                      | 107       |
| 18                      | 54        |
| **Total**: 476 students |           |

Steps:

1. **Find median position**:

$$
\frac{476 + 1}{2} = 238.5
$$

So between the 238th and 239th students.

2. **Locate median group**:

   * 14-year-olds: positions 1–76
   * 15-year-olds: positions 77–197
   * 16-year-olds: positions 198–315
     Median falls in the **16-year-old group**.

3. **Work out how far into the group**:

   * Before group: 197 students.
   * Need to reach 238.5 → 238.5 − 197 = 41.5 students into the group.

4. **Convert to fraction of the group**:

$$
\frac{41.5}{118} \approx 0.35
$$

→ 35% into age 16.

5. **Add to group start value**:

$$
16 + 0.35 = 16.35 \ \text{years}
$$

≈ 16 years 4 months.

This method is called **linear interpolation**.

---

### **6. When Interpolation Can Be Wrong**

* Assumes data is **evenly spread** in the class interval.
* If it’s **bunched** at one end, median estimate can be misleading.

**Example:** Rainfall 0–2 mm

* Many days might be **exactly 0 mm**, not evenly spread up to 2 mm.
* Midpoint-based methods could overestimate actual median.

---

✅ **Key Takeaways:**

* Median is better than mean when data is skewed or has extreme outliers.
* For grouped data, use interpolation — but **only** if even spread is reasonable.
* Always check the **context** before trusting the median estimate.

