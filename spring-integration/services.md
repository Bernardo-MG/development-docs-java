# Services

## Activator

Maps a channel to a method, sending the channel's content as argument.

```java
public interface EmployeeService {

   public Employee update(final Employee employee);

}
```

An instance of the service should be initialized into Spring's context.

```markup
<si:service-activator
   input-channel="updateEmployeeChannel"
   output-channel="employeeOutputChannel"
   ref="employeeService" method="update">
</si:service-activator>
```

## Header Fields as Arguments

```java
public interface EmployeeService {

   public Employee update(final Employee employee,
      @Header(value = "EVENT_TYPE") final String event);

}
```

