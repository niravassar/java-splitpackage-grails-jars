## Summary

This project is a java 9 project where you can dump grails jars in the lib folder and run
`gradlew java9c`. It will spit out the split packages that are in multiple jars. When using modules in Java 9 +, this will throw
an error in compilation if using module-path.

Using this project we can analyze the packages that are split and design for refactoring. FOr example, I just took
all the libs from the dist grails directory and placed them in the lib

This uses the gradle plugin:

https://github.com/jonnyzzz/gradle-java9c

## Gradle 5 and Java 11

If this project is upgraded to use JAVA_HOME for Java 11 and also to use Gradle 5, this gradle-java9c plugin is shown to work.

https://docs.gradle.org/current/userguide/gradle_wrapper.html#sec:upgrading_wrapper

- use `gradlew wrapper --gradle-version 5.0`
- change JAVA_HOME to jdk 11
