
---

# 📘 Chapter: Hypothesis Testing in Business

## 1. Introduction to Hypothesis Testing

In business decision-making, we often need to test if an assumption (hypothesis) about a population is true or not.

* **Null Hypothesis (H₀):** Assumes there is no effect/difference.
* **Alternative Hypothesis (H₁):** Assumes there is an effect/difference.
* **p-value:** Probability of observing the sample result if H₀ is true.
* **Significance Level (α):** Commonly 0.05 (5%). If p < α, reject H₀.

👉 Hypothesis testing helps businesses:

* Compare sales performance between regions.
* Check customer preferences.
* Validate marketing campaign results.
* Analyze product defects and quality control.

---

## 2. **t-Test (Comparing Means)**

### Purpose

Used to compare the **means** of two groups and check if the difference is statistically significant.

### Formula (One-sample t-test)

$$
t = \frac{\bar{X} - \mu}{s / \sqrt{n}}
$$

where,

* $\bar{X}$ = sample mean
* $\mu$ = population mean
* $s$ = sample standard deviation
* $n$ = sample size

### Types of t-tests

1. **One-sample t-test** → Compares sample mean to population mean.
2. **Independent t-test** → Compares means of two independent groups.
3. **Paired t-test** → Compares means before and after treatment (same group).

### Business Example

👉 A retail chain wants to test whether the **average monthly sales after a new ad campaign** is higher than the historical average of \$50,000.

* H₀: μ = 50,000 (no increase in sales).
* H₁: μ > 50,000 (sales increased).
* Run a **one-sample t-test** with sample sales data.

If p < 0.05 → campaign is effective.

---

## 3. **Chi-Square Test (Testing Categories/Proportions)**

### Purpose

Used to test the relationship between **categorical variables** or the **goodness of fit**.

### Formula (Chi-Square statistic)

$$
\chi^2 = \sum \frac{(O - E)^2}{E}
$$

where,

* $O$ = observed frequency
* $E$ = expected frequency

### Types of Chi-Square Tests

1. **Goodness of Fit Test** → Does sample data match expected distribution?
2. **Test of Independence** → Are two categorical variables related?

### Business Example

👉 A marketing manager wants to check if **customer preference for product type (Basic, Standard, Premium)** is independent of **gender (Male, Female)**.

* H₀: Customer preference is independent of gender.
* H₁: Customer preference depends on gender.
* Use **Chi-Square Test of Independence** on survey data.

If p < 0.05 → preference differs by gender → useful for targeted marketing.

---

## 4. **ANOVA (Analysis of Variance)**

### Purpose

Used to compare **means of 3 or more groups**.
Instead of running multiple t-tests, ANOVA reduces error and controls Type-I error rate.

### Formula (One-way ANOVA F-statistic)

$$
F = \frac{MS_{between}}{MS_{within}}
$$

where,

* $MS_{between}$ = variance between groups
* $MS_{within}$ = variance within groups

### Types of ANOVA

1. **One-way ANOVA** → Compares means across one factor (e.g., sales in different regions).
2. **Two-way ANOVA** → Compares means across two factors (e.g., sales by region & season).

### Business Example

👉 A restaurant chain tests whether **average customer satisfaction ratings** differ across **3 cities (Delhi, Mumbai, Bangalore)**.

* H₀: All cities have the same average satisfaction.
* H₁: At least one city differs.
* Run **One-way ANOVA**.

If p < 0.05 → significant difference → management should investigate why.

---

## 5. Business Insights from Hypothesis Testing

* **t-test** → Did sales improve after a new strategy?
* **Chi-Square** → Is customer preference linked to demographics?
* **ANOVA** → Which branch or region performs better?

