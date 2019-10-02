# Table of contents

* [Introduction](README.md)

## General

* [Compiling and running](general/compiling-and-running.md)
* [Code Style](general/code-style.md)
* [Comments](general/comments.md)
* [Javadoc](general/javadoc.md)
* [Variables](general/variables.md)
* [Primitives](general/primitives.md)
* [Arrays](general/arrays.md)
* [Operators](general/operators.md)
* [Control Flow](general/control-flow.md)
* [Inheritance](general/inheritance.md)
* [Generics](general/generics.md)
* [Enums](general/enums.md)
* [Serialization](general/serialization.md)
* [Manifest](general/manifest.md)
* [Java Beans](general/java-beans.md)
* [Immutable and Unmodifiable](general/immutable-and-unmodifiable.md)
* [Regular Expression](general/regular-expression.md)

## Errors and Exceptions

* [General](errors-and-exceptions/general.md)
* [Catching Exceptions](errors-and-exceptions/catching-exceptions.md)
* [Checked Exceptions](errors-and-exceptions/checked-exceptions.md)

## Collections

* [Iterable](collections/iterable.md)
* [Collection](collections/collection.md)
* [List](collections/list.md)
* [Set](collections/set.md)
* [Queue](collections/queue.md)
* [Stack](collections/stack.md)
* [Map](collections/map.md)

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

## Beans

* [Hashcode, equals and toString](beans/hashcode-equals-and-tostring.md)

## Java Bean Validation

* [Specification](java-bean-validation/specification.md)
* [Annotations](java-bean-validation/annotations.md)
* [Validator](java-bean-validation/validator.md)

## JPA

* [General](jpa/general.md)
* [JPA Entities](jpa/jpa-entities.md)
* [Lifecycle](jpa/lifecycle.md)
* [JPQL](jpa/jpql.md)
* [Criteria API](jpa/criteria-api.md)

## Utilities Classes

* [Libraries](utilities-classes/libraries.md)
* [Constants Class](utilities-classes/constants-class.md)

## Preconditions

* [Guava](preconditions/guava.md)

## Testing

* [Libraries](testing/libraries.md)
* [Junit](testing/junit/README.md)
  * [Setting Up Tests](testing/junit/setting-up-tests.md)
  * [Disable Tests](testing/junit/disable-tests.md)
  * [Test Lifecycle](testing/junit/test-lifecycle.md)
  * [Testing Exceptions](testing/junit/testing-exceptions.md)
  * [Dependencies with Spring](testing/junit/dependencies-with-spring.md)
* [Mockito](testing/mockito/README.md)
  * [Mocking](testing/mockito/mocking.md)
  * [Verify Calls](testing/mockito/verify-calls.md)
  * [Capture Arguments](testing/mockito/capture-arguments.md)

## LOGGING <a id="logging-in-java"></a>

* [Log4j](logging-in-java/log4j.md)
* [SL4J](logging-in-java/sl4j.md)
* [JPA](logging-in-java/jpa.md)
* [Hikari](logging-in-java/hikari.md)

## HIBERNATE

* [Logging](hibernate/logging.md)
* [More Information](hibernate/more-information.md)

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

* [Injections](spring-dependence-injection/injections.md)
* [Injecting Values](spring-dependence-injection/injecting-values.md)
* [Injecting Multiple Instances](spring-dependence-injection/injecting-multiple-instances.md)
* [Interdependence](spring-dependence-injection/interdependence.md)

## Spring Beans

* [Initialization and Destruction](spring-beans/initialization-and-destruction.md)
* [Extending Initialization](spring-beans/extending-initialization.md)

## Spring Data

* [Transactional](spring-data/transactional/README.md)
  * [Transaction Aspect](spring-data/transactional/transaction-aspect.md)
  * [Transactional Test](spring-data/transactional/transactional-test.md)
* [JPA Repositories](spring-data/jpa-repositories/README.md)
  * [Custom Repositories](spring-data/jpa-repositories/custom-repositories.md)
  * [Configuration](spring-data/jpa-repositories/configuration.md)
  * [Queries](spring-data/jpa-repositories/queries.md)
  * [Sorting and Paging](spring-data/jpa-repositories/sorting-and-paging.md)
  * [Example API](spring-data/jpa-repositories/example-api.md)
* [Components and Configuration](spring-data/components-and-configuration/README.md)
  * [Common Persistence Beans](spring-data/components-and-configuration/common-persistence-beans.md)
  * [Datasource](spring-data/components-and-configuration/datasource.md)
  * [Persistence Providers](spring-data/components-and-configuration/persistence-providers.md)

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
* [Loading Pageable Automatically](spring-mvc/loading-pageable-automatically.md)
* [Testing](spring-mvc/testing/README.md)
  * [Request Path Testing](spring-mvc/testing/request-path-testing.md)
  * [Testing JSON](spring-mvc/testing/testing-json.md)
  * [Argument Resolvers](spring-mvc/testing/argument-resolvers.md)

## Spring WS

* [Examples](spring-ws/examples.md)

## Spring Boot

* [General](spring-boot/general.md)
* [Setting Up](spring-boot/setting-up.md)

## Spring Security

* [Examples](spring-security/examples.md)
* [Setting Up](spring-security/setting-up.md)

## Spring AOP

* [Configuration](spring-aop/configuration.md)
* [Logging Aspect Example](spring-aop/logging-aspect-example.md)

## Testing Spring

* [Conditional Tests](testing-spring/conditional-tests.md)
* [Initializing DB](testing-spring/initializing-db.md)

