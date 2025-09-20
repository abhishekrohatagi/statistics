
---

# **Chapter: Quality of Test**

In statistics, whenever we run a hypothesis test, we want to make **good decisions** based on data. But tests are not perfect. Sometimes they can make mistakes, and sometimes they can be powerful or weak. This chapter explains the **quality of a test**, how to measure it, and things that can go wrong.

---

## **1. Type 1 Error and Type 2 Error**

When we do a hypothesis test, we start with:

* **Null hypothesis (H₀)** – the default assumption (e.g., “this marketing campaign has no effect on sales”)
* **Alternative hypothesis (H₁)** – the claim we want to test (e.g., “this campaign increases sales”)

**The two types of mistakes a test can make:**

| Error Type           | Happens When                                      | Example (Business)                                                                                                                                |
| -------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Type 1 Error (α)** | We **reject H₀** when it is actually true         | A company thinks a new ad increases sales, runs the campaign, but in reality, it had no effect. The company wasted money.                         |
| **Type 2 Error (β)** | We **fail to reject H₀** when H₁ is actually true | A company thinks a new website layout has no effect on conversions, but it actually **does improve conversions**. They miss out on extra revenue. |

**Key Points:**

* Type 1 error is also called **false positive**.
* Type 2 error is also called **false negative**.
* Reducing one error usually increases the other.

**Business Example:**

A startup tests whether giving a 10% discount increases sales.

* **H₀:** Discount does not increase sales
* **H₁:** Discount increases sales

If they **reject H₀ by mistake**, they think the discount works (Type 1 error).
If they **don’t reject H₀ when discount actually works**, they miss an opportunity (Type 2 error).

---

## **2. Size and Power Analysis**

### **Size of a test (α):**

* Size is the **probability of making a Type 1 error**.
* Example: If α = 5%, there’s a 5% chance we wrongly reject H₀.
* **Smaller α** → safer from false positives, but increases Type 2 error.

### **Power of a test (1 – β):**

* Power is the **probability of correctly rejecting H₀** when H₁ is true.
* High power means the test is **likely to detect a real effect**.

**Factors affecting power:**

1. **Sample size**: Bigger sample → higher power
2. **Effect size**: Bigger real effect → higher power
3. **Significance level (α)**: Higher α → slightly higher power

**Business Example:**

A company tests a new pricing strategy:

* They compare 100 customers vs. 10,000 customers.
* With 100 customers, even if the strategy works, test may **not detect** it → low power.
* With 10,000 customers, test can detect small effects → high power.

**Power Analysis in Excel (Simplified):**

1. Collect previous data (mean, std deviation).
2. Use Excel formula: `=NORM.S.DIST(z, TRUE)` to calculate probabilities.
3. Calculate **power** using effect size, sample size, and α.
4. Adjust sample size to achieve desired power (usually ≥ 80%).

---

## **3. P-Hacking**

**P-hacking** is a **bad research practice**:

* Manipulating data or tests until you get a “significant” result (p < 0.05).

**How it happens:**

* Trying multiple tests on same data and reporting only the ones that “work.”
* Changing data, variables, or sample size to get a significant p-value.

**Why it’s bad:**

* Gives **false confidence** in results.
* Can mislead business decisions.

**Business Example:**

A company runs A/B tests for website design:

* They try 10 different metrics (clicks, time spent, purchases…).
* Only report “time spent increased significantly.”
* In reality, the increase could be due to **random chance**.

**How to avoid p-hacking:**

1. Predefine hypotheses before looking at data.
2. Limit number of tests.
3. Report all tests, not just significant ones.
4. Adjust significance for multiple testing (Bonferroni correction).

---

## **Summary Table**

| Concept       | Definition                                  | Business Example                             |
| ------------- | ------------------------------------------- | -------------------------------------------- |
| Type 1 Error  | Reject H₀ when true                         | Think discount works but it doesn’t          |
| Type 2 Error  | Fail to reject H₀ when false                | Don’t notice website layout improves sales   |
| Size (α)      | Chance of Type 1 error                      | 5% risk of false positive                    |
| Power (1 – β) | Chance to detect real effect                | Big customer sample detects effect           |
| P-hacking     | Manipulating data/tests to get significance | Reporting only favorable metrics in A/B test |

---

### **Key Takeaways for Data Analysts**

1. Always **check both Type 1 and Type 2 errors**.
2. Use **power analysis** to decide sample size before testing.
3. Avoid **p-hacking**; be transparent with data and methods.
4. Bigger sample size generally improves test reliability.
5. Real business decisions depend on understanding these errors — wrong conclusions cost money.

---


Do you want me to do that next?
