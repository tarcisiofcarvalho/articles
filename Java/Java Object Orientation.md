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

When a subclass provides a specific implementation method that has been declared in the super-class, it is the override. The override method should have the **same name** and the **same parameters** just the behavior will be changed. Take a look:

```java
public class Employee{

  // It is the super class
  private double salary;
  
  public void setSalary(double salary){
    this.salary = salary; 
  }
}

public class Contractor extends Employee{

  // It is the sub class
  private double salary;
  
  public void setSalary(double salary){
    this.salary = salary * 0.85; // Fifteen percent of salary discount 
  }
}
```
#### Runtime polymorphism

The runtime polymorphism uses the concept of upcasing where a reference declaration a class B uses its super class A. take a look:

```java
// It is the super class
public class A{

  void methodX(){};
}

// It is the sub class
public class B extends A{

  void methodX(){
    System.out.println("Method overridden at runtime");
  }
}

// Upcasting example class
public class{

  A temp = new B(); // It is the upcasting
  temp.methodX(); 

}
```
Since the temp refers to the subclass object and subclass method overrides the Parent class method, the subclass method is invoked at runtime, so Runtime polymorphism.

### Abstraction

Abstract hides the implementation and deal just with the functionalities. You can abstract a class from 0 to 100% using **class abstrac** or 100% using **interface**

An abstract class can't be instantiated, it can have contructor and static methods, and final modifiers to force subclasses not override it.

### Encapsulation

Encapsulation hides the data using the private properties from a class, as a Java Bean model that follow getter and setters standard. See below a sample of encapsulation:

```java
public class Person{
  private String name;

  public void setName(String name){
    this.name = name; // Here the "name" is encapsulated, you can do any validation before setting the name for example
  }
  
  public String getName(){
    return this.name; // Here the "name" is encapsulated, so you can perform any action here before to return the name
  }
  
}
```


### References
* https://www.javatpoint.com/
