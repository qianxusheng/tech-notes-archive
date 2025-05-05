# Java tutorial summary https://docs.oracle.com/javase/tutorial/index.html

concept basics:
---
- **object:** state is stored in field, behavior is exposed by methods  
- **class:** a blueprint of object  
- **inferface:** a collection of methods without implementation  
- **package:** a namesapce that organizes classes and interfaces  
- **type:** Note that types refers to classes, interfaces, enumerations, and annotation types. Enumerations and annotation types are special kinds of classes and interfaces, respectively, so types are often referred to in this lesson simply as classes and interfaces.

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
- **nested class:** inner class and static nested class; 1. it's a way of logically grouping classes that are only used in one place; 2. It increases encapsulation; 3. It can lead to more readable and maintainable code. Nested class is a **member**, so it can access all the private members.  
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

inheritance:
---
- You can write a new *instance method* in the subclass that has the same signature as the one in the superclass, thus *overriding* it.  
- You can write a new *static method* in the subclass that has the same signature as the one in the superclass, thus *hiding* it.
- You can write a subclass *constructor* that invokes the constructor of the superclass, either implicitly or by using the keyword **super**.  
- **Private Members in a Superclass:** A subclass does not inherit the private members of its parent class. However, if the superclass has **public** or **protected methods** for accessing its private fields, these can also be used by the subclass. **A nested class** has access to all the private members of its enclosing class—both fields and methods. Therefore, a public or protected nested class inherited by a subclass has indirect access to all of the private members of the superclass.
- **casting:**
  - implicity casting(subclass->superclass) *Object obj = new MountainBike()*;  
  - explicity casting(superclass->subclass) *MountainBike myBike = (MountainBike)obj*.
- **Multiple Inheritance of State, Implementation, and Type:** Java does not allow multiple inheritance of state and implementation to avoid issues like field and method conflicts. However, Java supports multiple inheritance of type through interfaces.
- **overriding and hiding: happens when superclass and subclass have the same signature**
  - overriding: instance method in the subclass overrides the superclass's method.  
  - hiding: static method in the subclass hides the one in the superclass.
  - modifier: An overriding method may increase the visibility of the method it overrides, but cannot reduce it.
  - interface methods(complicated): some rules to decide choose which method.
- **polymorphism:** a principle in biology in which an organism or species can have many different forms or stages.  
- **super:** access superclass'smethods that are overrided by subclass or invoke superclass's constructor.  
- **object:** Object is a superclass of all other class, and it contians *clone*, *hashcode*, *toString*, *equals*, *getClass*, *finalize*.
- **final:** The final keyword is used to prevent a method from being overridden.  
- **abstract class and interface:**
  - abstract class: You want to share code among several closely **related classes**; You want to declare **non-static or non-final fields**.  
  - interface: You expect that **unrelated classes** would implement your interface; You want to take advantage of **multiple inheritance** of type.

Number and String:
---
They are Classes.  

generics: `generic type` is a instance, `generic class` is a class, `generic method`  
Generics were introduced to the Java language to provide tighter type checks at compile time and to support generic programming.
---
- **Invoking and Instantiating a Generic Type:** `Box<Integer> integerBox = new Box<Integer>()`;  
  - **type parameter:** `Box<T> box`; T is type parameter - placeholder;    
  - **type argument:** `Box<String> box`; String is type argument;  
  - **Parameterized Types:** `Box<String>` is a parameterized type. We use a specific type(String) as the type argument.
- **diamond:** `Box<Integer> integerBox = new Box<>()`; It is a syntax that complier can infer current type by context.  
- **raw type:** A raw type refers to a generic type that hasn't been assigned a specific type argument. For example, Box rawBox = new Box();. Raw types are common in legacy code, as many API classes (such as those in the Collections framework) were not generic before JDK 5.0.  
- **generic methods**  
- **bounded type parameter:** It is crucial for generic methods, as it allows you to impose constraints on the type parameter. For example, you might need to bound the type parameter to Comparable so that you can perform comparisons within the generic method.  
- **subtyping in generics:** Even A is B's subclass, it doesn't mean `class<A>` is `class<B>`'s subtype. The default behavior in generics is that generic types do not have an inheritance relationship, even if their type parameters do. Therefore, to establish an inheritance relationship between generic types, the generic class itself must explicitly extend another generic class.  
- **type inference:** Type inference is a Java compiler's ability to look at each method invocation and corresponding declaration to determine the type argument (or arguments) that make the invocation applicable. We can use type inference in generic method, instantiation of generic class, generic constructors.  
- **wild card:** In generic code, the question mark (?), called the wildcard, represents an unknown type. The wildcard ? is designed to address the issue of subtype incompatibility in generics, allowing code to handle different generic types more flexibly while preserving type safety. There are three tpyes of wildcards: Upper bounded wildcards, unbounded wildcards, lower bounded wildcards.  
- **type erasure:** Type erasure ensures that no new classes are created for parameterized types; consequently, generics incur no runtime overhead.  

package:
---
- **package:** use package statement. In on single file, you are allowed to put only one public type in the file, but you can put multiple private types in the file.

reflection:
---
Reflection is commonly used by programs which require the ability to examine or modify the runtime behavior of applications running in the Java virtual machine. For example, you can create a class browser to enumerate the members of classes.  

JVM:
---
- The Java Virtual Machine (JVM) is a virtual computer that runs Java bytecode(this means the program is running on the JVM). It hides differences between operating systems and hardware, enabling Java’s “write once, run anywhere (WORA)” capability.
- main functionality:
  - Class Loader: load .class file.
  - Execution Engine: executes bytecode using either an interpreter or JIT (Just-In-Time) compiler for faster performance.
  - Garbage Collector: automatic memory management (GC).  
  - Runtime Date Area: allocates memory during program execution.  
  - Native Interface: support for native library integration.  
