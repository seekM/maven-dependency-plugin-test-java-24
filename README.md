This project intends to show the behaviour of the maven plugin `org.apache.maven.plugins:maven-dependency-plugin:3.8.1` using different versions of the JDK.

Running `mvn clean dependency:analyze` in this project works when using JDK 23 (`<maven.compiler.release>23</maven.compiler.release>`), but fails when using JDK 24 (`<maven.compiler.release>24</maven.compiler.release>`) with the follwing error message:

```
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-dependency-plugin:3.8.1:analyze (default-cli) on project maven-dependency-plugin-test-jdk24: Execution default-cli of goal org.apache.maven.plugins:maven-dependency-plugin:3.8.1:analyze failed:
Byte code of 'com.github.seekM.Main' is corrupt from directory = [...]]\maven-dependency-plugin-test-jdk24\target\classes, path = [...]\maven-dependency-plugin-test-jdk24\target\classes\com\github\seekM\Main.class: Unsupported class file major version 68
```