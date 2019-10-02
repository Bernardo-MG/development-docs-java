# Transactional

Transactionality can be marked by using the @Transactional annotation. Note that there is a JPA annotation of the same name, but we are using the Spring one.

## Aspects and Final

Transactionality is handled through aspects and the cglib library, which means that transactional classes and methods can't be final.



