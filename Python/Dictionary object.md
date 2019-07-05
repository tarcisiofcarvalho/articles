# Python - Dictionary object


#### The length of a dictionary

```python
my_dict = {'a':1,'b':2}

len(my_dict.keys())
```
Output >> 2

or 

```python
len(my_dict)
```
Output >> 2

#### Accessing dictionary members

First way:

```python
x = my_dict['a']
```

Second way:

```python
x = my_dict.get['a']
```

#### Iterate over a dictionary

First way, getting both keys (x) and values (y)

```python
for x, y in my_dict.items():
  print(x, y)
```

Second way, getting just values

```python
for x in my_dict.values():
  print(x)
```

Third way, getting the member object:

```python
for x in my_dict:
	print(x)
```