# Table of contents

* [Introduction](README.md)

## General

* [Compiling and running](general/compiling-and-running.md)
* [Code Style](general/code-style.md)
* [Operators](general/operators.md)
* [Control Flow](general/control-flow.md)
* [Inheritance](general/inheritance.md)
* [Enums](general/enums.md)
* [Manifest](general/manifest.md)
* [Immutable and Unmodifiable](general/immutable-and-unmodifiable.md)
* [Regular Expression](general/regular-expression.md)
* [Executable class](general/executable-class.md)

## Beans and Objects <a id="beans"></a>

* [Primitives](beans/primitives.md)
* [Variables](beans/variables.md)
* [Java Beans](beans/java-beans.md)
* [Serialization](beans/serialization.md)
* [Hashcode, equals and toString](beans/hashcode-equals-and-tostring.md)

## Generics

* [General](generics/general.md)
* [Generic Methods](generics/generic-methods.md)
* [Bound Parameters](generics/concrete-generics.md)
* [Wildcards](generics/wildcards.md)
* [Type Erasure](generics/type-erasure.md)
* [Type Parameter Naming Conventions](generics/type-parameter-naming-conventions.md)

## Documentation

* [Comments](documentation/comments.md)
* [Javadoc](documentation/javadoc/README.md)
  * [Code Example](documentation/javadoc/code-example.md)

## Collections and Data Structures <a id="collections"></a>

* [Arrays](collections/arrays.md)
* [Iterable](collections/iterable.md)
* [Collection](collections/collection.md)
* [List](collections/list.md)
* [Set](collections/set.md)
* [Queue](collections/queue.md)
* [Stack](collections/stack.md)
* [Map](collections/map.md)

## Introspection

* [Properties](introspection/acquiring-methods.md)

## Errors and Exceptions

* [General](errors-and-exceptions/general.md)
* [Catching Exceptions](errors-and-exceptions/catching-exceptions.md)
* [Checked Exceptions](errors-and-exceptions/checked-exceptions.md)

## Functional

* [General](functional/general.md)
* [Interfaces](functional/interfaces.md)
* [Function](functional/function.md)
* [Predicate](functional/predicate.md)
* [Consumer](functional/consumer.md)
* [Supplier](functional/supplier.md)
* [Method References](functional/method-references.md)
* [Lambdas](functional/lambdas.md)
* [Streams](functional/streams/README.md)
  * [Common Operations](functional/streams/common-operations.md)
  * [Searching for Values](functional/streams/searching-for-values.md)
  * [Other Operations](functional/streams/other-operations.md)
  * [Data Structure Transformations](functional/streams/data-structure-transformations.md)

## Internationalization

* [General](internationalization/general.md)
* [Locale](internationalization/locale.md)
* [Resource Bundle](internationalization/resource-bundle.md)
* [Formatting](internationalization/formatting.md)

## Java Bean Validation

* [Specification](java-bean-validation/specification.md)
* [Annotations](java-bean-validation/annotations.md)
* [Validator](java-bean-validation/validator.md)

## Utilities Classes

* [Libraries](utilities-classes/libraries.md)
* [Constants Class](utilities-classes/constants-class.md)
* [Apache Commons](utilities-classes/apache-commons/README.md)
  * [Strings](utilities-classes/apache-commons/strings.md)
  * [Dates](utilities-classes/apache-commons/dates.md)
* [Guava](utilities-classes/guava/README.md)
  * [Preconditions](utilities-classes/guava/preconditions.md)

## JPA

* [General](jpa/general.md)
* [JPA Entities](jpa/jpa-entities.md)
* [Lifecycle](jpa/lifecycle.md)
* [JPQL](jpa/jpql.md)
* [Criteria API](jpa/criteria-api.md)

## Ant

* [Scripts](ant/scripts.md)
* [Examples](ant/examples/README.md)
  * [Replace Version](ant/examples/replace-version.md)
  * [Merge Files](ant/examples/merge-files.md)
  * [Execute Command](ant/examples/execute-command.md)

## LOGGING <a id="logging-in-java"></a>

* [SL4J](logging-in-java/sl4j.md)
* [Log4j](logging-in-java/log4j/README.md)
  * [Logging Levels](logging-in-java/log4j/logging-levels.md)
  * [Formatted Messages](logging-in-java/log4j/formatted-messages.md)
  * [Templated Messages](logging-in-java/log4j/templated-messages.md)
  * [Mapped Diagnostic Context](logging-in-java/log4j/mapped-diagnostic-context.md)
* [JPA](logging-in-java/jpa.md)
* [Hikari](logging-in-java/hikari.md)

## Testing

* [Libraries](testing/libraries.md)
* [Junit](testing/junit/README.md)
  * [Setting Up Tests](testing/junit/setting-up-tests/README.md)
    * [JUnit 4 Tests](testing/junit/setting-up-tests/junit-4-tests.md)
    * [JUnit 5 Tests](testing/junit/setting-up-tests/junit-5-tests.md)
  * [Disable Tests](testing/junit/disable-tests.md)
  * [Test Lifecycle](testing/junit/test-lifecycle.md)
  * [Testing Exceptions](testing/junit/testing-exceptions.md)
  * [Display Name](testing/junit/display-name.md)
  * [Test Files](testing/junit/test-files.md)
* [Mockito](testing/mockito/README.md)
  * [Mocking](testing/mockito/mocking.md)
  * [Verify Calls](testing/mockito/verify-calls.md)
  * [Throw Exceptions](testing/mockito/throw-exceptions.md)
  * [Capture Arguments](testing/mockito/capture-arguments.md)

## KeyStore

* [Types](keystore/types.md)
* [Generation](keystore/generation.md)
* [Certificates](keystore/certificates.md)
* [Keys](keystore/keys.md)
* [Reading](keystore/listing.md)

## HIBERNATE

* [Logging](hibernate/logging/README.md)
  * [Sessions](hibernate/logging/sessions.md)
  * [Statistics](hibernate/logging/statistics.md)
  * [Queries](hibernate/logging/queries.md)
* [More Information](hibernate/more-information.md)

## Jackson

* [General](jackson/general.md)
* [Deserialize](jackson/deserialize/README.md)
  * [Dates](jackson/deserialize/dates.md)
  * [Enums](jackson/deserialize/enums.md)
* [Object Hierarchy](jackson/object-hierarchy.md)
* [Ignoring Data](jackson/ignoring-data.md)
* [Change Field Name](jackson/change-field-name.md)
* [Mixin](jackson/mixin.md)

## Maven

* [Execution](maven/execution/README.md)
  * [Commands](maven/execution/commands.md)
  * [Parameters](maven/execution/parameters.md)
  * [Building the Project](maven/execution/building-the-project.md)
* [Deployments](maven/deployments/README.md)
  * [Configuration](maven/deployments/configuration.md)
  * [Deploying Web Projects Locally](maven/deployments/deploying-web-projects-locally.md)
  * [Deploying Documentation](maven/deployments/deploying-documentation.md)
* [Tests](maven/tests/README.md)
  * [Deploying the WAR for Testing](maven/tests/deploying-the-war-for-testing.md)
* [Site](maven/site/README.md)
  * [Setting Up](maven/site/setting-up.md)
  * [Reports](maven/site/reports.md)
  * [Theme](maven/site/theme.md)
* [Maven Lifecycle](maven/maven-lifecycle/README.md)
  * [Binding Plugins to Phases](maven/maven-lifecycle/binding-plugins-to-phases.md)
* [Dependency Management](maven/dependency-management/README.md)
  * [Artifact Repositories](maven/dependency-management/artifact-repositories.md)
* [Maven Archetype](maven/maven-archetype/README.md)
  * [Testing Archetypes](maven/maven-archetype/testing-archetypes.md)
* [Configuration](maven/configuration/README.md)
  * [Project Setup](maven/configuration/project-setup.md)
  * [Maven Build Plugins](maven/configuration/maven-build-plugins.md)
  * [Profiles](maven/configuration/profiles/README.md)
    * [Forcing an Active Profile](maven/configuration/profiles/default-profile.md)
  * [Default Properties](maven/configuration/default-properties.md)
  * [Parent POM](maven/configuration/parent-pom.md)
  * [Settings File](maven/configuration/settings-file.md)
  * [Versions](maven/configuration/versions.md)
  * [Extensions](maven/configuration/extensions.md)
  * [Setting Up the JAR](maven/configuration/setting-up-the-jar/README.md)
    * [Attach Sources](maven/configuration/setting-up-the-jar/attach-sources.md)
    * [Attach Javadocs](maven/configuration/setting-up-the-jar/attach-javadocs.md)
    * [Manifest](maven/configuration/setting-up-the-jar/manifest.md)
* [JPA](maven/jpa/README.md)
  * [Generating Metamodel](maven/jpa/generating-metamodel.md)
* [Frontend with Maven](maven/frontend-with-maven/README.md)
  * [WebJars](maven/frontend-with-maven/webjars.md)
  * [npm and Webpack](maven/frontend-with-maven/npm-and-webpack.md)
* [Continuous Integration](maven/continuous-integration.md)
* [Ant](maven/ant.md)
* [Executable JAR](maven/executable-jar.md)

## Spring

* [General](spring/general.md)
* [SpEL](spring/spel.md)
* [Files](spring/files.md)
* [Sending Mails](spring/sending-mails.md)

## Spring Configuration

* [Profiles](spring-configuration/profiles.md)
* [Conditional Configuration](spring-configuration/conditional-configuration.md)
* [Properties Object](spring-configuration/properties-object.md)

## Spring Dependence Injection

* [Injections](spring-dependence-injection/injections/README.md)
  * [Asking for a Specific Bean](spring-dependence-injection/injections/asking-for-a-specific-bean.md)
* [Injecting Values](spring-dependence-injection/injecting-values.md)
* [Injecting Multiple Instances](spring-dependence-injection/injecting-multiple-instances.md)
* [Interdependence](spring-dependence-injection/interdependence.md)
* [Component Scanning](spring-dependence-injection/component-scanning.md)

## Spring Beans

* [Initialization](spring-beans/initialization.md)
* [Destruction](spring-beans/initialization-and-destruction.md)
* [Extending Initialization](spring-beans/extending-initialization.md)

## Spring Data

* [Configuration](spring-data/components-and-configuration/README.md)
  * [Common Persistence Beans](spring-data/components-and-configuration/common-persistence-beans.md)
  * [Datasource](spring-data/components-and-configuration/datasource.md)
  * [Persistence Providers](spring-data/components-and-configuration/persistence-providers.md)
* [Repositories](spring-data/jpa-repositories/README.md)
  * [Custom Repositories](spring-data/jpa-repositories/custom-repositories.md)
  * [Queries](spring-data/jpa-repositories/queries.md)
  * [Sorting and Paging](spring-data/jpa-repositories/sorting-and-paging.md)
  * [Example API](spring-data/jpa-repositories/example-api.md)
* [Transactional](spring-data/transactional/README.md)
  * [Configuration](spring-data/transactional/configuration.md)
  * [Annotation](spring-data/transactional/annotation.md)
  * [Transaction Aspect](spring-data/transactional/transaction-aspect.md)
  * [Transactional Test](spring-data/transactional/transactional-test.md)

## Spring MVC

* [General](spring-mvc/general.md)
* [Setting Up a Web Application](spring-mvc/setting-up-a-web-application.md)
* [Serving Resources](spring-mvc/serving-resources.md)
* [Securing URLS](spring-mvc/securing-urls.md)
* [Controllers](spring-mvc/controllers/README.md)
  * [Mapping and Choosing Controller Methods](spring-mvc/controllers/mapping-and-choosing-controller-methods.md)
  * [Mapping Controller Variables](spring-mvc/controllers/mapping-controller-variables.md)
  * [Request Argument Validation](spring-mvc/controllers/request-argument-validation.md)
  * [Controller Advices](spring-mvc/controllers/controller-advices.md)
* [Error Handling](spring-mvc/error-handling.md)
* [Binding Configuration](spring-mvc/binding-configuration.md)
* [Model Attributes](spring-mvc/model-attributes.md)
* [View Resolvers](spring-mvc/view-resolvers.md)
* [Resolving Sort and Pageable Arguments](spring-mvc/loading-pageable-automatically.md)
* [Logging](spring-mvc/logging.md)
* [Validating Request Data](spring-mvc/validating-request-data.md)

## Spring WS

* [Examples](spring-ws/examples.md)

## Spring Boot

* [General](spring-boot/general.md)
* [Setting Up](spring-boot/setting-up.md)

## Spring Security

* [Examples](spring-security/examples.md)
* [Setting Up](spring-security/setting-up/README.md)
  * [Method Security](spring-security/setting-up/method-security.md)

## Spring AOP

* [More Information](spring-aop/more-information.md)
* [Configuration](spring-aop/configuration.md)
* [Aspect](spring-aop/aspect.md)
* [Logging Aspect Example](spring-aop/logging-aspect-example.md)

## Spring Cache

* [Configuration](spring-cache/configuration.md)

## Spring Integration

* [Gateway](spring-integration/gateway.md)
* [Routing](spring-integration/routing.md)
* [Services](spring-integration/services.md)

## Testing Spring

* [Test configuration](testing-spring/test-configuration.md)
* [Setting Up Junit](testing-spring/dependencies-with-spring.md)
* [Conditional Tests](testing-spring/conditional-tests.md)
* [Initializing DB](testing-spring/initializing-db.md)
* [Spring MVC](testing-spring/testing/README.md)
  * [Setting Up the MVC Test Context](testing-spring/testing/preparing-a-controller-for-testing-requests.md)
  * [Request Path Testing](testing-spring/testing/request-path-testing.md)
  * [Testing JSON](testing-spring/testing/testing-json.md)
  * [Argument Resolvers](testing-spring/testing/argument-resolvers.md)
  * [Response Status](testing-spring/testing/response-status.md)

## JMeter

* [General](jmeter/general.md)

## Neo4J

* [More Information](neo4j/more-information.md)
* [Cypher](neo4j/cypher.md)

## JQAssistant

* [More Information](jqassistant/more-information.md)
* [Maven Plugin](jqassistant/maven-plugin/README.md)
  * [Git](jqassistant/maven-plugin/git.md)
  * [Maven Dependencies](jqassistant/maven-plugin/maven-dependencies.md)
* [Queries](jqassistant/queries/README.md)
  * [Structure](jqassistant/queries/structure.md)
  * [Pruning](jqassistant/queries/pruning.md)
  * [Maven](jqassistant/queries/maven.md)
  * [Controller](jqassistant/queries/controller.md)
  * [Detecting Problems](jqassistant/queries/detecting-problems.md)
* [Concepts](jqassistant/concepts.md)
* [Constraints](jqassistant/constraints.md)
* [Groups](jqassistant/groups.md)
* [Rules](jqassistant/rules/README.md)
  * [Custom Rules](jqassistant/rules/custom-rules.md)

## AspectJ

* [Wrapping Method](aspectj/wrapping-method.md)

