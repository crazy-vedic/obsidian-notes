## Runtime Polymorphism (Dynamic Binding)

Runtime polymorphism or Dynamic Method Dispatch is a process in which a call to an overridden method is resolved at runtime. This type of polymorphism is achieved by Method Overriding.

**Method Overriding Example**:

javaCopy code

`class Car {     void run() {         System.out.println("Car is running");     } }  class Audi extends Car {     @Override     void run() {         System.out.println("Audi is running safely with 100km");     }      public static void main(String args[]) {         Car b = new Audi(); //upcasting         b.run();     } }`