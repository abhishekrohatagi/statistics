
---

# 📘 Notes on Nonlinear Data (Exponential & Polynomial Relationships)

---

## 1. Why Linear Methods Don’t Always Work

* Correlation and regression work best when the relationship between **X and Y is straight-line**.
* But many real-world datasets are **curved (nonlinear)**:

  * Example: exponential growth, square root patterns.
* Using normal regression here can be misleading.

  * Correlation may look strong (e.g., 0.88) but the graph clearly shows a curve.

---

## 2. Exponential Data

* General form:

  $$
  y = a \cdot b^x
  $$

* Examples: population growth, compound interest, virus spread.

* Curve rises (or falls) sharply instead of forming a line.

---

## 3. Linearizing Exponential Data

* Trick: Plot **X vs log(Y)** instead of **X vs Y**.
* Why? Because logs transform the curve into a line.

From:

$$
y = a \cdot b^x
$$

Take logs:

$$
\log(y) = \log(a) + x \cdot \log(b)
$$

* Now it looks like a straight-line equation:

  * Intercept = $\log(a)$
  * Slope = $\log(b)$

---

## 4. Regression for Exponential Data

1. Plot X vs log(Y).
2. Run regression.
3. Convert intercept & slope back:

   * $a = 10^{\text{intercept}}$
   * $b = 10^{\text{slope}}$
4. Final model:

   $$
   y = a \cdot b^x
   $$

**Example:**

* Intercept = 1.747 → $a \approx 56$
* Slope = 0.05584 → $b \approx 1.14$

Final equation:

$$
y = 56 \cdot (1.14)^x
$$

(Meaning: Y increases by \~14% whenever X increases by 1.)

---

## 5. Polynomial (Power Law) Data

* General form:

  $$
  y = a \cdot x^b
  $$

* Examples:

  * $y = 20x^2$
  * $y = 3x^{0.5}$ (square root curve)

---

## 6. Linearizing Polynomial Data

* Trick: Plot **log(X) vs log(Y)**.

From:

$$
y = a \cdot x^b
$$

Take logs:

$$
\log(y) = \log(a) + b \cdot \log(x)
$$

* Straight-line equation:

  * Intercept = $\log(a)$
  * Slope = $b$

---

## 7. Regression for Polynomial Data

1. Take logs of both X and Y.
2. Plot log(X) vs log(Y).
3. Run regression.
4. Convert back:

   * $a = 10^{\text{intercept}}$
   * $b = \text{slope}$
5. Final model:

   $$
   y = a \cdot x^b
   $$

**Example:**

* Intercept ≈ 0.004 → $a \approx 1$
* Slope ≈ 0.525 → $b \approx 0.5$

Final equation:

$$
y = x^{0.5} = \sqrt{x}
$$

---

## 8. Key Takeaways

* If data is **exponential** → Plot **X vs log(Y)**.
* If data is **polynomial (power law)** → Plot **log(X) vs log(Y)**.
* Both transformations turn curves into **straight lines**, so regression works correctly.

✅ **In one line:**
Use logarithms to “straighten” curved data, run regression, then convert back to the original equation.

---

