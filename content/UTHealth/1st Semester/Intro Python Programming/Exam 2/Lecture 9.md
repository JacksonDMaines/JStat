# Lists
## List Functions
The correct name for this is methods but we can call this list functions. These use the . notation to alter or adjust a list. Ex:
```python
rolls = [4,6,6,2,6]
rolls.append(1)
print(rolls)
>[4,6,6,2,6,1]
rolls.count(6)
>3
rolls.remove(6)
print(rolls)
>[4,6,2,6,1]
```
You should note some of the interesting characteristics of these functions. There is no need to save the list again with this function, it does all the edits to the list itself.  

Many function have an non permanent version if you just add 'ed' to end of function name. These are typical functions so the argument is the list, no need for the . notation. 
## List Slicing
You can parse a section of a list with the indexes.
```python
dna = 'CTGACGACTT'
dna[5]
>"G"
dna[:5]
>"CTGAC"
dna[5:]
>"GACTT"
```
**Note:** The notation is **list\[n:m]** 
- **n**, is the index of the first value in the slice
- **m-1**, is the index of the last value in the slice 
- If **n** or **m** is missing you either start from the beginning or go till in.
- Negative indexes are a thing too, just think of the last value as -1 and second to last as -2 and so on




