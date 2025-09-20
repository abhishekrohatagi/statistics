
---

## 🔹 The Big Idea

We want to check if **Bitcoin and Ethereum prices move together** (are correlated) or not.
We do this using a **hypothesis test for correlation**.

---

## 🔹 Step 1: What is the question?

* We collected **monthly prices** of Bitcoin and Ethereum for 1 year → so **12 data points**.
* We calculated the **correlation coefficient (R)** = **0.533**.
* Question: *Is this strong enough evidence that Bitcoin and Ethereum are really correlated in the whole population?*

---

## 🔹 Step 2: Hypotheses

In hypothesis testing, we set up two statements:

* **Null Hypothesis (H0):** No correlation in the population (ρ = 0).
  👉 Bitcoin and Ethereum prices are *not related*.

* **Alternative Hypothesis (H1):** Positive correlation in the population (ρ > 0).
  👉 Bitcoin and Ethereum *are positively related*.

We test if the sample result (0.533) is strong enough to reject H0.

---

## 🔹 Step 3: Critical Value

* Correlation ranges between **-1 and +1**.
* We need to know: *What correlation value is big enough to count as “statistically significant” at the 1% level?*
* Formula uses **degrees of freedom = n - 2**.

  * Here, n = 12 → df = 10.
* At **1% significance**, the **critical value = 0.658**.
  👉 That means: unless R ≥ 0.658, we cannot claim real correlation.

---

## 🔹 Step 4: Compare

* Our sample R = **0.533**.
* Critical value = **0.658**.
* Since **0.533 < 0.658**, the sample correlation is **not strong enough**.

👉 **Conclusion:** We **do not reject H0**.
This means:

* We don’t have enough evidence to prove correlation.
* But this does **NOT** mean there is no correlation — just that we cannot prove it yet.

Think of it as: *“More research is needed.”*

---

## 🔹 Step 5: Bigger Sample Example

Now instead of 12 months, suppose we collect **365 daily prices**.

* n = 365 → df = 363.
* Critical value now is much smaller = **0.122**.
* Our sample R = **0.557**, which is way bigger than 0.122.

👉 Here, we can **reject H0** and confidently say:
“Yes, Bitcoin and Ethereum are correlated.”

---

## 🔹 Key Takeaways

1. **Small samples need higher correlation** to be considered significant.
   (Because small samples may show fake patterns by chance.)
2. **Large samples can detect even small correlations**.
3. Failing to reject H0 ≠ proving no correlation. It just means *not enough evidence yet*.
4. Always compare your observed R with the **critical value**.

---

✅ In simple terms:

* With 12 months of data → correlation 0.533 was *not enough* evidence.
* With 365 days of data → correlation 0.557 was *more than enough* evidence.

---

