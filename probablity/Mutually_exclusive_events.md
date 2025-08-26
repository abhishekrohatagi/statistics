
---

## 🔑 Key Idea: Mutually Exclusive Events

* **Mutually exclusive events** = Events that **cannot happen at the same time**.
* Example:

  * Rolling a **6** (event A)
  * Rolling a **5** (event B)
  * On a single dice roll, you **cannot** get both 6 and 5 → so they are mutually exclusive.

---

## 📖 Formal Definition

Two events A and B are **mutually exclusive** if:

$$
P(A \text{ and } B) = 0
$$

That means there’s **no overlap** between the two events.

---

## ✅ Rule for Mutually Exclusive Events (OR Rule)

If events are mutually exclusive, then:

$$
P(A \text{ or } B) = P(A) + P(B)
$$

* Example: Probability of rolling an even number on a dice.

  * Even numbers = {2, 4, 6}
  * P(2) + P(4) + P(6) = (1/6) + (1/6) + (1/6) = 3/6 = 1/2

👉 Because rolling a 2, 4, or 6 **cannot happen at the same time**, we simply add them.

---

## 📊 Venn Diagram View

* **Mutually exclusive events** → No overlap in circles.
* **Non-mutually exclusive events** → Overlap exists (both can happen).

---

## 📝 General Rule (When events are NOT mutually exclusive)

If there’s an overlap, we must avoid double-counting:

$$
P(A \text{ or } B) = P(A) + P(B) - P(A \text{ and } B)
$$

This works **always**.

* For mutually exclusive events, $P(A \text{ and } B) = 0$, so the formula reduces to the simple add rule.

---

## 📝 Example from Lecture: Sam

* Probability Sam is late = 0.2
* Probability it rains = 0.25
* Probability both (rain and late) = 0.1

Now apply formula:

$$
P(\text{Rain or Late}) = P(\text{Rain}) + P(\text{Late}) - P(\text{Rain and Late})
$$

\= 0.25 + 0.2 − 0.1
\= 0.35

👉 So, the chance that either it rains or Sam is late = **35%**

---

## 📌 Key Learnings for Notebook

1. **Mutually exclusive events** = cannot happen at the same time.

   * Rule: $P(A \text{ or } B) = P(A) + P(B)$
   * Condition: $P(A \text{ and } B) = 0$

2. **General OR Rule (Addition Rule):**

   $$
   P(A \text{ or } B) = P(A) + P(B) - P(A \text{ and } B)
   $$

   * Works for **all** cases.

3. **Example:**

   * Dice: Even numbers = 2, 4, 6 → probability = 1/2
   * Sam: Late (20%), Rain (25%), Both (10%) → OR probability = 35%

---

👉 So:

* **Independent events** = events don’t affect each other (AND rule).
* **Mutually exclusive events** = events can’t happen together (OR rule).

---

