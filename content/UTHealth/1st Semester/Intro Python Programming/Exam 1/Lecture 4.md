# HW 2 Notes
Ways to do Other way to do HW1 part 2? with converting time to seconds. 
```python
# Input all as one tuple. 
inputs = int(input("Input hours:")),int(input("Input minutes:")),int(input("Input seconds:"))
```
Or
```python
# Input as one string and split into 3 variables.
hour,minutes,seconds = input("Enter hours:minutes:seconds").split(":")
# This is all still a string. So you need to switch to int before converting to seconds. 
```
# Conditions and If Loops

## Conditions
Boolean is a either a True or False. Its data type is a `bool`. 

| Boolean Operators | Meaning               |
| ----------------- | --------------------- |
| <                 | less than             |
| <=                | less than or equal    |
| >                 | greater than          |
| >=                | greater than or equal |
| =                 | equal                 |
| !=                | not equal             |
### Boolean Operations
This is basic logic, `and`, `or` and `not`. The order of operations for these are first `not`, second `and`, last `or`.  

| P   | Q   | P and Q | P or Q |
| --- | --- | ------- | ------ |
| F   | F   | F       | F      |
| T   | F   | F       | T      |
| F   | T   | F       | T      |
| T   | T   | T       | T      |
All `not` does is change the to the opposite Boolean. False -> True or True -> False. 

## Loops
Loops work like any other coding language. Just be careful because when you want to initialize a loop you need to use **":"**. Then everything within that loop needs to be indented to the same length. 

**Ex:** If else 
```python
number = float(input("Enter an integer: "))
if number < 0:
	print(number, "is negative")
else: 
	print(number, "is a fine number")
print("Until next time...")
```
 - **Note:** the indent in this needs to be consistent throughout the block 
 - **Note:** colon defines the block

You can also to `elif` to use s else if statement.
```python
number = float(input("Enter an integer: "))
if number < 0:
	print(number, "is negative")
elif number > 0: 
	print(number, "is a positive")
else:
	print(number, "is zero")
print("Until next time...")
```
