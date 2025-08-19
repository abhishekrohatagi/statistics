
---

# 📘 **Random Sampling Techniques**

---

## 🔹 **Sampling Frame**

* **Definition:** A complete *list of all elements* in the population.
* Necessary to perform *true* random sampling.
* Without a sampling frame → cannot use random sampling (e.g., sand grains in Hawaii).

---

## 🔹 **1. Simple Random Sampling (SRS)**

**Method:**

* Number every item in the sampling frame.
* Use random numbers / Excel `RAND()` to select required sample size.
* Every item has an *equal chance* of being selected.

**Pros:**

* No bias in method.
* Quick, easy, and cheap.
* All items equally likely to be included.

**Cons:**

* Requires a sampling frame.
* Does *not guarantee representativeness*, especially with small sample sizes (e.g., gender imbalance possible by chance).

---

## 🔹 **2. Systematic Random Sampling**

**Method:**

1. Know your **population size (N)** and desired **sample size (n)**.
2. Calculate **gap (k)** = N / n.
3. Choose a random **starting point** between 1 and k.
4. Select every *k-th* item thereafter.

**Pros:**

* Quick, easy for large populations.
* Simpler than generating many random numbers.

**Cons:**

* Requires a sampling frame.
* Can introduce bias *if list is ordered non-randomly*.

  * Example: family names → may skip related individuals.

---

## 🔹 **3. Stratified Random Sampling**

**Method:**

* Divide population into *homogeneous groups* (called **strata**) based on a characteristic (e.g., age).
* Ensure sample reflects same proportions as population.
* Use SRS or systematic sampling *within* each stratum.

**Pros:**

* Ensures sample is representative based on chosen characteristic(s), even with small samples.

**Cons:**

* Must know how to classify population into strata.
* Only ensures representativeness *for those chosen characteristics*.
* Still depends on random sampling inside each stratum.

---

## 📌 **Summary Table**

| Method        | Needs Sampling Frame | Good for Representativeness? | Notes           |
| ------------- | -------------------- | ---------------------------- | --------------- |
| Simple Random | ✅ Yes                | ❌ Not guaranteed             | Fully random    |
| Systematic    | ✅ Yes                | ❌ May introduce bias         | Easier than SRS |
| Stratified    | ✅ Yes                | ✅ For chosen characteristics | Requires strata |

---

