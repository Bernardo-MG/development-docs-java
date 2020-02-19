# Preparing a Controller for Testing Requests

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

