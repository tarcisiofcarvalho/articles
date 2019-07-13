# Java Object Oriented Programming

The object oriented programming has the objective to define the real world things as objects. Let's see it in detail:

### Object and Classes

An **object** has *state* (properties), *behavior* (methods) and *identity* (used by the JVM). A **class** is a template for objects, so an object an instance of a given class. A class can contain:

* Properties
* Methods
* Constructors
* Blocks
* Nested class and interface

Note: You can create anonymous objects, that has no reference, by just following the sample below:

```java
new Person();
```

it can be used when you need to construct this object just once and no methods should be called except the constructor itself.


### Inheritance

Inheritance is a mechanism one class (sub-class) extends the properties and behavior of another class (super class). The multiple Inheritance is not supported in Java, for example a given class A cant's extends from class B and class C, just one. However one super-class C can has more than one child.

### Polymorphism

The polymorphism can guve many forms to one single action. It is divided between compiled-time and runtime polymorphism. Let's see:

#### Overload

You overload a method when you create a new method with the same name and return type, but with different parameters. It increase the code readability.

```java
  public void getPerson(int id){};
  public void getPerson(String name){};
```

We can overload the main method in Java, but the JVM will call just the main method that accepts a string array.

Also, we can have a type promotion in the paremeters as example below:

```java
  public void getPerson(long id){}; // Long type parameter
```

```java
 Person person = organization.getPerson(30); // We are passing integer type that will be promoted to long
```

#### Override



### References
* https://www.javatpoint.com/
