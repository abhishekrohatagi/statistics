
---

## 🔑 What are Tree Diagrams?

* A **tree diagram** is a **visual tool** to solve probability problems.
* It breaks down a problem into **branches** → each branch represents a possible outcome and its probability.
* Very useful when:

  1. Events happen in sequence (like first event, then second).
  2. Outcomes depend on what happened before.

---

## 🏸 Example 1: Tanya Playing Tennis

* Probability it’s sunny = 0.6
* If sunny → Tanya plays tennis = 0.8 (doesn’t play = 0.2)
* If not sunny (0.4) → Tanya plays tennis = 0.35 (doesn’t play = 0.65)

### Step 1: Draw the tree

* First split: **Sunny (0.6)** vs **Not Sunny (0.4)**
* Second split from each branch: **Play** or **Don’t Play** with given probabilities.

### Step 2: Multiply along each path (AND rule)

* Sunny & Plays = 0.6 × 0.8 = 0.48
* Not Sunny & Plays = 0.4 × 0.35 = 0.14

### Step 3: Add paths that satisfy the condition (OR rule)

* Probability Tanya plays = 0.48 + 0.14 = **0.62**

👉 So Tanya has a **62% chance** of playing tennis this Saturday.

---

## 🍬 Example 2: Sweets in a Bag

* Total sweets = 10 (7 red, 3 blue)
* Chen picks 2 sweets without replacement.
* Find probability both are the same color.

### Step 1: First pick

* Red = 7/10, Blue = 3/10

### Step 2: Second pick (depends on the first)

* If first Red → remaining = 6 red, 3 blue → Probabilities = 6/9, 3/9
* If first Blue → remaining = 7 red, 2 blue → Probabilities = 7/9, 2/9

### Step 3: Multiply for each path

* Red → Red = (7/10) × (6/9) = 42/90
* Blue → Blue = (3/10) × (2/9) = 6/90

### Step 4: Add for OR rule (same color)

* Probability (same color) = 42/90 + 6/90 = 48/90 = **8/15**

👉 So, the probability Chen picks two sweets of the same color = **8/15**.

---

## 📌 Key Learnings for Notebook

1. **Tree diagrams** help visualize sequential probability problems.
2. **Steps to solve using a tree diagram**:

   * Draw branches for each possible outcome.
   * Multiply probabilities along a branch (**AND rule**).
   * Add probabilities of different branches if they lead to the desired outcome (**OR rule**).
3. Example Results:

   * Tanya plays tennis → **0.62 probability**.
   * Chen picks same color sweets → **8/15 probability**.

---



Would you like me to also make a **step-by-step diagram sketch (ASCII style tree)** for Tanya’s tennis example so you can quickly visualize it in your notes?
