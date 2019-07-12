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

### Prototype Pattern

### Builder Pattern
