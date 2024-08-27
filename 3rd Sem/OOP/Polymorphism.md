Polymorphism allows us to perform a single action in different ways. In Java, we use method overloading and method overriding to achieve polymorphism.
    
	Method overloading happens when a class has two or more methods by the same name but different parameters.

    Method overriding means having two methods with the same method name and parameters, one of the methods is in the parent class and the other is in the child class.

    In Python and JavaScript, you can also override methods but JavaScript doesn't support method overloading.

```java
class Display {
    void show(int x) {
        System.out.println("One parameter: " + x);
    }
    void show(int x, int y) {
        System.out.println("Two parameters: " + x + ", " + y);
    }
}
```
    
    Method overriding example in Java (we saw this in the ElectricCar class example too):
    
```java
@Override
public void start() {
    System.out.println("Electric Car started silently");
}

```