# General

Generics allow templating classes to specify types.

This is a list without generics:

```java
List list = new ArrayList();
list.add("hello");
String s = (String) list.get(0);
```

This is the same list, specifying it contains Strings:

```java
List<String> list = new ArrayList<String>();
list.add("hello");
String s = list.get(0); // no cast
```

### Diamond Operator

Since Java 7 the type can be implicit:

```java
List<String> list = new ArrayList<>();
```

## More Information

* [Generics](https://docs.oracle.com/javase/tutorial/java/generics/index.html)

