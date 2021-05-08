An opinionated template for a Maven project that I feel is a good starting point for a new project. Obviously,
additional tweaking will probably be necessary. Notably, I've omitted any major framework such as Spring because there
are several valid alternatives (Quarkus, Micronaut, or no framework at all).

Includes:

 - [PMD](https://pmd.github.io/) for static analysis, and an opinionated configuration of its Java rules
 - [Checkstyle](https://checkstyle.sourceforge.io/) for consistent code style, configured to use
   [Google's style guide](https://google.github.io/styleguide/javaguide.html)
   - In practice, I think Google's rules can be improved upon, so I use a slightly customized rule set
 - [Jacoco](https://www.eclemma.org/jacoco/) for code coverage 
 - [Flatten plugin](https://www.mojohaus.org/flatten-maven-plugin/) for cleaning up POMs
 - [Enforcer plugin](https://maven.apache.org/enforcer/maven-enforcer-plugin/) to prevent mistakes in POMs

Dependencies included by default:

 - [Lombok](https://projectlombok.org/) to reduce boilerplate
 - [Junit](https://junit.org/) for unit tests
 - [Slf4j](http://www.slf4j.org/) as a logging facade. If you're writing an application, you will need a logging
   implementation ([Logback](http://logback.qos.ch/), [Log4j](https://logging.apache.org/log4j/2.x/), etc.)

## Now what?

If you're writing an application (as opposed to a library), you will probably want to choose some way to bundle your
application together with its dependencies, either as a [fat JAR](https://stackoverflow.com/questions/19150811/what-is-a-fat-jar)
(e.g. [Spring Boot Maven Plugin](https://docs.spring.io/spring-boot/docs/2.4.5/maven-plugin/reference/htmlsingle),
the [Maven Shade plugin](http://maven.apache.org/plugins/maven-shade-plugin/), or the
[Maven Assembly plugin](http://maven.apache.org/plugins/maven-assembly-plugin/)), or as a Docker image (e.g.
[with Spring Boot](https://spring.io/guides/gs/spring-boot-docker/)).

