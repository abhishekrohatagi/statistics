
---

## **What is Variance?**

* **Variance** measures **how spread out** the values of a random variable are from the average (expectation).
* It tells us **how much uncertainty or risk** is there in the outcomes.

👉 Formula:

$$
Var(X) = E\big[(X - E(X))^2\big]
$$

Or easier:

$$
Var(X) = E(X^2) - [E(X)]^2
$$

Where:

* $E(X)$ = expectation (mean/average)
* $E(X^2)$ = expected value of squared outcomes

---

### **Simple Example (Dice 🎲)**

* A dice has outcomes {1,2,3,4,5,6}, all equally likely.
* Expectation = 3.5
* Variance ≈ 2.92

👉 Meaning: Outcomes are spread around 3.5 with average squared distance ≈ 2.92.

---

### **Business Use Case (Amber Student Example)**

Let’s use the same booking PMF (student bookings in a year):

| Bookings (X) | Probability P(X) |
| ------------ | ---------------- |
| 0            | 0.05             |
| 1            | 0.35             |
| 2            | 0.35             |
| 3            | 0.15             |
| 4            | 0.08             |
| 5            | 0.02             |

From before, we found:

$$
E(X) = 1.92
$$

---

#### Step 1: Compute $E(X^2)$

$$
E(X^2) = \sum [x^2 \cdot P(X=x)]
$$

$$
= 0^2*0.05 + 1^2*0.35 + 2^2*0.35 + 3^2*0.15 + 4^2*0.08 + 5^2*0.02
$$

$$
= 0 + 0.35 + 1.40 + 1.35 + 1.28 + 0.50 = 4.88
$$

---

#### Step 2: Apply variance formula

$$
Var(X) = E(X^2) - [E(X)]^2
$$

$$
Var(X) = 4.88 - (1.92)^2
$$

$$
Var(X) = 4.88 - 3.6864 = 1.1936
$$

---

### ✅ Interpretation

* Variance = **1.19** (standard deviation ≈ 1.09).
* This means: number of bookings per student usually fluctuates **around 1 to 2 bookings**.
* **Low variance** → most students behave similarly.
* **High variance** would mean some book very little, some book a lot (big differences).

---

### **Why is this useful for business?**

1. **Risk & Uncertainty:** Variance tells Amber Student how unpredictable student bookings are.
2. **Revenue Planning:** If variance is low → stable revenue; if high → need buffer plans.
3. **Target Marketing:** High variance might show two customer segments (light users vs heavy users).

---

👉 So:

* **Expectation = average outcome**
* **Variance = how spread out the outcomes are around that average**

---

