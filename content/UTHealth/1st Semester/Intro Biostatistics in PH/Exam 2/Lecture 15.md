# Two-Sample Test for Independent Data

## Independent Two-Sample CLT
- Independence within and between groups
- $n_{1},n_{2}\geq 30$
- groups are not heavily skewed
$$
t= \frac{(\bar{X}_{1}+\bar{X}_{2})-(\mu_{1}-\mu_{2})}{\sqrt{ \frac{s^2_{1}}{n_{1}} + \frac{s_{2}^2}{n_{2}} }} \sim N(0,1)
$$

## Independent Two-Sample t-Test 
### Unequal Variances
- Independence within and between groups
- Normality among samples 
- **Variances are unequal**

$$
t = \frac{\bar{X}_{1}-\bar{X}_{2}-(\text{null value})}{\sqrt{\frac{s^2_{1}}{n_{1}}+\frac{s^2_{2}}{n_{2}}}} \sim t_{df}
$$
- df = Welch-satterthwaite's 

### Equal Variances
- Independence within and between groups
- Normality among samples 
- **Variances are equal**
$$

t = \frac{\bar{X}_{1}-\bar{X}_{2}-(\text{null value})}{\sqrt{s^2_{polled}\left( \frac{1}{n_{1}}+\frac{1}{n_{2}} \right)}} \sim t_{n_{1}+n_{2}-2}
$$





