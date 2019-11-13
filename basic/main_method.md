# public static void main(String[] args)

Java main method is the entry point of any java program.  
**String[] args** can be changed to **String... args**

## public
It has to be **public** so that java can execute this method on runtime.

**Main.java**
```java
package day01.main_method;

public class Main {
    // non-public main method
    static void main(String[] args) {
        System.out.println("Hello World.");
    }
}
```
**Output:**
```
Error: Main method not found in class day01.main_method.Main, please define the main method as:
   public static void main(String[] args)
or a JavaFX application class must extend javafx.application.Application
```

## static
There is no object of the class present on runtime.  
That’s why the main method has to be static so that JVM can load the class into memory and call the main method.

## void
Java main method doesn't return anything.

## main
The name of java main method is fixed, cannot be changed.

## String[] args
Java main method accepts a single argument of type String array. This is also called as java **command line arguments**.

**Main.java**
```java
package day01.main_method;
public class Main {
    public static void main(String[] args) {
        for (String arg : args) {
            System.out.println(arg);
        }
    }
}
```

**Output:**
```
[root@dev-vm6 ~]# javac Main.java
[root@dev-vm6 ~]# java Main first second third
first
second
third
```
