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


## Provide Middleware 
1- Synchronous & Asynchronous

Distinguish between the type of coupling:
 Pure signal: the message does not contain any data; computing is done
based on the existence of the message
 Object.notify()/notifyAll() in Java (Thread synchronization)
 Structured/Unstructured data: the message contains data and the
receiver knows how to process it
 send some text to a translation service
 Data and Command: the message contains data and a reference to a
processing style
 send address data and whether to create/update an entry
 Data and Processor: the message contains data and executable code
for processing it.



## Persistance Context
collection of managed entity objects, spring boot manages the lifecycle of all the entities
synchronizes the objects with DB

## @autowired annotation

allows access to the entity object without instatiating the object, Spring boot takes care of instatiation and lifecycle of object

because of this we are kind of accessing the proxy, so JPA entity can never be final.


*Owning side is the one who has the FK

## Core Principles of JAVA EE 
1- Dependency Injection
2- Implicit Services : DI, security, Data Access from db
3- Interceptors : Intercepting the method and calling some other functions such as logging etc before/after the main function by adding some proxy. Method Interceptors
4- Annotations : Compile Time ( @Data), runtime (@Profile -> Dev, Prod switching) , Built in (@Override,@Deprecated) 
@Bean -> method instatiates the object, @Configuration -> indicated a new component and has @Bean annotation

## Inversion of Control 
Inversion of Control (IoC) is a design pattern in software development that allows for loosely coupled components and improves the modularity and extensibility of an application. Spring Boot, a popular Java-based framework, makes use of IoC extensively.

@Bean
public DataSource dataSource() {
   DriverManagerDataSource dataSource = new DriverManagerDataSource();
   dataSource.setDriverClassName("com.mysql.jdbc.Driver");
   dataSource.setUrl("jdbc:mysql://localhost:3306/mydb");
   dataSource.setUsername("root");
   dataSource.setPassword("password");
   return dataSource;
}
Then, in other classes, the developer can simply annotate a DataSource variable with @Autowired to have the Spring Container inject the Bean:

##class path scanning 
Classpath is scanned at startup and all beans and components are instantiated by the
framework resulting in the ApplicationContext (sum of all configured components and
beans)
@Service => Business layer, @Repository => Persistance layer, @Controller => MVC , @Configuration, @Bean => Component 


## Spring Boot 
 Extension of the spring framework (spring framework is complex to use & configure)
• Eliminating boilerplate configuration for setting up spring application - autoconfiguration/ makes it easy to setup new project
• Build dependency management via starters
• Resolves application context: Servlet, Filter and ServletContextInitializer
• Spring Boot also includes an embedded web server, which allows developers to quickly create and deploy web applications without needing to set up a separate web server.

## Model model
spring UI class to put the data in also get data from client.

## Java bean Validation
@NotNull, @Min(),@Size(max=)

in method we recieve Errors class object which has hasErrors() method by which we redirect to client to tell the client about the errors


@Autowired
private DataSource dataSource;

In Spring Boot, IoC is achieved through the use of the Spring Container, also known as the Application Context. The Spring Container manages the creation, configuration, and lifecycle of the objects (known as Beans) that make up an application. Instead of creating and managing objects directly in code, developers define the objects as Beans in configuration files or with annotations and let the Spring Container handle their instantiation and injection.
In addition to IoC, Spring Boot also makes use of other design patterns such as Dependency Injection (DI) 

## Principles of REST



