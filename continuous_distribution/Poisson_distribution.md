
---

### **1. What is the Poisson distribution?**

The Poisson distribution is a way to find the **probability of a certain number of events happening in a fixed time or space**.

---

### **2. Poisson Process**

A **Poisson process** is when events happen:

* Completely at random
* At a certain average rate

**Examples:**

* Animals adopted from a shelter per week
* People arriving at a restaurant per hour
* Earthquakes per year in a region

**Key:** Time unit (hour, week, year) doesn’t matter as long as it’s consistent.

---

### **3. Poisson Distribution**

It **calculates probabilities for the number of events** in a fixed period.

**Example questions it can answer:**

* Probability of 5 animals being adopted in a week
* Probability of 12 customers in an hour
* Probability of fewer than 20 earthquakes in a year

---

### **4. Lambda (λ)**

* λ = average number of events per time period
* In our shelter example, λ = 8 adoptions per week
* λ is also the **expected value** (most likely number of events)

**Observation:** The distribution peaks at λ.

---

### **5. Lambda changes the shape**

* Smaller λ → distribution is narrow, mostly around small numbers
* Larger λ → distribution spreads out, peak at λ
* Peak **always at λ**

---

### **6. Probability of a single value**

* Probability of exactly 5 adoptions (when λ = 8)
* Use `poisson.pmf(5, 8)` → ≈ **9%**

---

### **7. Probability of less than or equal to a value**

* Probability of **≤ 5 adoptions** → use `poisson.cdf(5, 8)` → ≈ **20%**

---

### **8. Probability of greater than a value**

* Probability of **> 5 adoptions** → `1 - poisson.cdf(5, 8)` → ≈ **81%**
* If λ = 10 → probability of >5 adoptions ≈ **93%**

---

### **9. Sampling from a Poisson distribution**

* Use `poisson.rvs(λ, size=n)` to simulate multiple periods
* Example: simulate 10 weeks → adoptions might vary like 14 in one week, 6 in another

---

### **10. Central Limit Theorem still applies**

* If you take **many sample means** from a Poisson distribution, their distribution looks **normal**

---

### **11. Practice**

* Try calculating probabilities for different values of λ, single values, ≤ values, and > values

---

✅ **Key takeaway:** Poisson is all about **counting random events over a fixed time/space**, with λ as the average rate.

---

