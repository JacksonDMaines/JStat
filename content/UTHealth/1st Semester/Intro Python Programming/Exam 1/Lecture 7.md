# Functions
Create your own functions, see example:
```python
def model_one()
	word = input("Enter word: ")
	L = len(word)
	ans = word * L
	print(ans)
	
# or

def model_one()
	word = input("Enter word: ")
	L = len(word)
	ans = word * L
	return ans
```
- return vs print
	- return allows you to assign the output of the function to a variable
	- print just prints as you might expect....

**Note:**
- Variables inside a function are considered local variables, so you should be able to call them outside of function. 
	- Example: *L* 


You call the function by calling the name said function. 
```python
model_one()
> Enter word: test
> testtesttesttest
```


You can additionally add arguments to functions. As showed below: 
```python
def model_one(a)
	word = input("Enter word: ")
	ans = word * a
	print(ans)
	
model_one(3)
>Enter word: test
>testtesttest
```


