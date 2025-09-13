# Conditional Probabilities

Let $A$ and $B$  be events then 
$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$
this can be rearranged for example
$$
P(A\cap B)=P(A|B)P(B)
$$
## Diagnostic Accuracy Measures
Imagine this example:
- **$D^+$:** Having disease
- **$D^-$:** Not having disease
- **$T^+$:** Test positive
- **$T^-$:** Test negative

### Sensitivity(TPR):
- $P(T^+|D^+)$
Probability of a positive test when person has disease

### Positive Prediction Value(PPV):
- $P(D^+|T^+)$
Probability of having the disease given they have a positive test 

### Specificity(TNR):
- $P(T^-|D^-)$
Probability of a negative test when person has no disease

### Negative Prediction Value(NPV):
- $P(D^-|T^-)$
Probability of not having the disease given they have a negative test

### False Negative Rate(FNR):
- $P(T^-|D^+)$

### False Positive Rate(FPR):
- $P(T^+|D^-)$

### Prevalence 
- $P(D^+)$ 
Probability of disease in the population. 


|       | $D^+$                                          | $D^-$                                           |                                  |
| ----- | ---------------------------------------------- | ----------------------------------------------- | -------------------------------- |
| $T^+$ | True Positive ($TP$)                           | False Positive ($FP$)                           | $PPV=\frac{TP}{TP+FP}$           |
| $T^-$ | False Negative ($FN$)                          | True Negative ($TN$)                            | $NPV=\frac{TN}{FN+TN}$           |
|       | $TPR =\frac{TP}{TP+FN}$ $FNR=\frac{FN}{TP+FN}$ | $TNR=\frac{TN}{FP+TN}$ $FPR = \frac{FP}{FP+TN}$ | $Prev=\frac{TP+FN}{TP+FN+FP+TN}$ |


