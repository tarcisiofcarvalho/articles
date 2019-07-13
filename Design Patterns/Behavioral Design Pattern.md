# Behavioral Design Pattern

The Behavioral Design Pattern deals with objects iteration and responsabilities

### Iterator Pattern

Provide a way to access the elements of an aggregate object sequentially without exposing its underlying representation. It's a way to iterate over a collection of data as a List accessing the objects in sequential way without coding much iterate control implementation.

```java
List<String> list = new ArrayList<String>();

list.add("Name A");
list.add("Name B");
list.add("Name C");
list.add("Name D");

Iterator it = list.iterator();

while(it.hasNext())
  System.out.println(it.next().toString()); // All names should be printed
```
