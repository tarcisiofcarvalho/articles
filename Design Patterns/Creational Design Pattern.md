# Creational Design Pattern

(It is under construction)

The creational design pattern provides a way to **create object** in a good way, avoiding to instantiate them directly using **new** keyword as example.

Please see below main creational design pattern.

### Factory Method Pattern

The Factory Pattern defines that the responsability to create an object should be given to the subclasses, that will decide which class to instantiate. 

This pattern promotes the loose-coupling, by eliminates the need to bind a specific class.

As example, thinking in a object model to deal with database entities, we can have an abstract class **Entity** and two classes Employee and Organization, and a classe GetEntityFactory. See below:

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

### Singleton Pattern

### Prototype Pattern

### Builder Pattern
