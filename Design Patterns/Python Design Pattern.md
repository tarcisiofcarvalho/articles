# Python Design Patterns

This article is under construction, the objective is cover the design pattern for Python in a macro level

### Pre-bound Pattern

In Python everything is an object, as functions or even classes. You can create object instances from classes inside your scope or from an imported module. This pre-bound pattern aims instantiate objects in the module execution time, so, instead of you instantiate an object, you can just call the methods from the object instantiated in the module, when you import it. 

As an example, you can call random.set_see(..) for example from *random* module. Just to see how the random does this, take a look in the code below. This pattern is used in many python libraries. 

```python
from datetime import datetime

class Random8(object):
    def __init__(self):
        self.set_seed(datetime.now().microsecond % 255 + 1)

    def set_seed(self, value):
        self.seed = value

    def random(self):
        self.seed, carry = divmod(self.seed, 2)
        if carry:
            self.seed ^= 0xb8
        return self.seed

_instance = Random8()

random = _instance.random
set_seed = _instance.set_seed
```

### Sentinel Object Pattern

In programming, we have always to deal with exceptions, unexpected values, null and so on. A sentinel object has a value that can simplify your code, avoiding you to handle exceptions for common operations as a string not found in a search. For example, you can bring "-1" or "None"if the sub-string was not found in a string, instead of to raise an exception.

The sentinel pattern itself refers to object identity, not to the object value itself.

### Null Pointer Pattern

Python does not support Null Point Pattern, because each "name" in Python is a pointer that stores the address of an object to which it refers. So, you won't see the "null pointer exception" in Python as in other languages.

### Null Object Pattern

Python "hasn't null pointer exceptions", however you can work with "null objects" that is a normal object with proper reference, just the name, or value of the object refers to something that describe your Null Object, as example "NO_CHILD" string object if you would like to associate it with a family tree data. 

### Constant Pattern

Usually we use Caps Letter "NUMBER_OF_DAYS" for constants, but it is not a rule itself. The constant pattern in Python has the only the sense that the object itself is imutable, but the name can still ne reassigned. Example:

```python
January = 1 # calendar.py

# you can change the value
import calendar
calendar.January = 13

# you can also delete the value
del calendar.January
```

# References

https://python-patterns.guide
