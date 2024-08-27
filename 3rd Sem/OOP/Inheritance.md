Inheritance is a mechanism where a new class is derived from an existing class. In Java, classes can be derived from classes thus creating a hierarchy of classes. The derived class (subclass) inherits the members (fields and methods) of the base class (superclass).
    
    In Python and JavaScript, you also have inheritance, but it is achieved differently. In JavaScript, for example, you use the `extends` keyword to create a child class. In Python, the name of the parent class is included in parentheses in the class definition.
    
    Here is an example of a class in Java:
    
```java
public class ElectricCar extends Car {
    private int batteryLife;

    // Constructor
    public ElectricCar(String model, String color, int year, int batteryLife) {
        super(model, color, year);  // calling the constructor of the superclass (Car)
        this.batteryLife = batteryLife;
    }

    // Methods
    public void recharge() {
        System.out.println("Electric Car is recharging");
    }

    // Override Car's start method
    @Override
    public void start() {
        System.out.println("Electric Car started silently");
    }

    // Getter and Setter methods
    // ...
}

```