# Test Files

## JUnit 4

The TemporaryFolder rule allows creating testing folders.

```java
@Rule
public TemporaryFolder folder = new TemporaryFolder();
```

```java
file = folder.newFile("/file.txt");
```

## JUnit 5

The TempDir annotation initializes a testing folder.

```java
@TempDir
public static File folder;
```

Which can be used for creating test files:

```java
file = new File(folder, "/file.txt");
```

