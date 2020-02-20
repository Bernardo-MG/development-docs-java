# Setting Up the MVC Test Context

Notice that the builders generate the MVC context with the build\(\) method.

## Mocking from a Controller

```java
private final UserController getController() {
	final UserService service; // Mocked service

	service = Mockito.mock(UserService.class);

	return new UserController(service);
}
```

```java
mockMvc = MockMvcBuilders.standaloneSetup(getController()).build();
```

## Mocking from Application Context

```java
@Resource
private WebApplicationContext webApplicationContext;
```

```java
mockMvc = MockMvcBuilders.webAppContextSetup(webApplicationContext).build();
```

