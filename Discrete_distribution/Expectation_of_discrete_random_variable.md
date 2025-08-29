
---

## **What is the Expectation (or Expected Value)?**

* The **Expectation** of a discrete random variable is like the **average value you expect** if the random process happens many times.
* It is a **weighted average**, where each possible value is multiplied by its probability.

**Formula:**

$$
E(X) = \sum [x_i \cdot P(X = x_i)]
$$

Where:

* $x_i$ = each possible value of the random variable
* $P(X = x_i)$ = probability of that value (from PMF)

✅ Simple way to think:

> “If I repeat this random experiment many times, on average what number should I expect?”

---

### **Simple Example**

**Dice Roll:**

* Random variable $X$ = number on a dice (1–6)
* Probability of each value = 1/6

$$
E(X) = 1*(1/6) + 2*(1/6) + 3*(1/6) + 4*(1/6) + 5*(1/6) + 6*(1/6) = 3.5
$$

* Even though you **can’t roll 3.5**, this is the **average outcome over many rolls**.

---

### **Real Business Use Case**

**Scenario:** Amber Student wants to know **average number of bookings per student in a year**.

Suppose we have this PMF (from actual business data):

| Bookings (X) | Probability P(X) |
| ------------ | ---------------- |
| 0            | 0.05             |
| 1            | 0.35             |
| 2            | 0.35             |
| 3            | 0.15             |
| 4            | 0.08             |
| 5            | 0.02             |

**Expected number of bookings per student:**

$$
E(X) = 0*0.05 + 1*0.35 + 2*0.35 + 3*0.15 + 4*0.08 + 5*0.02
$$

$$
E(X) = 0 + 0.35 + 0.7 + 0.45 + 0.32 + 0.1 = 1.92
$$

✅ **Interpretation:** On average, a student books **\~2 accommodations per year**.

---

### **Why is this useful for business?**

1. **Staffing & Resource Planning:** If average bookings = 2 per student, plan inventory, rooms, or support accordingly.
2. **Revenue Forecasting:** Multiply expected bookings by average revenue per booking → estimate expected revenue.
3. **Marketing Strategy:** Identify if promotions can increase the expected number of bookings.

---


