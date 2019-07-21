# Python Object Oriented

### Class

* Declaration

```python
class ClassName:
  'Documenting'  
```

* Getting the class documenting
```python
className.__doc__
```

* Constructor
```python
class className:

  __init__(self,param1,param2):
    ...
```

* Class Variable
```python
class className:
  variable1 = 10 # I will be shared to all instance objects
```

* Managing attributes in an object

```python
hasattr(emp1, 'age')    # Returns true if 'age' attribute exists
getattr(emp1, 'age')    # Returns value of 'age' attribute
setattr(emp1, 'age', 8) # Set attribute 'age' at 8
delattr(empl, 'age')    # Delete attribute 'age'
```

* Built-In class attribiutes

```python
print "Employee.__doc__:", Employee.__doc__
print "Employee.__name__:", Employee.__name__
print "Employee.__module__:", Employee.__module__
print "Employee.__bases__:", Employee.__bases__
print "Employee.__dict__:", Employee.__dict__
```

### Subclass

```python
class Parent:        # define parent class
   parentAttr = 100
   def __init__(self):
      print "Calling parent constructor"

   def parentMethod(self):
      print 'Calling parent method'

   def setAttr(self, attr):
      Parent.parentAttr = attr

   def getAttr(self):
      print "Parent attribute :", Parent.parentAttr

class Child(Parent): # define child class
   def __init__(self):
      print "Calling child constructor"

   def childMethod(self):
      print 'Calling child method'

c = Child()          # instance of child
c.childMethod()      # child calls its method
c.parentMethod()     # calls parent's method
c.setAttr(200)       # again call parent's method
c.getAttr()          # again call parent's method
```

* Check if the class is subclass of a given super class: issubclass(sub, sup)
* Check if the object is instance of a given class: isinstance(obj, Class)

### Overriding
```python
class Parent:        # define parent class
   def myMethod(self):
      print 'Calling parent method'

class Child(Parent): # define child class
   def myMethod(self):
      print 'Calling child method'

c = Child()          # instance of child
c.myMethod()         # child calls overridden method
```

### Static attribute x instance attribute
```python
class className:

  classAttribute = 0
  
  __init(self):
    self.instanceAttribute = 1
```

### References

https://www.tutorialspoint.com/python/python_classes_objects
