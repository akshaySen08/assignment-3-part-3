# assignment-3-part-3
Internet Computing Assignment 3 Part 3


What Is JUnit?
JUnit is a Java unit testing framework that’s one of the best test methods for regression testing. An open-source framework, it is used to write and run repeatable automated tests.

As with anything else, the JUnit testing framework has evolved over time. The major change to make note of is the introduction of annotations that came along with the release of JUnit 4, which provided an increase in organization and readability of JUnits. The rest of this blog post will be written from usages of Junit 4 and 5.

How to Set Up JUnit Testing
So let’s dive right in. Here are the steps to set up JUnit.

The more common IDEs, such as Eclipse and IntelliJ, will already have JUnit testing integration installed by default. If one is not using an IDE and perhaps relying solely on a build system such as Maven or Gradle, the installation of Junit 4/5 is handled via the pom.xml or build.gradle, respectively. It is important to note that Junit 5 was split into 3 modules, one of those being a vintage module that supports annotation/syntax of Junit 4 and 3 (although usage of Junit 3 is frankly dismal and typically seen only in much older projects).
