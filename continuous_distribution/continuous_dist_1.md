
---

### **1. Continuous vs. Discrete**

* **Discrete variables**: You can count them (like number of people, dice rolls).
* **Continuous variables**: They can take **any value** in a range (like waiting time, height, weight).
* Example: You can’t list every possible waiting time for a bus (1 min, 1.5 min, 1.53 min… infinite possibilities).

---

### **2. Waiting for the Bus Example**

* Bus comes **every 12 minutes**.
* If you arrive randomly, your waiting time can be **anywhere from 0 to 12 minutes**.

---

### **3. Continuous Uniform Distribution**

* Since any waiting time is equally likely, we represent this as a **flat line**.
* This is called a **continuous uniform distribution**.
* Graphically: The line is flat between 0 and 12 minutes.

---

### **4. Probability = Area**

* For continuous distributions, probability is measured as the **area under the line**.
* Example: Probability of waiting **between 4 and 7 minutes**:

  * Width = 7 − 4 = 3
  * Height = 1/12 (since total area must be 1)
  * Area = 3 × 1/12 = **0.25 or 25%**

---

### **5. Using Python**

* You can calculate probabilities with **SciPy**:

  ```python
  from scipy.stats import uniform

  # Probability of waiting ≤ 7 minutes
  prob = uniform.cdf(7, loc=0, scale=12)
  print(prob)  # ~0.583 or 58%
  ```
* **Waiting more than 7 minutes**: `1 - 0.583 ≈ 0.417 or 41%`
* **Probability of waiting 4–7 minutes**:

  ```python
  prob_4_7 = uniform.cdf(7, 0, 12) - uniform.cdf(4, 0, 12)
  print(prob_4_7)  # 0.25 or 25%
  ```

---

### **6. Total Probability**

* Probability of waiting **0–12 minutes** = 1 (100%). Makes sense because it **must** fall in that range.

---

### **7. Generating Random Numbers**

* To simulate waiting times according to the uniform distribution:

  ```python
  random_times = uniform.rvs(0, 5, size=10)  # 10 random values between 0 and 5
  print(random_times)
  ```

---

### **8. Other Continuous Distributions**

* Not all continuous distributions are flat like uniform.
* Example:

  * **Normal distribution**: Values around a mean are more likely.
  * **Exponential distribution**: Models waiting times for events.
* Rule: **Area under the curve = 1**

---

### **9. Practice**

* Now, try calculating probabilities for other ranges or generating random numbers with different distributions in Python.

---

✅ **Key Takeaways**

1. Continuous variables can take any value in a range.
2. Continuous distributions are represented as curves, not blocks.
3. Probability = area under the curve.
4. Uniform distribution is simple: all values equally likely.
5. Python’s `uniform.cdf()` and `uniform.rvs()` are useful tools.

---
