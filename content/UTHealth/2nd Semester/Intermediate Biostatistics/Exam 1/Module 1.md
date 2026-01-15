## Lecture #1
- Sensitivity: $P(T^+|D^+)$
- Positive Predicted Value: $P(D^+|T^+)$
- False Negative Rate: $P(T^-|D^+)$
- Specificity: $P(T^-|D^-)$
- Negative Predicted Value: $P(D^-|T^-)$
- False Positive Rate: $P(T^+|D^-)$
- Prevalence: $P(D^+)$
**Note:** Complement of conditional
$$
(A|B)^c = A^c|B
$$
So False Negative Rate is complement of Sensitivity, and False Positive Rate is complement of Specificity

**Bayes Rule:**
$$
P(B|A) = \frac{P(A \cap B)}{P(A)}
$$
**(Simple) Total Probability Rule:** 
$$
P(A) = P(A|B)P(B)+P(A|B^c)P(B^c)
$$
