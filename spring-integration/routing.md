# Routing

## Header Value

```markup
<si:header-value-router input-channel="employeeChannel" header-name="EVENT_TYPE">
  <si:mapping value="employeeChangeRequest" channel="employeeChangeChannel" />
  <si:mapping value="employeeDeleteRequest" channel="employeeDeleteChannel" />
</si:header-value-router>
```

## Custom

```java
public class EmployeeRouter
{

   public EmployeeRouter()
   {
      super();
   }

   @Override
   @Router
   public final String route(final Employee employee)
   {
      final String channel;

      // Set channel name

      return channel;
   }

}
```

The router should be initialized into the Spring context.

```markup
<si:router input-channel="employeeChannel"
   ref="employeeRouter" />
```

