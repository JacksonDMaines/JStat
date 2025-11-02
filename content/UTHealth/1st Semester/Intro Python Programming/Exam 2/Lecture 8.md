# Packages
You can rum packages, modules, or libraries with a simple command. 
```python
import random

from random import randint
```

- **import:** Just import the entire package. Meaning every single function
But what if you don't need every single function in a package.
- **from**: you can call the library you want, but with **import** you can call the individual function you need. 

**Note:** if you import the entire package, you will need to call the name of the library then . name of function. Ex:
```python
import random
random.randint(1,10)
```
But if you use from and call the individual function you don't need to use the . notation. Ex:
```python 
from random import randint
randint(1,10)
```

