# Lecture 5
## Range Function
- The range function makes a list of number with a specified pattern. 
```python
range(start, stop, step)
```
- 'Start' will always be the start of the list
	- Defaults to zero
- The 'Stop' value will never be included in the list regardless of the step
- 'Step' will describe the steps between values within the list
	- Defaults to one

**Note:** To view this as a list you need to call range within the list function, Ex:
```python
list(range(5))
>[0,1,2,3,4]
```

You can determine the length of a list with:
```python
len(range(5))
>5
```
or
```python
import math
math.ceil((stop - start)/step)
```

**Examples:**
```python
list(range(1,10,3))
>[1,4,7]

list(range(0, 15, 2))
>[0, 2, 4, 6, 8, 10, 12, 14]

import math
math.ceil((10 - 1)/3)
>3
math.ceil((15 - 0)/2)
>8
```
# Lecture 6
## While loops
 - A while loops is a loop that continues until a stopping condition is meet. Ex:
```python
i = 0 
while i < 3:
	print(i)
	i += 1 
	
> 0
> 1
> 2
```

**Note:** you can have an input as the condition in the while loop