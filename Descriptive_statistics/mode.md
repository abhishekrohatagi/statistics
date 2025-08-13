
## **1. What the Mode Is**

* The **mode** is simply the **most common value** in a dataset.
* Example:

  * Data: `30, 32, 32, 37, 42, 50`
  * **Mode** = `32` (appears twice, others appear once).
* If two numbers tie for most common → **bimodal** dataset.
* If more than two tie → can be **multimodal**.

---

## **2. Why the Mode Can Be Weak**

* In small datasets, the mode can be **arbitrary** and not representative.
* Example: If the most common number appears just twice, that doesn’t necessarily reflect the “average” well.
* The mode is **not always meaningful** for small samples.

---

## **3. When the Mode Is Useful**

The lecture lists **three main situations** where the mode works well:

### **A. For Qualitative (Categorical) Data**

* Example: Favorite colors of people in a survey.
* Mean/median don't make sense here.
* The mode is the **most common category** (e.g., "Blue" is most chosen).

### **B. For Large Datasets with Few Options**

* Example: Number of cars per UK household:

  * 0 cars: 4.3M
  * 1 car: 5.9M → **mode**
  * 2 cars: 2.6M
* With a huge sample, the mode is more meaningful and less random.

### **C. For Frequency Distributions**

* When data is shown as a curve of frequency vs. value:

  * **Mode** = peak of the curve.
  * Example: House prices → most common price point.
  * In **positively skewed distributions** (long tail to the right), we usually see:

    ```
    Mode < Median < Mean
    ```
  * In **negatively skewed distributions** (long tail to the left), we usually see:

    ```
    Mean < Median < Mode
    ```

---

## **4. Relationship Between Mode, Median, and Mean**

* Positive skew (e.g., house prices): `Mode < Median < Mean`
* Negative skew (e.g., life expectancy): `Mean < Median < Mode`
* The lecture ends with a challenge:
  Try to find a dataset where:

  * `Median < Mean < Mode`, or
  * `Mean < Mode < Median`

---

## **5. Summary**

* **Mode** = most frequent value.
* Weak in **small datasets**.
* Useful for:

  * Categories
  * Large datasets with limited choices
  * Identifying peaks in frequency distributions
* Mode behaves differently depending on **data skew**.

