## **1. Recap: Averages in Practice**

* **Goal of an average**: to give a **representative value** for a dataset — something that reflects a “typical” case.
* **Example dataset**: House prices.

  * In a small, evenly distributed set, **mean** and **median** are close → either can work.
  * **Mode** in small datasets is often meaningless because it can change arbitrarily if one number changes.

---

## **2. Outliers and Their Effect**

* **Big problem with the mean**: it’s highly affected by outliers.

  * Example: If one house is replaced by a \$1M mansion, the **mean** shoots up but doesn’t reflect the majority of houses.
  * **Median** stays stable because it’s based on the middle value(s) and ignores extremes.
* **Rule of thumb**:

  * **Mean**: Use when data has no extreme outliers.
  * **Median**: Use when data has skew or extreme values.

---

## **3. When Mean & Median Are the Same**

* In **symmetrical distributions**, mean = median = center of distribution.

  * Even with unusual shapes, if it’s symmetrical, both will land in the middle.
  * Example: Normal distribution, or any mirror-symmetrical curve.

---

## **4. Skewed Distributions**

* **Positive skew** (e.g., income):

  * Hard lower bound (0), no upper bound.
  * **Mode** < **Median** < **Mean**.
  * Mean is inflated by high outliers.
  * Example (U.S. incomes at the time of recording):

    * Median: \$34,000 (half earn less, half more)
    * Mean: \$52,000 (inflated by top earners)
* **Negative skew** (e.g., life expectancy):

  * Few low outliers, hard upper bound.
  * Mean < Median < Mode.

---

## **5. When There’s No “Right” Answer**

* **Crime rate example**:

  * Year-to-year data can give different stories depending on which average you use.
  * Sometimes mean goes up, median goes down → no single "true" answer.
  * You must look at **the raw numbers** to really understand changes.
* **Lesson**: Averages can hide the full story — dig into the data.

---

## **6. Key Takeaways**

* Always **check which average** is being used (mean, median, mode).
* Question **whether it’s the most appropriate** for the situation.
* Recognize when averages might **mask important details** (e.g., local variations, subgroups).
* For **skewed or small datasets**, median is often better.
* For **categorical data** or very large datasets with few categories, mode can be meaningful.
* Don’t rely solely on averages — they’re just summaries.

---

## **Self-Check Questions**

1. In your work or studies, when you see “average,” do you know which type it is?
2. Was it the best choice for that dataset?
3. Could the average be hiding an uneven distribution of values?
