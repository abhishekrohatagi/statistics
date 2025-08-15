
---

## **1. What is “Coding” (in statistics)?**

* Not related to programming!
* *Coding data* means **transforming** data into a new scale or format — usually to make calculation/interpretation easier.
* Two most common transformations:

  * **Scaling** – multiplying or dividing values (e.g., converting inches to cm).
  * **Shifting** – adding or subtracting a constant (e.g., moving values relative to a baseline).

Example: Converting **Fahrenheit ➝ Celsius**

$$
C = \frac{5}{9}(F - 32)
$$

---

## **2. Scaling**

* Multiply/divide all data points by a constant.
* **Effect on Mean:** Multiplied/divided by the same factor.
* **Effect on Standard Deviation:** Also multiplied/divided by the same factor.

> If $Y = aX$, then
>
> $$
> $$

\mu\_Y = a\mu\_X,\quad \sigma\_Y = a\sigma\_X
]

---

## **3. Shifting**

* Add/subtract a constant to all values.
* **Effect on Mean:** Increases/decreases by that constant.
* **Effect on Standard Deviation:** *No change* (spread remains same).

> If $Y = X + b$, then
>
> $$
> $$

\mu\_Y = \mu\_X + b,\quad \sigma\_Y = \sigma\_X
]

---

## **4. Combined Coding Formula**

General coding:

$$
Y = aX + b
$$

| Statistic | Formula                      | Effect of shift $b$ |             |             |
| --------- | ---------------------------- | ------------------- | ----------- | ----------- |
| Mean      | $\mu_Y = a\mu_X + b$         | included            |             |             |
| SD        | ( \sigma\_Y =                | a                   | \sigma\_X ) | **ignored** |
| Variance  | $\sigma_Y^2 = a^2\sigma_X^2$ | **ignored**         |             |             |

---

## **5. Example – Fahrenheit to Celsius**

Given: Mean = 64°F, SD = 15°F
Conversion formula: $C = \frac{5}{9}(F - 32)$

* Mean in °C:

  $$
  \mu_C = \frac{5}{9}(64 - 32) = 17.8°\text{C}
  $$
* SD in °C:

  $$
  \sigma_C = \frac{5}{9} \times 15 = 8.3°\text{C}
  $$

*Note:* The “−32” shift does **not** affect SD, only the scaling factor matters.

---

## **6. Reverse Coding Example**

Given: $X = \frac{M - 1200}{10}$,
and $\mu_X = 2.1$, $\sigma_X = 1.4$ → find mean & SD of $M$

* Formula rearranged: $M = 10X + 1200$

* Mean:

  $$
  \mu_M = 10(2.1) + 1200 = 1221
  $$

* SD:

  $$
  \sigma_M = 10 \times 1.4 = 14
  $$

---

## **7. Key Takeaways**

* **Scaling affects both mean & SD.**
* **Shifting affects only the mean.**
* Use coding to:

  * Work in more convenient units
  * Avoid converting large datasets point-by-point
  * Simplify calculation or interpretation

---

