# https://docs.python.org/3/tutorial/

I am lazy, just read the content I am interested

## list comprehension
Python supports list comprehension and nested list comprehension, which is a really concise way to create list compared to using for-loop.

## immutable
*String* and *Tuple* are immutable in python, which means you cannot modify it since it is created. *Set* and *dictionary* and *list* are mutable.

## primitive types
Commonly use: int, float, boolean, str, tuple, None;

## tuple and list
tuple is immutable and usually contains a heterogeneous sequence of elements; list is mutable and usually contains a homogeneous sequence of elements.  

## set
To create empty set, you need to *set()*.

## sorted and reversed
*sorted* return a list  
*reversed* return a iterator  
*.reverse()* and *.sort()* are methods of **list**

## pass and continue
pass is just a placeholder for condition body.  
continue is going to next loop and pass the current loop.

## script
script is python .py file, which can use as a module and import it.

## input and output
- output formatting  
formatted string literals: f'XXXX {variable_name} XXXX'  
str.format(): print('{}{}{}'.format(c,b,c))
- reading and writing files  
open(filename, mode, encoding=None)  -- use *with* open file or manually *file.close()*  
*read*, *readline*, *write*, *json* and more...

## syntax errors and exceptions
syntax errors: most common, and it's compile-time error  
exceptions: it's runtime error, you can use **try...except** to catch or **raise** to trigger  
finally: The finally keyword is used to release resources, regardless of whether an exception occurs or not.

## class
- scope: local(nested function); enclosing(outer function); global(in the module); built-in(python built-in function, like *len()*)
- namespace(dictionary): class creates a new namespace
- class object: Class objects support attribute references and instantiation -- x = class.i; x = Myclass()
- instance object: use instance as object -- node = TreeNode() --> this is a instance object
- method object: use method as object -- xf = x.f() --> *xf* is a method object
- class variable and instance variable
- `@classmethod`(cannot access instance variable, use *cls* as parameter), `@staticmethod`(cannot access either instance variable or class variable, don't have parameter), None(instance method, use *self* as parameter)
- access modifier: python don't have access modifier, we use naming convetion, like `_number` means this variable is private.
- Generator and Iterator: An iterator implements the __iter__() and __next__() methods. Generators provide a concise way to create iterators using generator expressions (), which `lazily generate values on demand`.

## virtual environment
Venv is used for eliminating package conflicts between different Python applications.
