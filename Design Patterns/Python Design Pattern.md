# Python Design Patterns

This article is under construction, the objective is cover the design pattern for Python in a macro level

#### Pre-bound pattern

In Python everything is an object, as functions or even classes. You can create object instances from classes inside your scope or from an imported module. This pre-bound pattern aims instantiate objects in the module execution time, so, instead of you instantiate an object, you can just call the methods from the object instantiated in the module, when you imported it. 

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

# References

https://python-patterns.guide/python/prebound-methods/


module’s global namespace?