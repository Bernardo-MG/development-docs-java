# Deploying Web Projects Locally

Maven can deploy web applications locally by using plugins.

First of all define a property for the deployment context:

```markup
<properties>
   <server.path>/webproject</server.path>
</properties>
```

This will be used to deploy the project into the [http://localhost:8080/webproject/](http://localhost:8080/webproject/) URL.

### Jetty

When using the [Jetty plugin](https://www.eclipse.org/jetty/documentation/current/jetty-maven-plugin.html) with Maven use this configuration:

```markup
<plugin>
   <!-- Jetty -->
   <groupId>org.eclipse.jetty</groupId>
   <artifactId>jetty-maven-plugin</artifactId>
   <version>${plugin.jetty.version}</version>
   <configuration>
      <stopKey>STOP</stopKey>
      <stopPort>9999</stopPort>
      <stopWait>5</stopWait>
      <webApp>
         <contextPath>${server.path}</contextPath>
      </webApp>
   </configuration>
</plugin>
```

Afterwards it can be run with:

```bash
mvn jetty:run
```

### Tomcat

When using the [Tomcat plugin](http://tomcat.apache.org/maven-plugin-2.0/tomcat7-maven-plugin/) with Maven use this configuration:

```markup
<plugin>
   <!-- Tomcat 7 -->
   <groupId>org.apache.tomcat.maven</groupId>
   <artifactId>tomcat7-maven-plugin</artifactId>
   <version>${plugin.tomcat7.version}</version>
   <configuration>
      <path>${server.path}</path>
   </configuration>
</plugin>
```

Afterwards it can be run with:

```markup
mvn tomcat7:run-war
```

