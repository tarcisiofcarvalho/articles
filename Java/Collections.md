# Java Collections

(Under construction)

### HashMap

It belongs **java.util** and implements **HashTable** data structure.

* **put()**: Store the object into the backend array. The hashcode() method is used in conjunction with a hash function to find the correct location for the object into the bucket. If a collision occurs then the entry object which contains both key and value is added to a linked list and that linked list is stored into the bucket location

* **put()**: *The same key*, it will replace the old value by the new one, and return the old one

* **required object**: A HashMap object should have **equals()** (used in retrieve) and **hashcode()** (used in insert) methods.

* **removing an element**

```java
Iterator itr = map.entrySet().iterator();

while(itr.hasNext()){
  Map.Entry current = itr.next();

  if(current.getKey().equals("matching"){
     itr.remove(); // removing the current element
  }
}
```
