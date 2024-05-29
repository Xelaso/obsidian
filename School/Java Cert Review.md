## StringBuilder

- .append() returns the object itself, a reference to itself (the object)
    
## Arrays
- ArrayList class
	- in the java.util package
- Arrays class 
	- .toString(simple array):
		-  turns a ‘Type[]’ array into a string to be outputted (would output the array’s pointer, ie, I@7dc5e7b4, otherwise)
		- if the array is null, the result is []
	- .sort(simple array):
		-  sodrts the array, if the array is null, returns []
		- .binarySearch(simple array, value to look for):
		- the array must be sorted prior to being passed in; if it is not, the result is undefined (unpredictable)
		- if there are duplicate elements, there is no guarantee on which one is returned
		- Returns the index of the element
		- If the element is not found, take the negative index of where it would be inserted and subtract 1
	- .asList(simple array):
		- returns a List that is FIXED IN SIZE
		- cannot add nor remove, will throw runtime error UnsupportedOperationException
		- can modify values using set
	- .binarySearch(reference to simple array, value to search for):
		- returns index of the value to look for if found
		- if not found, returns the index the value _should_ be in, converts it to negative, then subtracts 1
## Control Flow
- Switch Statements
	- The case constant must be compile-time constant (either a literal or a **final variable that is initialized with a literal upon declaration**)
	- cannot have 2 case statements with the same value
	- can switch only on int-compatible or string 
	- The case values must be smaller than or equal to the switch value (ie if you switch on a byte, the cases cannot be bigger than byte. Will cause **compile time error**)
- Labeled For and While Loops
	- must _directly_ precede the loop heading, no code between the label and the loop
- Conditions for For and While Loop:
	- if the condition in a for and while loop are compile time constant and evaluate to false, a compile error will be thrown

## Exceptions
- Try-Catch
	- Catch can be omitted
	- **Cannot** only have 'try'; must have at least one catch or finally
	- finally always runs
	- Can have multiple catches, however the exceptions caught must be in order of most specific to least specific
- Exceptions
	- Throwable Classes: Exception and Error
	- Error does not need to be (but can) caught
		- usually handled/deferred to JVM
	- Exception
		- In the java.lang package
		- Unchecked Exception:
			- handled by JVM
			- not required to be declared or caught
			- List of Unchecked Exceptions:
				- ArithmeticException
				- RuntimeException
				- NulPointerException
				- ArrayIndexOutOfBoundsException
				- NumberFormatException
				- InputMismatchException
				- IllegalStateException
		- Checked Exception:
			- Must be declared or handled
			- Declared: 
				- methodName throws CheckedException
			- Handled:
				- try{
					- throw new CheckedException
				- } 
				- catch(Exception e){}
			- List of checked exceptions:
				- IOException
				- any self written exceptions
			- When overriding a method that declares an exception, you can either do nothing (don't declare an exception) or declare one of the same type of **narrower**
## Inheritance
- Overriding methods
	- When overriding a method, the access scope must be the same or broader than the original. 
		- public > protected > default > private
- Interface:
	- variables must be public static final
- When a child class declares a static method with the same signature as the parent class, it is called 'hiding', not 'overridden'. only instance methods can be overwritten; same for variables

## Java Enviroment
- javac myClass.java:
	- compiles myClass.java file into a myClass.class file
	- MUST have .java extension
- java myClass
	- executes myClass.class file
	- CANNOT have .class extension
## Function
- a method with return type void CAN have return, it just cannot return any value
- Java is a pass-by-value language
	- copies of privatives and object references are sent to the methods
	- methods can modify values INSIDE the objects using the reference, but not the reference itself
		- ie: a method assigning a passed in object to null will not change the calling method's variable to null

## Predicate
- Only 2 types of syntax
```java
Predicate<Type> a = s-> <Boolean Expression>
Predicate<Type> a = (<Type> s) -> <Boolean Expression>
Predicate<Type> a = (<Type> s) -> {
	//put statement here
	return <Boolean>
}
Predicate<Type> a = s -> {
	//put statement here
	return <Boolean>
}
```

## Basics
- Variable naming
	- it is legal to name a variable a java class name
		- String Integer = "bad practice";
- Static Imports
	- used to import static methods from a class
	- You can import one method or use \* to import all static methods
	- import static java.name.\*;
- If you import two packages with classes of the same name, you need to fully put the class name when using it
	- package1.className or package2.className
- Operator Overloading
	- changing what operators do
		- in c++, you can use \#define to change meanings of certain things
	- java does not support it
- Using '\_' in numbers:
	- cannot be in the front or back of a number, nor next to a decimal

## Initialization Block
- Order of what runs:
	- Static Initialization Block
	- Any code you have before you create an instance of the object with a non static initilzation block 
	- Object calls super until reaches top of hierarchy
	- Instance initilzation block is then called (after super but before anything else in constructor)
## Garbage Collector
- System.gc()
	- manually suggests JVM to check for things to be garbage collected
	- JVM is free to ignore the command
- 