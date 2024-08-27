Abstraction is a process where you hide certain details and only show the essential features of the object. In Java, abstraction is achieved using abstract classes and interfaces.
    An abstract class can have both abstract (method without body) and non-abstract methods (method with body). It can provide a default behavior that can be shared by multiple subclasses.
    
    An interface in Java is a completely abstract class that is used to group related methods with empty bodies:
    
```java
interface Animal {
    void eat();
    void sound();
}

class Dog implements Animal {
    public void eat() {
        System.out.println("Dog eats");
    }
    public void sound() {
        System.out.println("Dog barks");
    }
}

```