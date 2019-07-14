### Thread-safe

When you have more than one thread accessing a resource that change something and this change can't be stopped, you need a thread-safe to avoid the thread B access the resource X when the thread A is accessing it. In order to setup thread-safe in this scenario we can use the "synchronized" keyword as below:

```java
public synchronized void processPayment(double amount){};
```

The synchronized will ensure that thread A will have the work requested done before the resource answers the thread B request.

### References

* https://www.devmedia.com.br/thread-safe-java-entendendo-o-conceito-e-usando-em-sua-aplicacao/28858
