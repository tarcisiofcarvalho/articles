# Objects in Python

### Mutable Objects

The mutable objects in Python are List, Set and Dict. You are able to change the objects inside these container. It is helpful, because you can change the size of these container without extra code.

### Immutable Objects

The immutable objects in Python are int, float, complex, string, tuple, frozen set [note: immutable version of set] and bytes. You are not able to change the object in memory, take a look:

```python
x = 10 # Will be created a int object in the memory
y = x # Will be created just a reference of identifier y to the object created by x

print id(x)
140677102993072

print id(y) # Will print the same object reference
140677102993072

# Lets try to change the value of x
x = 15
print id(x) # Will be created a new object, the current one was not changed
140677102992952

print id(y) # The y identifier is pointing to the same int object that contains 10
140677102993072
```
### References

https://medium.com/@meghamohan/mutable-and-immutable-side-of-python-c2145cf72747
