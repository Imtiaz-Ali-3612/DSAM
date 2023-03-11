# DSAM

Core Characterstics of DS :

## Autonomous Entities / Partial Failures
1. No Global Time
2. No Global Memory
3. Communication Errors
4. Heterogeneity (technical, semantical)
5. Complex Associations (dynamic bindings, multi-party)

## Dependency Injection & Spring Framework
Problems without dependency injection :
1- If many classes needed the object they all would have created new instance, which may created issue with memory.
2- If class is singleton we cannot instantiate the class in every class.
3- Difficult to test


Solution:
Dependency Injection ( Passing the object through constructor)
in case of Spring boot Spring framework handles the dependency, we Inject the object in Constructor with @Inject() annotation.
and to let spring know we need the object of class we declare the class with @Service() annotation.
now spring framework manages the object instantiation for us and pass same object to all classes thats going to need the service.


