# Hypothesis Testing
"Decision Theory"
- Yes or No questions

P-Value 
- Is it enough?
- Standard to make decision

## Steps
1. Make hypothesis
2. Decide on significant level ($\alpha$)
3. Apply Test
4. Conclude


### Make Hypothesis 
- Needs to be quantifiable and verifiable
- Always about the <u>population</u> parameter (unknown)
	- Not about point estimate 

**Null:** $H_{0}$
- Claim that can be rejected
- An existing belief

**Alternative:** $H_{1}$
- Claim that can be supported
- New\Stronger perspective 

**Note:** The equality is only under the null hypothesis

**One-Sided Test:**
- Less than or greater than in $H_{1}$

**Two-Sided Test:**
- Not equal to in $H_{1}$
- Safer test

### Significant Value 
- $\alpha=0.05,0.01,0.1$
- Criteria to compare with p-value

- $P-Value\leq \alpha$
	- Reject $H_{0}$
- $P-Value>\alpha$ 
	- Fail to reject $H_{0}$
		- This doesn't mean $H_{0}$ is true


### How to get P-Value
- Test Statistics + Sampling Distribution
$$
t = \frac{x-\mu_{0}}{\frac{s}{\sqrt{ n }}}
$$ 
- One-Sided:
	- $P(Z>t)$ or $P(Z<t)$ 
- Two-Sided:
	- $2\cdot P(Z>|t|)$ 

**Note:** There is a close relationship between Two-Sided Hypothesis test and confidence interval
- If CI contains $\mu_{0}$ we could not reject
- If CI doesn't contain $\mu_{0}$ we could reject
## Error
- Type I and II

|              | Fail to Reject $H_{0}$ | Reject $H_{0}$ |
| ------------ | ---------------------- | -------------- |
| $H_{0}$ True | good                   | Type 1 Error   |
| $H_{A}$ True | Type 2 Error           | good           |
- $P(Type\space 1) = \alpha$
- $P(Type\space 2) =\beta$

- Trade off relationship between $\alpha$ and $\beta$

## Power
- Way to measure the performance of a test
- Higher power good

$$
Power = P(\text{rej } H_{0}|H_{1} \text{ true}) = 1-$\beta$
$$
- Looking for 80-90%
- Increases with:
	- Sig. Level
	- SD $\sigma \downarrow$
	- $n\uparrow$ 

## Practical vs Statistical Sig. 
- Sometimes P-Values lie
- Be careful....


