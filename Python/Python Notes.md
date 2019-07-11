## Python Notes

Some Python language considerations

### Consideration about Python modules import 

As a script language Python execute all imported modules conditions, constants, looping, etc, it is useful, but you can broke your code if you assign a value by mistake to a variable declared at a module level, etc.

### Explicit vs implicit
Python programmers believe that “Explicit is better than implicit” 

### Getting Python Object ID

As everthing in Python is an object, you can get the object id using the function "id()" that usually corresponds the object address in the memory. 

```python
x = "Python Object"
print id(x)
200135852101020
```

### Some Python Libs

|lib/pkg|desc|
|---|---|
|pkgutil|utilities form import system, as files|
