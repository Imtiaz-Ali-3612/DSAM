# DSAM

## Core Characterstics of DS :

1. Autonomous Entities / Partial Failures
2. No Global Time
3. No Global Memory
4. Communication Errors
5. Heterogeneity (technical, semantical)
6. Complex Associations (dynamic bindings, multi-party)

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

## Failure Models in Distributed Systems 
1. Sysnchronization : two services are synchrinzed while performing the task
2. Scheduling : 
3. Communication Failure : 
4. Security Failure ( MITM) : Man in the middle can occur to demage/steal the information

## Potential of DS 
1. Robustness ( less likely to cause severe demage due to errors/
2. Flexibility
3. Availability 
4. Cost Saving

## Middelware :
Middleware in distributed systems is software that acts as a bridge between different applications, services, or systems, enabling them to communicate and interact with each other seamlessly.
Middleware is the classical means to manage the complexity of distributed systems

Communication: Middleware provides communication services that allow different applications to exchange data and messages with each other. It can support a range of communication protocols such as HTTP, TCP/IP, and message-oriented middleware (MOM) protocols like JMS.

Integration: Middleware can integrate different applications and services to work together seamlessly. It can provide integration services such as data mapping, transformation, and routing.

Security: Middleware can provide security services to ensure the confidentiality, integrity, and availability of data in a distributed system. It can provide services such as authentication, authorization, encryption, and digital signatures.

Transaction Management: Middleware can provide transaction management services that allow different applications to participate in a transaction. It can manage transactional consistency and recovery in a distributed system.

Resource Management: Middleware can manage distributed resources such as databases, message queues, and web services. It can provide services such as connection pooling, caching, and load balancing.


## Clustering 
Clustering is a technique used in distributed computing and computer networking to group multiple independent computers, servers or nodes together to work as a single system. Clusters are typically used to improve performance, reliability, load balancing, reduce failover, and availability of a system by allowing multiple computers to work together to perform tasks.
Verticle Clustering : multiple services same machine 
Horizontal Clustering : different machines


Vertical Clustering : 
