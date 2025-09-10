# Extra Print Functions and Sequences

# Prints
- f strings. Can call vars in a string with certain degree of accuracy. 
```python
>>> results = 67/7
>>> print(f"this is equal to ${results:.2f}")
```
- the 2 in **2f** defines how many values after the decimal there are.

Here are some other forms.
```python
>>> print("this is equal to $", "{:.2f}".format(results))
>>> print("this is equal to $", format(results, '.2f'))
```


# Sequences
Sequences are a set of values. You can tell something is a sequence if you can call certain positions within the set. For Example
```python 
>>>var = [1,2,3,4]
>>>var[1]
2
```

Why does **var[1]** give 2 and not 1? Well sequences in python are indexed at 0, meaning they start at 0 and count up to n-1. 

| Index   | 0   | 1   | 2   | 3   |
| ------- | --- | --- | --- | --- |
| **var** | 1   | 2   | 3   | 4   |

What are some example of sequences? What was shown before with the **[]**'s was a list (you can confirm this by doing type(var)). You can also define list with the function list(). Other types of sequences are strings and tuples. Tuples can be defined by separating values with commas with or without **()**(parentheses are preferred). 

## Mutable vs Immutable
- **Mutable:** means you can edit the sequence. Meaning you can reassign values or add new values to the sequence. 
	- Only list are mutable.
- **Immutable:** means you cannot edit the sequence.
	- Tuples and strings are immutable. 

