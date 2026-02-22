# Equations

$$
\text{Point Prev = } \frac{\text{total with condition}}{\text{total in group}}
$$
$$
\text{Period Prev = } \frac{\text{\# with condition}}{\text{avg in group}}
$$

$$
\text{Incidence Prop. (Cum. Inc.) = } \frac{\text{\# new}}{\text{\# at risk}} \cdot \text{ person over time (person years)}
$$
$$
\text{Incidence Rate (density) = } \frac{\text{\# new}}{\text{total time}} \cdot \text{ person over time (person years)}
$$


$$
\text{Period Prev = } \text{Incidence} \cdot \text{Disease duration}
$$

$$
\text{Attack Rate = } \frac{\text{\# develop}}{\text{\# at risk}}
$$

$$
\text{Mortality Rate = } \frac{\text{\# death}}{\text{\# at risk}}
$$

$$
\text{Case Fatality Rate = } \frac{\text{\# dying}}{\text{\# with disease}}
$$

$$
\text{Direct Mortality Rate = } \frac{\text{\# Expected}}{\text{\# in Standard Pop.}}
$$

$$
\text{Standardized Mortality Ratio = } \frac{\text{\# obs. deaths}}{\text{\# of expected deaths}}
$$

## Validity
- $Sens = T^+|D^+$
- $Spec = T^-|D^-$
- $PPV = D^+|T^+$
- $NPV = D^-|T^-$

## Reliability
$$
\text{Percent agreement} = \frac{\text{\# of agreed}}{\text{total}}
$$

$$
\text{Kappa Stat.} = \frac{P_{obs}-P_{exp}}{1-P_{exp}}
$$
- $P_{obs} = \frac{TP+TN}{total}$
- $P_{exp} = \frac{TP_{exp} + TN_{exp}}{total}$
	- $TP_{exp} = \frac{\text{ row total}\cdot \text{col total}}{total}$


| $>.75$      | Excellent |
| ----------- | --------- |
| $.4<KP<.75$ | **Good**  |
| $<.4$       | **Poor**  |

$$
\text{Risk Ratio} = \frac{\text{Cumulative Incidence Exposed}}{\text{Cumulative Incidence Unexposed}}
$$

$$
\text{Rate Ratio} = \frac{\text{Incidence Rate Exposed}}{\text{Incidence Rate Unexposed}}
$$

- **RR>1:** "*Exposed has X.XX times risk/rate of developing condition compared to unexposed.*"
- **RR<1:** "*Exposed has X.XX times risk/rate of developing condition compared to unexposed.*"
	- "*Exposed has (1-.XX)% less risk/rate of developing condition compared to unexposed*"

$$
\text{Odds Ratio} = \frac{\text{a/c}}{\text{b/d}}
$$
- Where $a$ is ++ and $d$ is --

# Other
## Stages 
- Primary: Prevents Onset (Preclinical)
- Secondary: Early Detection (Clinical)
- Tertiary: Treat



| Epi- | -demi- | -ology |
| ---- | ------ | ------ |
| Upon | People | Study  |

- Distribution: When Where, Whom
- Determinates: Why? 
	- Pop, gene, social, pol. env.


**When**
- Prev $\uparrow$ : PPV $\uparrow$ NPV $\downarrow$
- Sens $\uparrow$ : PPV $\uparrow$ NPV $\uparrow$ 
- Spec $\uparrow$ : PPV $\uparrow$  NPV $\uparrow$ 
- Cutoff $\uparrow$ : Spec $\uparrow$ Sens $\downarrow$ PPV $\uparrow$ 
- Cutoff $\downarrow$: Sens $\uparrow$ Spec $\downarrow$ PPV $\downarrow$
PPV more effected by Spec.


**Temporality:** Time of cause and effect

- **Prospective:** Current
- **Retrospective:** Past


## Cohort
- Time-to-event
- Useful for rare and common exposure
- Bad for rare outcomes
- Follow up


## Bias
- **Selection:** Individual not randomly chosen
- **Information:** Systematic differences
	- Exposer id: technical error in baseline
	- Outcome: knowledge of exposure 


## Adjust
- **Direct:** Standard Pop., local Rates
	- Comparing States
- **Indirect:** Standard Rates, Local Pop.
	- Unknown Rates

## Analysis
- **Intention to Treat:** analyzed based on assigned group
- **Per-protocol:** Analyzed based on treatment taken. 

