# exploring-java
- Final modifiers in Java
    - can be applied to a var, a method, or a class
    - when used with a class, the class cannot be extended further
    - One method of protecting a class from being subclassed
        - often, sensitive classes are made final due to security reasons
```Java
class SensitiveData {
    public static void main(final String[] args) {
        System.out.println('sensitive environmental string');
    }
}
```

## Compile source code with Java
```git
javac QuickStart.java
```
```Java
class QuickStart {
    public static void main(String[] args) {
        System.out.println("Java mother fuckers");
    }
}
```