# Java Tips

* Constructor has no final method

* The subclasses have visibility of protected superclass even out of superclass package

* Wrapper class wraps int, float, boolean, etc

* The best way to implement a thread is implementing the Runnable interface

* The servlet is the java server side that provides dynamic components, it init() once, service() always, destroyed() once

* The **Request Dispatcher** is an interface that *forward* requests to other resources and *include* other resources in the response.

* **Java Applet** is designed to transmit the Java code over the internet using Java-Enabled Webbrowser

* **Numeric Promotion** is the promotion of small java primitive types to bigger ones. Example:
1. int to float and long
2. byte, char, short to int
3. long and float to double

* **False sharing** occurs in multi-threading with multi-core system. The processors share the same memory cache, and when one thread change the line in memory cache, the other thread will be impacted.







