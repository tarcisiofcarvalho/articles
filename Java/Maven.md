#### Check Maven version

```sh
mvn -v
```
### List Maven archetype availables

```sh
mvn archetype:generate
```

### Create a project

```sh
mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-webapp -DarchetypeVersion=1.4 -DinteractiveMode=false
```

### Life cycle commands

```sh
# validate the project is correct and all necessary information is available
mvn validate

# compile the source code of the project
mvn compile

# test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
mvn test

# take the compiled code and package it in its distributable format, such as a JAR.
mvn package

# run any checks on results of integration tests to ensure quality criteria are met
mvn verify

# install the package into the local repository, for use as a dependency in other projects locally
mvn install

# done in the build environment, copies the final package to the remote repository for sharing with other developers and projects.
mvn deploy

```

### References

https://maven.apache.org
