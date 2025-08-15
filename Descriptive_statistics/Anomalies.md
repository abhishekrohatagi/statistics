
---

## **1. Why Data Cleaning Matters**

Before analyzing any dataset, it's essential to clean it so your conclusions are meaningful. Cleaning makes sure you're working with relevant, reliable information.

---

## **2. Two Key Parts of Data Cleaning:**

### **A. Detecting & Removing *Anomalies***

* **Anomalies = values that are clearly invalid or recorded incorrectly**
* These don’t match the **type** or **expected format** of your data.
* Examples:

  * Non-numeric entries in a numeric column
  * Impossible values (e.g., negative sales, or zeros that actually represent cancelled transactions)
* **How to detect them:**

  1. Sort data and visually inspect values
  2. Filter invalid types (e.g., text in numeric field)
  3. Look for obvious errors (like 0 or blank values that shouldn’t be there)
* **Action:** Remove or correct after confirming with data owners/stakeholders.

---

### **B. Identifying *Outliers***

* **Outliers = valid data points that lie *far away* from the majority of data**
* They may indicate errors, unusual events, or special cases.
* Important to *detect* them — but decision to *remove* requires context.

---

## **3. Two Common Ways to Define Outliers**

### **1. Using Mean & Standard Deviation (Suitable for symmetric/normal data)**

> A data point is an outlier if it lies **more than 2 standard deviations** away from the mean.

* Formula:

  $$
  |x - \bar{x}| > 2s
  $$
* Compute:

  * Upper cutoff: $\bar{x} + 2s$
  * Lower cutoff: $\bar{x} - 2s$
* Any point outside this range is flagged as an outlier.

---

### **2. Using Quartiles & IQR (Robust for skewed data)**

> A data point is an outlier if it is **1.5× IQR beyond Q1 or Q3**

* Compute:

  * $IQR = Q3 - Q1$
  * Lower bound = $Q1 - 1.5 \times IQR$
  * Upper bound = $Q3 + 1.5 \times IQR$
* Anything below/above these is considered an outlier.

---

## **4. What To Do After Finding Outliers?**

* **Do not automatically delete them.**
* Instead:

  * Investigate reason behind the value
  * Ask: *Error? Rare event? Special circumstance?*
  * Decide whether to:

    * Keep it (if genuine)
    * Remove it (if irrelevant or error)
    * Analyze with & without it (for sensitivity)

---

## **5. Example Insight From Lecture**

| Dataset                        | Outlier?                          | Remove?                                              |
| ------------------------------ | --------------------------------- | ---------------------------------------------------- |
| Shop transactions              | Huge spend (e.g. £500)            | Depends → could be multiple purchases paid together  |
| USA Inflation Rate (2010–2021) | 4.7% in 2021 (beyond both bounds) | Likely **keep**, but flag as special (pandemic year) |

---

## **6. Key Takeaways**

* Cleaning data is crucial before analysis.
* **Anomalies = obviously invalid → remove**
* **Outliers = extreme but valid → investigate**
* Two main detection methods:

  * **Mean ± 2×SD**
  * **Q1/Q3 ± 1.5×IQR**
* Domain understanding is essential for deciding what to keep.

---

