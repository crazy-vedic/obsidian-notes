This is the mechanism where you bundle the data (variables) and the methods that operate on the data into a single unit, which is called a class. A class is a blueprint for the object. You can think of a class as a template for creating objects (specific instances of the class).
    
    In Python, JavaScript, and Java, a class is defined using the `class` keyword. In C, however, there's no built-in class support but you can achieve similar functionality with structs.
    
   ```java
public class Car {
	private String model;
	private String color;
	private int year;

	// Constructor
	public Car(String model, String color, int year) {
		this.model = model;
		this.color = color;
		this.year = year;
	}

	// Methods
	public void start() {
		System.out.println("Car started");
	}

	// Getter and Setter methods
	// ...
}

```
    
    The `private` keyword is a modifier that makes the variables `model`, `color`, and `year` private so they can't be accessed directly from outside the `Car` class. You would typically use getter and setter methods to read and modify the private variables.