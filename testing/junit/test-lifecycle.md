# Test Lifecycle

Methods can be annotated so they will be called at specific points on the test lifecycle.

## JUnit 4

* AfterClass
* After
* BeforeClass
* Before

### Initializing Data

```java
public class TestSuite {

    @Before
    public final void setUpData() {
        // Loads tests data
    }

}
```

## JUnit 5

* AfterAll
* AfterEach
* BeforeAll
* BeforeEach

### Initializing Data

```java
@RunWith(JUnitPlatform.class)
public class TestSuite {

    @BeforeEach
    public final void setUpData() {
        // Loads tests data
    }

}
```

