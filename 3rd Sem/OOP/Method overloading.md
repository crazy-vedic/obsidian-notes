## Compile-time Polymorphism (Static Binding)

Compile-time polymorphism is achieved by method overloading. In method overloading, a class has more than one method with the same name but with different parameters.

**Method Overloading Example**:

```java
public class Display {
    void show(int x) {
        System.out.println("One parameter: " + x);
    }
    void show(int x, int y) {
        System.out.println("Two parameters: " + x + ", " + y);
    }
}

```