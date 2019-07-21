## Python Notes

Some Python language considerations

### Python Memory Management

Python memory is managed by Python private heap space

### Iterator

```python
mystr = "banana"
myit = iter(mystr)

print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
```
### Clone object

```python
import copy

x = copy.copy(y)
z = copy.deepcoy(mydict)

```

### Find bugs or perform static analysis

PyChecker is a static analysis tool that detects the bugs in Python source code and warns about the style and complexity of the bug. Pylint is another tool that verifies whether the module meets the coding standard.

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

### Environment varialbles

* PYTHONPATH: Where the Python locate module files imported into a program
* PYTHONSTARTUP: It contains the path of an initialization file containing Python source code.
* PYTHONHOME: It is usually embedded in the PYTHONSTARTUP or PYTHONPATH directories to make switching module libraries easy.

### References

https://www.tutorialspoint.com/python/python_interview_questions

### Python datatypes supported

* Numbers
* Strings
* List
* Dictionary
* Tuple

### String

String is immutable

* Array: every string in python is an array
```python
x = 'test'
print x[0]
>>> t
```
* Substring

```python
x = test
print x[1:3]
>>> es
```

* Multiply string
```python
x = test
x = x * 2
print x
>>> testtest
```

* Caps letter
```python
x = "tarcisio"
print x.capitalize()
>>> Tarcisio
```

* All char is a number
```python
x = "12345"
print x.isalnum()
>>> True
```
* All char is a digit
```python
x = "Test"
print x.isdigt()
>>> False
```
* All char is space
```python
x = "     "
print x.isspace()
>>> True
```

* Text is titlecased
```python
x = "Test Number One"
print x.istitle()
>>> True
```

* Text is uppercase
```python
x = "Test Number One"
print x.uppercase()
>>> False
```

* All char is lower case
```python
x = "Test"
print x.islower()
>>> False
```

* Merge 
```python
x = ' '.join(x,y,z)
```

* Len
```python
print len(x)
```

* Convert to lower and upper case
```python
print x.lower() # Use upper instead
```

* Max and Min char
```python
string = "raj" 
print max(string) # Use min instead
>>> r
```

* Strip landing white spaced
```python
string = " Tarcisio "
print string.strip(' ') # Performs both lstrip() and rstrip() on string.
```

* Change lettercases
```python
string = " Tarcisio "
print string.swapcase(' ') # Performs both lstrip() and rstrip() on string.
>>> tARCISIO
```

* Change to Titlecase
```python
string = " tarcisio "
print string.title()
>>> Tarcisio

### List

* Enclosed by [] brackets
* Can be changed

* Multiply a list
```python
list = ['test', 'one']
newList = 2 * list
print newList
>>> ['test', 'one', 'test', 'one']
```

* Add a list
```python
list = ['test', 'one']
newList = list + list
print newList
>>> ['test', 'one', 'test', 'one']
```

### Tuple

* Enclosed by () parentheses 
* Can't be changed. Ready-only

* Multiply a list
```python
tuple = ('test', 'one')
newTuple = 2 * list
print newTuple
>>> ('test', 'one', 'test', 'one')
```

* Add a list
```python
tuple = ('test', 'one')
newTuple = tuple + tuple
print newTuple
>>> ('test', 'one', 'test', 'one')
```

### Dictionary

* Enclosed by {} curly braces 
* A kind of hashTable

### Converting things

* String to int
```python
x = "10"
y = int(x)
```

* String to long
```python
x = "10"
y = long(x)
```

* String to float
```python
x = "10"
y = float(x)
```

* String to object
```python
x = "Test"
y = eval(x)
```

* String to tuple
```python
x = "Test"
y = tuple(x)
# eaach string char will be an element of the tuple
```

* String to list
```python
x = "Test"
y = list(x)
# eaach string char will be an element of the list
```

* String to set
```python
x = "Test"
y = set(x)
# eaach string char will be an element of the set
```

* Tuple to Dict
```python
tuple=((1,'a'), (2,'b'))
dict(tuple)
{1: 'a', 2: 'b'}
```
* String to frozenset
```python
x = "Test"
y = frozenset(x)
# eaach string char will be an element of the set
```

* Object to regex
```python
x = "..."
y = repr(x)
```

* Int to char
```python
x = 10
c = char(x)
```

* Int to unicode
```python
x = 10
u = unichr(x)
```

* Int to hex
```python
x = 10
u = hex(x)
```

* Int to oct
```python
x = 10
u = oct(x)
```

* Single char to its integer value
```python
x = 'a'
o = ord(x)
```

* Object to regex
```python
x = "..."
y = repr(x)
```

### Operators

* '**': Exponetial power
* '//': Floor Division (5.0 // 2 >> 2.0)
* 'in': Both variables point to the same object (x is y >> true)
* 'not': 

### Statements

* **continue**: break the current iteration and move to the next
* **break**: stop the iterations
* **pass**: do nothing, it means you will code it later
* **lambda**: creates an anonymous function. ( x = lambda param : param + 10 >>> x(20) >>> 30 )

### Random values

* **choice**: Get a random value from a list (x = choice(list))
* **randrange(start,stop,step)**: Get a random from a range (random.randrange(100, 1000, 2))
* **random**: Get a random float number between 0 and 1
* **seed**: Specify a seed (random.seed(30))
* **shuffle**: Randomize a list (random.shuffle(list))

### Where python stores the functions

Stack memory

### Doble data type

Python has no double data type




