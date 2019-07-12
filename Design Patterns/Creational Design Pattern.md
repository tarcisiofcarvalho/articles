# Creational Design Pattern

(It is under construction)

The creational design pattern provides a way to **create object** in a good way, avoiding to instantiate them directly using **new** keyword as example.

Please see below main creational design pattern.

### Factory Method Pattern

In general the factory patterns abstracts the the objects instantiation process. The factory method pattern itself, defines that the responsability to create an object should be given to the subclasses, than they will decide which class to instantiate. 

This pattern promotes the loose-coupling, by eliminates the need to bind a specific class.

See an example below:

*   Payment class
```java
abstract class Payment{

  protect double value;
  
  abstract double getValue();
 
}
```

*   CreditCard class
```java

public class CreditCard extends Payment{

  @Override
  public double getValue(){
    return value;
  }
}
```

*   Cash class
```java

public class Cash extends Payment{

  @Override
  public double getValue(){
    return value;
  }
}
```

*   GetPaymentFactory class
```java

public class GetPaymentFactory{

  public Payment getPayment(String paymentType){
    if(paymentType.equals("crediCard")
      return new CreditCard();
    
    if(paymentType.equals("cash")
      return new Cash();
    
    return null;
    
  }
}
````

If you instantiate the **GetPaymentFactory** class and call the method to **getPayment** passing the string argument "creditCard" or "cash" this method will instantiate the proper class, and decision will be later bind.

### Abstract Factory Pattern

The abstract factory pattern define an interface or abstract classes in order to group objects by family, without concern about what will be the subclasses. It delegates the object instantiation to another objects via composition, that differs from Factory Method Pattern delegate this role to the subclasses. Also, the Abstract Factory Pattern is known as factory of factories. See example below:

*   Lets create **Car** as an interface for the familiy of cars
```java
public interface Car{
  String getColor();
}
```

*   Lets create Ferrari class as a car
```java
public Ferrari implements Car{
  @Override
  public getColor(){
    return "Red";
  }
}
```

*   Lets create Porsche class as a car
```java
public Porsche implements Car{
  @Override
  public getColor(){
    return "Blue";
  }
}
```

*   The Abstract Factory Class
```java
public abstract class AbstractFactory{
  abstract Car getCar(String name);
}
```

*   The car factory
```java
public class CarFactory extends AbstractFactory{
  @Override
  public Car getCar(String name){
    if(name.equals("Ferrari")
      return new Ferrari();

    if(name.equals("Porsche")
      return new Porsche();
      
    return null;
  }
}
```

### Singleton Pattern

The Singleton Pattern deals with a single object, that is instantiate just once and can be used in overall application. The common use of this pattern is in logging, database, connections objects where you can avoid to create many instances of an object and need to keep the control as well.

*   Single Object
```java
public class SingleObject{
	
	private static SingleObject instance = new SingleObject();
	private SingleObject(){}
	
	public static SingleObjectc getInstance(){
		return instance;
	}
	
}
```
Notice that it hasn't a public constructor, so it will be instantiated once in earlier bind and can be called by the **getInstance** method.

To access the object you should use the command below that won't deal with "new" keyword, just get the object already instantiated

```java
  SingleObject object = SingleObject.getInstance();
```

### Prototype Pattern

The Prototype Pattern proposes to *clone* an object instead of instantiating a new when the the costs to instantiate is more expensive than to clone it.

*	Lets create a class "Sheep" that can be clone, take a look in the override method *clone* and the implementation of *Clonable* interface
```java
public class Sheep implements Clonable{
	
	private String name;
	
	public String getName(){
		return this.name;
	}
	
	public Sheep(String name) { 
		this.name = name; 
	}
	
	@Override
	public Sheep clone() throws CloneNotSupportedException{
		return new Sheep(name);
	}
}
```
* You can call this clone in this way:

```java
// The first object instantiation
Sheep first = new Sheep("First Sheep");
	
// It will be a new object cloned from the "first"
Sheep cloned = first.clone(); 
```
### Builder Pattern

### References

http://www.buyya.com/254/Patterns/Factory-2pp.pdf
https://www.javatpoint.com/abstract-factory-pattern
https://www.tutorialspoint.com/design_pattern/abstract_factory_pattern.htm
