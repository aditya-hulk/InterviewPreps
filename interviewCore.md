# ** ***Final Interview Question and Answer***
## What is final in java?
- final is a keyword which is used to restrict the user.
- it can be applied with   varialbes, methods and classes.
- When variable is declared as final then it value won't change.
- When class is marked with final keyword then it can't be inherited.[ It prevents inheritance]
    - String, Integer and other wrapper class are final class.
- When method is marked with final keyword then it cannot be overridden by sub class.
## Why constructor cannot be final in java?
![alt text](image-15.png)![alt text](image-16.png)![alt text](image-17.png)
### Rules of constructor:
- having same name as that of class name.
    - So if you override the constructor of abstract class in it's subclass 
    - eg class A having constuctor A() and Class B extends A having constructro B() 
    - in overrridden you require A() constructor in B which voilates it's rules.
## Code
![alt text](image-18.png)![alt text](image-19.png)![alt text](image-20.png)![alt text](image-21.png)![alt text](image-22.png)![alt text](image-23.png)![alt text](image-24.png)![alt text](image-25.png)![alt text](image-27.png)![alt text](image-28.png)![alt text](image-29.png)

##  What is a blank final variable in Java?
- A variable that is declared as final and not initialized at a time of declaration is called blank final variable.
- blank final variable is initialized in constructor.
- blank final static variable initialzied only in static block
## What is the difference between an abstract method and final method in Java?
- The key difference between abstract method and final method is that abstract method must be overridden in the subclass but final method cannot be overridden in the subclass
## Which is the most common predefined final class object in Java?
- String
## What are the two ways to make a class final?
- The first way to make a final class is to declare a class with final keyword.
-  Another way is to declare all of its constructors as private. If a class has only private constructors, it cannot be subclassed.
## Can we create an instance of final class in another class?
- Yes, we can create an instance of final class in another class but cannot be inherited.
## Is it possible to change the value of a final variable in Java?
- No, Java does not allow changing the value of a final variable. Once the value is set, it cannot be modified.
## Why Integer class has been defined final in Java?
- Integer class is a wrapper for int. If it is not declared final, any other class can extend it and modify the behavior of Integer
operations. To avoid it, Integer wrapper class is declared as final.
## Can we declare main method as final?
- Yes, we can declare the main method as final. And it can also run the show.

![alt text](image-26.png)
## Can we mark a block final in Java?
- No, a block cannot be marked final in java.
# ** ***About Static***
## What is static in Java?
- static is a keyword in java that is mainly used for memory management.
- The members that are marked with the static keyword are called static members.
- The users can apply static keywords with variables, methods, blocks, and nested classes. 
### Characteristic of static keyword.
- Shared memory allocation
- Accessible without object instantiation:
- Associated with class, not objects: 
- Can be overloaded, but not overridden:
- Cannot access non-static members:
### static method
![alt text](image-30.png)![alt text](image-31.png)
- When a method is declared with the static keyword, it is known as the static method.
-  Any static member can be accessed before any objects of its class are created, and without reference to any object.
#### Some restriction in static method
- They can only directly call other static methods.
- They can only directly access static data.
- They cannot refer to this or super keyword in any way.
### static varaible:
![alt text](image-32.png)![alt text](image-33.png)
- When a variable is declared as static, then a single copy of the variable is created and shared among all objects at the class level.
- Static variables are, essentially, global variables
- All instances of the class share the same static variable.
- We can create static variables at the class level only.
### Static block:
![alt text](image-34.png)
- in order to initialize your static variables, you can declare a static block that gets executed exactly once, when the class is first loaded. 
### Intresting hierachy
#### Static method and static block
![alt text](image-35.png)
- static block executed first. (order of execution when compare with static method.)
#### static varaible and static block
![alt text](image-36.png)![alt text](image-37.png)
- static block and static varaible are executed in the order they are present in a program.
### Restriction in static mehtod and other stuff
#### Static method with non static or instance varaible.
 ![alt text](image-38.png)
 #### Static method and instance method call.
 ![alt text](image-39.png)
 #### static method with super keyword
 ![alt text](image-40.png)
 ### instance method can access static variable and method
 ![alt text](image-41.png)![alt text](image-42.png)![alt text](image-43.png)
 ### Usage of static varaible and methods
![alt text](image-44.png)![alt text](image-45.png)
### Static Class
- A class can be made static only if it is a nested class.
- We cannot declare a top-level class with a static modifier but can declare nested classes as static. 
![alt text](image-46.png)
## What the outer class won't make static
### Class context
-   An outer class is not associated with any instance of another class.
- It represents a standalone structure that can contain methods, variables, and inner classes.
- Making it static would imply that it is tied to a specific instance, which contradicts its role as an outer class.

### Design principle:
- The design of Java aims to maintain a clear hierarchy and encapsulation.
-  Allowing an outer class to be static would complicate the model 
### Inner class
- Inner class require instance of outer class.
- The relationship between outer and inner classes relies on instances, and a static outer class would break this relationship.
## Can we access static members if no instance of the class is constructed?
- Yes,  because they are not tied to a specific instance. They are shared across all instances of the class.
##  What is the main use of static keyword in java?
- The static keyword can be used when we want to access the data, method, or block of the class without any object creation.
- It can be used to make the programs more memory efficient.
## Can we mark a local variable as static?
-  No, we cannot mark a local variable with a static keyword.
## When does a static variable get memory?
- When a class is loaded into the memory at runtime
- the static variable is created and initialized into the common memory location only once.
##  In which part of memory static variables are stored?
- Inside heap memory there is space called Permanent generation abbreviate as PermGen. Here static varialbe are stored.
## How static variable is different from the instance variable?
### Static varaible:
- A static variable is also called class variable
- Class variable can be accessed inside a static block, instance block, static method, instance method, and method of the inner class
- Class variable is always resolved during compile time
- Static variable cannot be serialized in Java
### Instance varaible:
- an instance variable is also called non-static variable.
- instance variable can be accessed only inside the instance members, and method of the inner class.
- instance variable is resolved during the runtime.
- instance variable can be serialized.
## What is a static method in Java?
- When a method is declared with the keyword ‘static’, it is called static method in java.
## Why is a static method also called a class method?
- A static method is also called a class method because it ties to a class rather than an individual instance of a class.
-  Therefore, we need not to create an object of the class to call and execute static method.
## Can we access static members (such as static variables and static methods) from an instance method?
- Yes, we can access static members from an instance method in java.
## Is it possible to access instance members from a static method?
- No, it is not possible to access instance members like instance variable and instance method from a static method.
## About method signature
![alt text](image-57.png)
## What is the difference between static method and instance method?
### Static method
- A static method is also known as class method
- The only static variable can be accessed inside static method 
- We do not need to create an object of the class for accessing static method 
-  Class method cannot be overridden 
-Memory is allocated only once at the time of class loading 
### Instance method
- the instance method is also known as non-static method.
- static and instance variables both can be accessed inside the instance method.
- in the case of an instance method, we need to create an object for access.
-  an instance method can be overridden.
- in the case of the instance method, memory is allocated multiple times whenever the method is calling.
## Can we have a static method in an interface?
- Yes, from Java 8 and onwards, the interface allows to define a static method with body.
## Can we use this or super keyword in static method in Java?
### About this keyword in static
- We cannot use “this” keyword in the body of static method because static methods are associated with a class, not an instance.
- Only instance methods have an implicit “this” object reference associated with them.
-  Therefore, class methods do not have a “this” object reference associated with them.
### About super keyword with static
- we cannot use the super keyword inside the body of static method.
- This is because we use super keyword to call superclass method from the overriding method in the subclass. 
- Since we cannot override the static methods, we cannot use the super keyword in its body.
##  Is it possible to overload static methods in a class?
-  Yes, we can overload static methods but not override them. This is because they are bound with class, not instance.
## Is it possible to override static method in class?
- No, we cannot override static methods 
- There is concept of method hiding
- Also  static methods belong to a class, not individual objects, and are resolved at compile time by java compiler.
## Can we override an instance method as static.
- No
##  Why static block is executed before the main method in java?
- When the dot class file is loaded into memory, static block is executed.
- After executing the static block, JVM calls the main method to start execution. 
## What is the use of static block in java?
- A static block can be used when
- we want to write that logic inside static block that is executed during the class loading.
- we want to change the default value of static variables.
- we want to initialize static variable of the class.
## . How static block is different from an instance block in java?
### Static block:
- Static block is also called a static initialization block 
-  Static block gets executed before the instance block
- Only static variables can be accessed inside the static block 
- Static block executes when the class is loaded into the memory 
- We cannot use this keyword inside the static block 
### Instance block:
- whereas instance block is also called instance initialization block or non-static block.
- whereas, instance block executes after the static block.
- whereas, both static and non-static variables can be accessed inside the instance block.
- whereas instance block executes only when an instance of the class is created.
- whereas this keyword can be used in the instance block.
## Can we declare a static block inside a method?
- No, we cannot declare a static block inside a method.


## Code Snippet
![alt text](image-47.png)![alt text](image-48.png)![alt text](image-49.png)![alt text](image-50.png)![alt text](image-51.png)![alt text](image-52.png)![alt text](image-53.png)![alt text](image-54.png)![alt text](image-55.png)![alt text](image-56.png)![alt text](image-58.png)![alt text](image-78.png)![alt text](image-79.png)![alt text](image-80.png)![alt text](image-81.png)![alt text](image-82.png)![alt text](image-83.png)![alt text](image-84.png)







