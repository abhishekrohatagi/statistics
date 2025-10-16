
---

### **1. What Are Measures of Center?**

Measures of center are ways to summarize a dataset by showing a **typical or central value**.
The three main measures are:

* **Mean** (average)
* **Median** (middle value)
* **Mode** (most frequent value)

---

### **2. Understanding Data with Histograms**

* A **histogram** divides data into ranges, called **bins**, and shows how many data points fall into each bin.
* Example: Mammals’ sleep hours:

  * 0–2 hours → 1 mammal
  * 2–4 hours → 9 mammals
* Histograms give a **visual summary**, while measures of center give a **numerical summary**.

---

### **3. Mean (Average)**

* Formula: **Add all values ÷ number of values**
* Example: Total sleep hours of 83 mammals ÷ 83 = 10.43 hours
* **Python:** `np.mean(data)`

**Key point:** Mean is **sensitive to outliers** (extremely high or low values).

---

### **4. Median (Middle Value)**

* The **median** is the middle value when all data is sorted.
* Example: For 83 mammals, the median is the 42nd value → 10.1 hours
* **Python:** `np.median(data)`

**Key point:** Median is **less affected by outliers**.

---

### **5. Mode (Most Frequent Value)**

* The **mode** is the value that occurs **most often**.
* Example: 4 mammals sleep 12.5 hours → 12.5 is the mode
* For categorical data (like diet type), the mode is very useful.
* **Python:** `statistics.mode(data)`

---

### **6. Outliers and Their Impact**

* An **outlier** is an extreme value very different from other data points.
* Example: Adding a mammal that **never sleeps**:

  * **Mean** changes a lot (drops by 3+ hours)
  * **Median** barely changes
* **Takeaway:** Median is **more robust** than mean when outliers exist.

---

### **7. Choosing the Right Measure**

* **Symmetrical data (balanced around center):** Mean works well
* **Skewed data (tail on one side):** Median is better

  * **Left-skewed:** tail on left → mean < median
  * **Right-skewed:** tail on right → mean > median

**Rule of thumb:**

* Use **mean** for normal/symmetrical data
* Use **median** for skewed data or data with outliers

---


