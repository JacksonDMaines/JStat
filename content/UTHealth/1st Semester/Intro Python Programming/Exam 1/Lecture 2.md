# Python Math
# Order of Operations

| Operator | Description                   |
| -------- | ----------------------------- |
| **       | Exponentiation                |
| + -      | Positive and Negative (Unary) |
| * /      | Multiplication and Division   |
| + -      | Addition and Subtraction      |
| =        | Assignment                    |

## Division
Typical division utilize "**/**". This will always give you a [[UTHealth/1st Semester/Intro Python Programming/Exam 1/Lecture 1#Variable Types|float]]. 

### Floor Division
Rounds normal division down to nearest integer. 
- Notated by "**//**". 


## Mod (Remainder)
The remainder of one number being divided by another.
- Notated by "**%**". 

## Imported Functions
```python
import math
```
You need to import math to use function in math. For example sqrt, pow, pi, cos, sin....

To actually use these functions, you need to call the package before the function like the following. 
```python
import math

math.sin(1)
math.sqrt(2)
math.pow(2, 4)
```

Note: Any function called by math will result in a [[UTHealth/1st Semester/Intro Python Programming/Exam 1/Lecture 1#Variable Types|float]]. Some built-in function will stay an [[UTHealth/1st Semester/Intro Python Programming/Exam 1/Lecture 1#Variable Types|int]](for example pow).


