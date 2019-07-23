# Java Environment

### Increase memory heap

You can increase the java heap memory when getting Out-of-Memory errors.

mx: Sets the maximum heap size that java will use for dynamically allocated objects and arrays to x

ms: Sets the startup size of the memory allocation pool (the Java heap) to x

```sh
java -ms64m -mx128m <class>
```

### References

https://people.cs.nctu.edu.tw/~chlo/web/docs/doc/data/java/4.htm
