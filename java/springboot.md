# Spring Boot
## Application Context
A Spring "container" is created at startup, and various Java Beans are registered with it (aka Spring Beans).
### Spring Beans
You register them with the `@bean` annotation. Then, dependencies can be auto-injected if they are also a bean (aka wiring).
