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

