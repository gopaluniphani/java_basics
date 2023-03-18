Inheritence
-> A child class can inherit public, default & protected the the properties & methods of parent class.
-> Enables reusability of code.

Method Overloading
-> You can define multiple methods with same name in the same class with different no. of arguments / different data type of the arguemnts(same no.)

Method Overriding
-> Overwrite the definition of a method that is inherited from the parent class.
-> You can also extend the behaviour of parent class's method by overriding and calling the super keyword without rewriting the same code.

Static Variables
-> Also knows as class variables.
-> only one variable will get created for that class.
-> all the objects of this class will share the same static variable.
-> no need to instantiate and object to access this variable.
-> can be directly accessed using class name

Scope of Variables
-> Three regions in memory
    -> stack
    -> heap
    -> code

    -> Stack
        -> All the variables of simple data types that are defined in a method will get created in stack. 
        -> These will go out of scope and get deleted from the memory once the method is returned.

    -> Heap
        -> All the objects/variables for which memory is dynamically allocated (using new operator) are stored in heap. And the reference to these objects are stored in stack.
        -> These objects won't be deleted from the memory even the method in which they were created is returned. But the reference to these objects will be deleted.
        -> To free the memory, there are two ways
            1. To call the destructor (close method of objects).
            2. Once the objects has no reference, the garbage collector will delete them.
    
    -> Code
        -> When JVM loads the program into memory, all the code will be saved in this region.
        -> The code includes all the classes and methods.
        -> Since static variables are class level variables, the memory for these variables will be created in the code region.
        -> Static vairables will only get deleted when the program is terminated.


Multi Threading -> Thread, Runnable
-> Threads are also called as Light Weight Processes
-> A process can have any number of threads.
-> All the threads will share resources such as
    -> static variables.
    -> objects.
    -> process id
-> But the threads will have a different
    -> stack
    -> thread id
-> Java Provides and easy API to create user level threads to achieve concurrent programming.
-> This API includes
    -> Thread class
    -> Runnable Interface
-> Since all the threads share resources, we should be careful on how we are accessing/modifying the values of shared objects.
    -> Especially when working with critical sections of code. (Eg: Husband/Wife withdrawing amount at the same time from a joint account). This scenario is also known as race condition.
    -> To solve this issue, we use thread locks.
    -> We have to be careful when using locks becuse it might lead to dead locks.
    

I/O -> Console, File
File Parsing -> JSON, XML

[Pending] JDBC -> Drivers (SQL -> MySQL, PostgresQL, NoSQL -> MongoDB)

