# Java tutorial summary https://docs.oracle.com/javase/tutorial/index.html

concept basics:
---
- **object:** state is stored in field, behavior is exposed by methods  
- **class:** a blueprint of object  
- **inferface:** a collection of methods without implementation  
- **package:** a namesapce that organizes classes and interfaces  

language basics:
---
- **primitive data types:** bit, short, int, long, float, double, char, boolean;  
- **field and variable:** instance variable(non-static field), class variable(static field); local variable; parameter;  
- **opertator**: ...  
- **expression, statement, blocks:** operator maybe used in expressions (1+1), expressions are the core component of statement (int a = 1 + 1;), blocks are made of a group of statements;  
- **control flow:** if-else-then; for; do-while; while; switch; break; continue; return  

class and object:
---
- **class declaration:** class can extend superclass or implement interface.  
- **class method:** mothod is consist of modifier, return type, method name(naming convention: verb and captialization, like *getType*), method body, parameter list, exception list;  
- **parameters and arguments:** Parameters refers to the list of variables in a method declaration. Arguments are the actual values that are passed in when the method is invoked.  
- **passing value:** primitive data type passing and reference data type passing. 
- **static:** static is a keyword used to declare variable is a static-field  
- **final static:** final static is used to declare one constant is compile-time constant, which is fixed once the code is compiled.  
- **control access(modifier):** class-level: public and no modifier(package-private); member-level: public, protected(same package or subclass), private(only in current class), no modifier(only in current package);  
- **constructor:** create personalized objects;  
- **initialization block:** static or non-static; helping constructor to initialize basic fields that we don't need to customize.
- **this:** *this* key word has two functionality. Field shadowing and **constructor reusing**:  
![image](https://github.com/user-attachments/assets/4f27898e-b92e-485a-9b2d-2c1c1a2773df)
![image](https://github.com/user-attachments/assets/f99c5526-5c5c-4886-ad29-6952d393598d)  
- **nested class:** inner class and static nested class; 1. it's a way of logically grouping classes that are only used in one place; 2. It increases encapsulation; 3. It can lead to more readable and maintainable code.  
- **shadowing in nested class:** When a variable is declared in an inner class with the same name as one in an outer class, the inner class variable takes precedence during access.  

annotation:
---
- An annotation itself is just a "label" — it doesn't perform any action on its own.  
- Through **reflection**, a program can read this "label" at runtime and execute corresponding logic based on it.  
- This approach is commonly used in *framework design*, such as in **Spring**, **JUnit**, and **ORM mapping**.‘

interface:
---
- When you define a new interface, you are defining a **new reference data type**. You can use interface names anywhere you can use any other data type name. If you define a reference variable whose type is an interface, any object you assign to it must be an instance of a class that implements the interface  
- **interface upgrading:** extends old interface; using default method(need to be implemented); static method  
- An interface declaration can contain method signatures, default methods, static methods and constant definitions. The only methods that have implementations are default and static methods.
