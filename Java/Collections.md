# Java Collections

(Under construction) Map, HasMap and TreeMap

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

### Iteration

Some ways to iterate over a Map

* Using foreach
```java
HashMap<String, String> loans = new HashMap<String, String>();
loans.put("home loan", "citibank");
loans.put("personal loan", "Wells Fargo");
for(String k : loans.keySet()){
  System.out.println("Key: " + k + " Value: " + loans.get(k));
}
```

* Using keySet and Iterator 
```java
Set<String> keySet = loans.keySet();
Iterator<String> it = keySet.iterator();
while(it.hasNext()){
  String k = it.next();
  System.out.println("Key: " + k + " Value: " + loans.get(k));
}
```

* Using EntrySet and looping 
```java
Set<Map.Entry<String,String>> entrySet = loans.entrySet();

for(Entry entry : entrySet){
  System.out.println("Key: " + entrySet.getKey() + " Value: " + entrySet.getValue());
}
```

* Using EntrySet and Iterator
```java
Set<Map.Entry<String,String>> entrySet = loans.entrySet();
Itertor<Entry<String,String>> it = entrySet.iterator();
while(it.hasNext()){
  String entry = it.next();
  System.out.println("Key: " + entrySet.getKey() + " Value: " + entrySet.getValue());
}
```

### References
https://javarevisited.blogspot.com/2011/12/how-to-traverse-or-loop-hashmap-in-java.html
