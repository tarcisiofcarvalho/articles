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
