# Java Collections

Collections overview

![](../images/collections.png)

Null and duplicated objects:
* Set: Unique objects, not null objects
* List: Duplicated objects, null objects
* Map: Not duplicated keys, duplicated values

Ordering:
* HashSet/HashMap: unordered
* LinkedHashSet/LinkedList/LinkedHashMap: insertion order
* TreeSet/TreeMap: ascending order

### HashMap

It belongs **java.util** and implements **HashTable** data structure.

* **put()**: Store the object into the backend array. The hashcode() method is used in conjunction with a hash function to find the correct location for the object into the bucket. If a collision occurs then the entry object which contains both key and value is added to a linked list and that linked list is stored into the bucket location

* **put()**: *The same key*, it will replace the old value by the new one, and return the old one

* **required object**: A HashMap object should have **equals()** (used in retrieve) and **hashcode()** (used in insert) methods.

* **removing an element on a transversing map**

```java
Iterator itr = map.entrySet().iterator();

while(itr.hasNext()){
  Map.Entry current = itr.next();

  if(current.getKey().equals("matching"){
     itr.remove(); // removing the current element, HasMap has .remove() but doesn't work in a iteration
  }
}
```

* **HashMap order**: Random order, it iteration will be a new order. You can't sort beacaus it is an unordered collection.

* **HashMap count**: size() ot mappingCount() in java8

* **HashMap collision**: if two keys have the same hashCode they will be stored in the same bucket

* **HashMap syncronized**: Collections.synchronizedMap(new HashMap<K,V>())

### Iteration

Some ways to iterate over a Map

![](../images/map_iteration.png)

* Using keySet and looping
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

### HashSet

It does not allow duplicate values and uses **add** method instead of **put** method. It uses **contain** method to check existence of an object, it is a unique list.

```java
HashSet<String> set= new HashSet<String>();
set.add ("first");
set.add ("second");
 
if(set.contains("first")){
	System.out.println("first found");
}
```

### Main difference between Hashtable and HashMap

Hashtable is legacy class and is syncronized, the HashMap should be prefered and it is not syncronized, you should implement sync if needed nby yourself.

### Remove duplicated objects from an ArrayList

Copy the **ArrayLit** to a **Set** that keeps the elements order as **LinkedHashSet**

```java
List<Integer> arrayList = new ArrayList<Integer>();
Set<Integer> set = new LinkedHashSet<Integer>(arrayList);
arrayList.clear();
arrayList.addAll(set);
```
### Reverse a List

You can use the java.util.Collections, reverse function. It's complexity of O(n):
```java
ArrayList<Integer> arrayList = new ArrayList<Integer>();

Collections.reverse(arrayList);
```

### Sort a List

```java
ArrayList<Integer> arrayList = new ArrayList<Integer>();
 
//Ascending order
Collections.sort(arrayList);
 
//Descending order
Collections.sort(arrayList, Collections.reverseOrder());
```

### Synchornized List

List interface is not synchronized, you can create the a List/ArrayList using the Collections.synchronizedList() and. synchronized()

```java
List list = Collections.synchronizedList(new ArrayList());

  synchronized(list) {
      Iterator i = list.iterator();
      while (i.hasNext())
          foo(i.next()); // Some action
 }
```

### Complexity in case a ArrayList resize

The normal complexity in an ArrayList search is O(n), but when this array list should be resized the complexity chasnges to O(log(n))

### ArrayList x LinkedList

In most of cases the ArrayList is a better choice than Linked list, except if you use much the **add** operation, so the complexity of LinkedList to add an element is less than ArrayList list that need to resize the array and the complexity changes to O(log(n))

### ArrayList x Vector

The main difference is that Vector is synchronized and thread-safe. See below Vector construction:

```java
// Creating a empty vector with size 10
Vector<Integer> vector1 = new Vector<Integer>(); 

// Creating a vector from a collection
Vector<Integer> vector1 = new Vector(Collection<? extends E>); 

// Creating a vector with specific size 15
Vector<Integer> vector1 = new Vector<Integer>(15); 

// Creating a vector with specific size 15 and increments of 2
Vector<Integer> vector1 = new Vector<Integer>(15,2); 

```

### Create an ArrayList from array in a simple way

```java
List<String> coolStringList = Arrays.asList("John", "Paul", "Loriee");
```

### ArrayList - sub array list

```java
List<String> list = arrayList.subList(1,5); // Sub array list from 1 to 5 position

```

### CopyOnWriteArrayList

It is a thread safe list with no synchronization needed. It is nit able to remove an element during an iterator loop.

```java
CopyOnWriteArrayList<String> list = new CopyOnWriteArrayList<String>();

```

### Removing Objects from a ArrayList

```java
list.remove("John"); // Object
list.remove(1); //Index

while(it.hasNext()){
	it.remove(); // Removing using iterator
}
```

### Creating a Read-only array list 

```java
ArrayList<String> list = Collections.unmodifiableCollection(new ArrayList<String>());
```
### References
https://javarevisited.blogspot.com/2011/12/how-to-traverse-or-loop-hashmap-in-java.html
http://www.javapractices.com/topic/TopicAction.do?Id=65
https://howtodoinjava.com/sort/collections-sort/
https://www.java67.com/2014/12/how-to-synchronize-arraylist-in-java.html

