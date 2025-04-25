This project intends to show the behaviour of the maven plugin `org.apache.maven.plugins:maven-dependency-plugin:3.8.1` using different versions of Java as the target of compilation.

Running `mvn clean dependency:analyze` in this project works when using Java 23 (`<maven.compiler.release>23</maven.compiler.release>`) as the target of compilation, but fails when using Java 24 (`<maven.compiler.release>24</maven.compiler.release>`) with the following error message:

```
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-dependency-plugin:3.8.1:analyze (default-cli) on project maven-dependency-plugin-test-java-24: Execution default-cli of goal org.apache.maven.plugins:maven-dependency-plugin:3.8.1:analyze failed:
Byte code of 'com.github.seekM.Main' is corrupt from directory = [...]]\maven-dependency-plugin-test-java-24\target\classes, path = [...]\maven-dependency-plugin-test-java-24\target\classes\com\github\seekM\Main.class: Unsupported class file major version 68
```