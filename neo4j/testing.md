# Testing

## Test Harness

```markup
<dependency>
   <!-- Neo4j Test Harness -->
   <groupId>org.neo4j.test</groupId>
   <artifactId>neo4j-harness</artifactId>
   <version>${neo4j.test.version}</version>
   <scope>test</scope>
   <exclusions>
      <exclusion>
         <groupId>org.slf4j</groupId>
         <artifactId>slf4j-nop</artifactId>
      </exclusion>
   </exclusions>
</dependency>
```

```java
private static Neo4j embeddedDatabaseServer;

@BeforeAll
static void initializeNeo4j() {
    embeddedDatabaseServer = Neo4jBuilders.newInProcessBuilder()
            .withDisabledServer()// disable http server
            .withFixture("CREATE ({name: 'Source'});")
            .withFixture("CREATE ({name: 'Target'});")
            .withFixture(
                    "MATCH (n {name: 'Source'}), (m {name: 'Target'}) MERGE (n)-[:MENTIONS]->(m);")
            .build();
}

@DynamicPropertySource
static void neo4jProperties(final DynamicPropertyRegistry registry) {
    registry.add("spring.neo4j.uri", embeddedDatabaseServer::boltURI);
    registry.add("spring.neo4j.authentication.username", () -> "neo4j");
    registry.add("spring.neo4j.authentication.password", () -> null);
}

@AfterAll
static void stopNeo4j() {
    embeddedDatabaseServer.close();
}
```

