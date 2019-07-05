# Python - List object


#### The length of a list

```python
list = [1,2,3,4,5]

print len(list)

5

```


#### Slice - Replace all elements of a list

You can replace all list elements without creating a new one, using slice as below:

```python
myList = [1,2,3,4,5]

myList[:] = [1,2,3]
````

#### Shallow list copy

You can create a shallow list copy, as a new memory object

```python
myList = [1,2,3]
b = myList[:]
b is myList

False
```

#### Clear a list

In Python < 3.2:

```python
del my_list[:]
```

in Python > 3.2:

```python
my_list.clear()
```