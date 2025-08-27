
# Variables, Assignments, Inputs and Outputs

# Variables
Save value to a variable. The variable is the "set to" value after the equals sign in the code.
```python
# Number variable
var = 10

# Text variable
text = "hello"

```

You can call these variables back after you set them for example:
```python
# Calling var
var 
> 10


# Calling text
text
> hello
```


Some tricks. 
 - Variables cant start with a number
	 - But they can contain a number
-  Variables cant have spaces
	- The common notation to replace a space is an underscore _


## Variable Types
The variables above are not comparable. Var is a number and text is... well text. These have fancy names in coding languages. For now, we will talk about these. 

- Text type: **str**
- Numeric Types: **int**, **float**

**str** is just text. But what is the difference between **int** and **float**? 
	**int** is an integer (think -2, -1, 0, 1, 2,.....)
	**float** is a real number (think .5, .123, -.124, 5.353, .....)


If you are ever unsure of what type a variable is. Use the built-in command "type()". For example:
```python
var = 10
type(var)
> <class 'int'>

var = "hello"
type(var)
> <class, 'str'>

var = 3.5
type(var)
> <class, 'float'>
```


