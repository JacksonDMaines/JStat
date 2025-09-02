# Spread

## Sample Variance
$$
s^2=\frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n-1}
$$

Question: Why squared? Why not use absolute value? 
Answer: Cause its harder down the road to use absolute value. Think derivatives. (Not continuous with abs)

Unit for sample variance is squared. 


## Sample Deviation
$$
s = \sqrt{s^2 }=\sqrt{\frac{\sum_{i=1}^{n}(x_{i}-\bar{x})^2}{n-1}}
$$

Unit for sample standard deviation is normal.

## IQR
Interquartile Range
$$
IQR = Q_{3}-Q_{1}
$$

middle 50% of data.

# Histogram
- Modality: # of prominent peaks in histogram
- Skewness: Measurement of distortion
- Outliers

### Modality
- 1 peak: Unimodal
- 2 peaks: Bimodal
- 2+ peaks: Multimodal
- 0 peaks: Uniform

## Skewness (asymmetric vs symmetric)
- Right Skew (Positive Skew): Tail on right
- Left Skew (Negative Skew): Tail on left

Utilize 'moderately' verbiage here  

Note: Uniform dist. is symmetric

## Outliers
Observation(s) that are far from the majority of the data.

## Bin width 
subjective.

# Boxplot
- graphing locality, spread,  and skewness of data
![[IMG_0391.jpeg]]
## Whiskers
Can reach up to the following:
- Upper Whisker: $Q_{3}+1.5(IQR)$
- Lower Whisker: $Q_{1}-1.5(IQR)$

Note: Whiskers cant extend past the min/max observation. So they get cut accordingly. 


# Robust Estimates
- Robust: Median and IQR
	- When you include extreme values these are effect very little. 
- Not Robust: Mean and SD
	- Gets dragged by extreme values. 

