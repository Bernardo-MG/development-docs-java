# Gateway

The entry to an integration flow.

## Mapping a Service

```java
public interface EmployeeService {

   public Employee updateEmployee(final Employee employee);

}
```

```markup
<si:gateway id="employeeFlow"
  service-interface="com.service.EmployeeService "
  default-reply-channel="employeeOutputChannel">
  <si:method name="updateEmployee" request-channel="updateEmployeeChannel"/>
</si:gateway>
```

These operations may be extended with additional metadata:

```markup
<si:gateway id="employeeFlow"
  service-interface="com.service.EmployeeService "
  default-reply-channel="employeeOutputChannel">
  <si:method name="updateEmployee" request-channel="updateEmployeeChannel">
	 <si:header name="EVENT_TYPE" value="employeeChangeRequest" />
  </si:method>
</si:gateway>
```

