# General

Generics allow templating classes to specify types.

This is a list without generics:

```java
List list;
String s;

list = new ArrayList();

list.add("hello");

s = (String) list.get(0);
```

This is the same list, specifying it contains Strings:

```java
List<String> list;
String s;

list = new ArrayList<>();

list.add("hello");

s = list.get(0); // no casting
```

## More Information

* [Generics](https://docs.oracle.com/javase/tutorial/java/generics/index.html)

