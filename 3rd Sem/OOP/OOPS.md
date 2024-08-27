[[Java]]


1. [[Encapsulation]]: 
	The feature of classes of being able to bundle the methods and attributes into a single unit, a class. 
    
2. [[Inheritance]]: 
	Mechanism by which a new class is derived from a previously made class, subclass inherits methods and attributes from the super. Can be used like Animals -> Humans.
	
3. [[Polymorphism]]: 
	[[Method overloading]]:
		Run time
		Taking two methods with the same name but different arguments in the same class.
		Allows us to construct a by two different methods.
	[[Method overriding]]:
		Compile time
		Overriding a method from a super by using decorator @override, dropping the previous method, and using the current one.
4. [[Abstraction]]: 


Staticicity:
	class Student{
	int rollno;
	String name;
	static String College="muj";

	Student(int r, String n) {
	rollno=r;
	name=n;
	}}

>[!NOTE]
>NOW IF EVER IN THE FUTURE WE CHANGE Student.College, College attribute of the class Student NOT the OBJECT
>VALUABLE FOR CONFIG VARIABLES OF OUR CLASS

Similarly, static methods are used for if you want to be able to call a method of a class, and no object or interaction is required with non static methods/variables.
Static shit is done before non-static shit

Finality:
	Final attributes can't be modified, final methods can't be overridden.


Buffered reader -> Input is being sent to buffer, then picking up from buffer
try{}-catch{}
IOException : All exceptions are a child of this parent class