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

#### Remove an element

```python
a = [1,2,3,4,5]

# remove the first matching element
a.remove(2) # Will remove the element with value 2

# remove using index
del a[1] # Will remove the element in the 1 index

# remove and bring the value
a.pop(1) # Remove the element in the specific index and return it
```

#### Comparing elements of two lists

Will return:
-1 if a<b

0 if a=b

1 if a>b
```python
cmp(a, b)
```

#### Get the index of an object in a list

```python
list.index(object)
```

#### Insert an object in a given index

```python
list.insert(index,object)
```

#### Reverse a list

```python
list.reverse()
```

#### Sort a list

```python
list.sort()
```
