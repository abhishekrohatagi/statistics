

## 🔹 What is Conditional Probability?

Conditional probability is the **probability of an event happening given that another event has already happened**.

It answers:
👉 *“What is the chance of Event A, given that Event B has already occurred?”*

Mathematically:

$$
P(A|B) = \frac{P(A \cap B)}{P(B)}
$$

Where:

* $P(A|B)$ = Probability of A **given** B
* $P(A \cap B)$ = Probability of both A and B happening
* $P(B)$ = Probability of B happening

---

## 🔹 Simple Example

* Probability of a person buying ice cream on any random day = **30%**.
* Probability that it’s a hot day = **40%**.
* Probability of both (Hot day **and** Ice cream bought) = **20%**.

So:

$$
P(IceCream|HotDay) = \frac{0.20}{0.40} = 0.50 = 50\%
$$

👉 This means: *On a hot day, the chance of someone buying ice cream is 50%.*

---

## 🔹 Business Use Case for Data Analytics

### **Case: E-commerce Platform (Amazon/Flipkart style)**

You are analyzing **customer purchase behavior**.

* Event A: Customer buys a **mobile phone cover**.
* Event B: Customer buys a **mobile phone**.

Now, conditional probability helps answer:
👉 *“If a customer has already bought a mobile phone, what is the probability they also buy a cover?”*

Suppose from data:

* Probability of buying a cover (A) = 0.20 (20%)
* Probability of buying a mobile (B) = 0.10 (10%)
* Probability of buying both (A ∩ B) = 0.08 (8%)

Then:

$$
P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{0.08}{0.10} = 0.80 = 80\%
$$

👉 Interpretation: *If a customer buys a phone, there’s an 80% chance they’ll also buy a cover.*

---

## 🔹 Why This Matters for Businesses?

1. **Recommendation Engines** – Amazon suggests “Frequently Bought Together” based on such probabilities.
2. **Targeted Marketing** – If probability of cross-sell is high, send personalized offers (e.g., “Buy a phone? Here’s 20% off on covers”).
3. **Customer Retention** – Banking sector uses conditional probability to predict “If a customer has a savings account, what’s the probability they will take a loan?”.
4. **Risk Analysis** – Insurance companies use it: “If a person smokes, what’s the probability of them filing a health claim?”

---


