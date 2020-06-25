# exploring-java

## Configuring Java
- Download latest JDK
    - https://jdk.java.net
    - extract zip to C:\Program Files
    - copy the path of the JDK installed directory
        - C:\Program Files
- Setup JAVA_HOME variable
    - navigate to windows settings
        - search for "env"
        - select "edit system env variables"
        - click "environment variables..."
        - edit the System variables
        - create new env variable for system "JAVA_HOME"
            - path to JDK
            - C:\Program Files\jdk-14.0.1
- Update OS PATH variable to use from command prompt
    - edit the PATH variable
        - new path variable
        - C:\Program Files\jdk-14.0.1\bin
            - bin directory is where java executables and java runtime reside
        - click ok on all windows
    - now, open windows powershell and execute the following to confirm that java is properly installed
```cmd
java --version
```
- then, navigate to VSCode, hit control-shift-p
    - type: Java: Configure Java Runtime
    - download extension bundle
- then, open settings.json and set the following
```json
{
"java.semanticHighlighting.enabled": true,
"java.configuration.checkProjectSettingsExclusions": false,
"java.home": "C:/Program Files/jdk-14.0.1"
}
```
- now, to execute the file, right click the file and select "run"
- then, to execute 
- the file in the text editor should look as follows (titled QuickStart.java)
```Java
class QuickStart {
    public static void main(String[] args) {
        System.out.println("Java FTW");
    }
}
```
- from the command prompt, enter the following
```cmd
javac QuickStart.java
```
- this will output a QuickStart.class file in the text editor
    - if you created a repo with Java .gitignore, this file will be .gitignored










- Final modifiers in Java
    - can be applied to a var, a method, or a class
    - when used with a class, the class cannot be extended further
    - One method of protecting a class from being subclassed
        - often, sensitive classes are made final due to security reasons
```Java
class SensitiveData {
    public static void main(final String[] args) {
        System.out.println('sensitive environmental var');
    }
}
```