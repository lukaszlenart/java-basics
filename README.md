# Java Basics training

## Tools

You can use one of those editors:

- [Intellij IDEA](https://www.jetbrains.com/idea/download/) - the Community edition is free
- [VS Code](https://code.visualstudio.com/) with a Java plugin

You must download and install

- [JDK 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Apache Maven](https://maven.apache.org/)
- Git client, either via command line or with [Github Desktop](https://desktop.github.com/)

## Test you environment

Confirm you have all the tools installed by running the below commands and checking the results:

- `java -version`
  ```
  java version "1.8.0_152"
  Java(TM) SE Runtime Environment (build 1.8.0_152-b16)
  Java HotSpot(TM) 64-Bit Server VM (build 25.152-b16, mixed mode)
  ```
- `mvn -v`
  ```
  Apache Maven 3.x.x
  ...
  ```
- `git --version`
  ```
  git version 2.x.x
  ```

## Task 1

Create a simple Java based application using a a Maven archetype

- start cmd
- enter this project root folder (`cd java-basics`)
- start the below command to generate your simple project, use your own artifact name
  ```
  mvn archetype:generate -DgroupId=pl.org.lenart -DartifactId=<your-name> -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.3 -DinteractiveMode=false
  ```
- enter the artifact folder (`cd <your-name>`)
- edit `App.java` file located in `src/main/java/pl/org/lenart/App.java`
- change `Hello world` text to show `Hello <your name>`
- save and the command
  ```
  mvn package
  ```
- use this command to start the app
  ```
  java -cp target/classes pl.org.lenart.App
  ```
- inspect output if matches your text
