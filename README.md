An opinionated [Maven archetype](https://maven.apache.org/guides/introduction/introduction-to-archetypes.html)
that will create a Maven project that I feel is a good starting point for a new project. Obviously, additional tweaking
will probably be necessary. Notably, I've omitted any major framework such as Spring because there are several valid
alternatives (Quarkus, Micronaut, or no framework at all).

Includes:

 - [PMD](https://pmd.github.io/) for static analysis, and an opinionated configuration of its Java rules
 - [Checkstyle](https://checkstyle.sourceforge.io/) for consistent code style, configured to use
   [Google's style guide](https://google.github.io/styleguide/javaguide.html)
   - In practice, I think Google's rules can be improved upon, so I use a slightly customized rule set
 - [Jacoco](https://www.eclemma.org/jacoco/) for code coverage 
 - [Flatten plugin](https://www.mojohaus.org/flatten-maven-plugin/) for cleaning up POMs
 - [Enforcer plugin](https://maven.apache.org/enforcer/maven-enforcer-plugin/) to prevent mistakes in POMs
