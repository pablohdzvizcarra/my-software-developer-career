# My Journey to Become a Software Engineer

In this repository, I will keep the progress of my career as a software engineer. I think it is very
important that we all have some record of our progress, when I started programming, I wanted to have
a record to go in the future and see what decisions I have taken and this repository is the result
of that record.

### Programming Changes My Life

#### Day 1444 Java 21

Today I begin to discover the new features that arrive with the new Java LTS release. 
I started to watch a big picture of the features, and did a deeper dive into JEP 440 Record Patterns.
Records are a great feature in Java really helpful, I love the way in which Java started to include this new 
features to the language. 

#### Day 1443 Continues with the Composite Pattern

Today I did a little exercise with the composite pattern, coding a basic application to create a menu with items.
I used a JSON file with the menu items then read this JSON file, parse the data to POJOs and create the structure with 
the composite pattern.
Tomorrow I will explore the Java 21 new features.
Java 21 arrives this week and looks like incredible and amazing.  

#### Day 1441-42 Composite Pattern

Currently, I am learning about the composite pattern. 
This pattern helps us to iterate over a hierarchy of objects like a tree in which you have a node and lefts.

#### Day 1440 Iterator Pattern

Today I begin to study the Iterator design pattern and the single responsibility principle.
I would need to do some exercises to understand the pattern, it's confused because you need to understand some 
Object-Oriented concepts to better learning. 

#### Day 1438-39 Continue Studying Design Patterns

I continue reading the Head First Design Patterns book, I begin to study the Iterator pattern. 

#### Day 1437 Learning Java API

Today I was studying some classes and implementations in the Java API like the AbstractList class, how it works the 
sort method.
The sort method works with a template method; you need to define the sort by a static method, the default algorithm 
to sort the array is hard to understand. I will hope that in the future I can understand more about the low-level 
components in the Java API and how these components work better. 

#### Day 1436 Template Method

Today I begin to study the template method pattern.
With this pattern, you create an algorithm recipe inside a method, for example, how to create juice and the subclasses 
only change the necessary things to complete the task, in the juice example maybe only the subclass that prepares an 
Orange Juice only needs to change one step to add Oranges. 

#### Day 1435 Podman

Today I begin to use podman for my container activities. In the work, we use OpenShift to deploy our applications 
creating Pods, the problem is these Pods work inside RHEL servers, and well, sometimes we have permission problems 
about using docker in our local machines to test the applications.
Podman and Docker have a lot of similarities but differ in some things like rootless containers. 

#### Day 1434 Good Code Practices

Today I have been working on package all the classes related to a database connection into a java package for reuse 
in other projects with this separation I can use the implementation for the database in any project only with copy 
and paste the entire package, these classes inside the package have some functionalities like, create, edit, delete 
documents and database.
I need to study again about Generics in Java and how the generics can be used to code reuse. 

#### Day 1433 Facade Pattern

Today I began to study the Facade design pattern, this pattern simplifies a subsystem to a client.
If you have a Client that needs to interact with your subsystem with this pattern, you can easily manage the 
interaction. 

#### Day 1432 Continues with the Adapter Pattern

The intent of the Adapter pattern is to change the interface from one object to the interface required for the client.
The adapter pattern does not create new behavior only modified the interface of the object.
Today I continue studying the adapter pattern and learn the differences between the Adapter and Decorator design 
patterns.

#### Day 1431 Adapter Pattern

Today I have been studying the Adapter pattern; the Adapter pattern permits that one object interact with another 
object that requires another interface, for example, if your C needs to interact with object A but object A requires 
a unique interface, you can create an adapter that works as the men in the middle between both objects and permit the 
interactions.

#### Day 1430 Phoenix Project Book

Today I have finished reading the Phoenix Project book, the history related in the book was funny really
funny, when I am reading the book I remember some things that happen at the work (joy moments).
I believe that DevOps is a great set of practices that every IT organization needs to follow, in the work we are 
currently working into a DevSecOps operation environment, but most of the time we cannot realize the practices well, 
maybe we can take some shortcuts to achieve something or our deployment process take long time like days to be 
completed.   

#### Day 1429 Continue Maven and Build Artifacts

Today I continue working on how to create Java libraries package in a .jar file and next upload the artifact into a 
repository, I try to upload the .jar file into a nexus repository running in Docker container, but I have some 
problems with the uploading process, I need to continue investigating this issue.
Also, I have the doubt about how to create the package automatically with a GitHub action.
I see some Java libraries that in the GitHub repository have built the .jar files with versioning ready to download 
and test.

#### Day 1428 Java Artifacts

Today I have needed to investigate how to create a Java library with a basic functionality like parse a String to 
a CamelCase style, then package the library in a Jar Java artifact and upload the Java artifact into a Maven 
repository, the final step is use this previous library created into a new Java project. 

#### Day 1427 Command Pattern

Today I have studied the Command design pattern, in the past I cannot find a real use case for use the command
pattern, well, I cannot understand the command pattern in a good way, but now studying and practicing more and applying
TDD with the book lecture I am understanding the command pattern better.
The easy definition of the command patter is, you have an object called command in this command object you can
store a receiver this receiver needs to know how to execute the command, and you have another object called invoker,
the invoker has the responsibility to execute the command.

#### Day 1426 Back to Work

Today I returned from my vacation to work, and my first day back brought several changes to the team.
I managed to complete some Java code tasks at work.
Now, I need to establish a new routine for my life
and ensure that I prioritize activities that will positively impact my career.

#### Day 1425 End of Vacation

Well, today my month vacation was completed,
I cannot achieve my career goals in my vacation days like finish reading the head-first design Patterns book,
but I continue reading two books making some Java code for book exercises.
My most important challenge to complete in my vacation was my change of home activity,
I need to move from a different city to work in the office at least two days each week.

#### Day 1413 Dependency Inversion

Today I started to study the dependency inversion principle.
In the past I studied the principle without understanding in a good way,
but now I want to gain a great acknowledgement about this.
Some things continue obscure in my mind about Object-Oriented programming and clean code.

#### Day 1412 Factory Method Pattern

Today I have studied the factory method pattern.
In the past, when I studied this design pattern, I had some doubts about how it works or in which real-life scenarios
can be useful.
I don't know that you can see the Factory Method pattern as a framework to create a family of objects related to a type.

**Day 1 - 50 HTML - CSS - Javascript**  [here](./day0-50.md)</br>
**Day 51 - 100 Javascript** [here](./day51-100.md)</br>
**Day 101 - 150 Javascript** [here](./day101-150.md)</br>
**Day 151 - 200 Javascript** [here](./day151-200.md)</br>
**Day 201 - 250 Javascript and start React JS** [here](day201-250.md)</br>
**Day 251 - 300 Javascript - React JS** [here](day251-300.md)</br>
**Day 301 - 350 Javascript - React JS and start Node JS** [here](day301-350.md)</br>
**Day 351 - 400 Start learn MERN stack** [here](day351-400.md)</br>
**Day 401 - 450 MERN stack - Docker - Typescript - TDD** [here](day401-450.md)</br>
**Day 451 - 500 Object Oriented Programming** [here](day451-500.md)</br>
**Day 501 - 550 Data Structures and Algorithms** [here](day501-550.md)</br>
**Day 551 - 600 Java**</br>
**Day 601 - 650 Java** [here](day601-650.md)</br>
**Day 651 - 700 Java and Spring Boot** [here](day651-700.md)</br>
**Day 701 - 750 Java | Spring Boot | MySQL** [here](day701-750.md)</br>
**Day 751 - 800 Java | Spring Boot | MySQL** [here](day751-800.markdown)</br>
**Day 801 - 850 Java | Spring Boot | OCI** [here](day801-850.md)</br>
**Day 851 - 900 Java | Design Patterns** [here](day851-900.md)</br>
**Day 901 - 950 Java | Design Patterns** [here](day901-950.md)</br>
**Day 951 - 1000 Java | Design Patterns** [here](day951-1000.md)</br>
**Day 1001 - 1050 Java | New Job** [here](day1001-1050.md)</br>
**Day 1051 - 1100 Java | Python | Cloud Computing** [here](day1051-1100.md)</br>
**Day 1101 - 1150 Java | Containers | Cloud Native Development | OpenShift** [here](day1101-1150.md)</br>
**Day 1151 - 1200 Java | Containers | Python | Security** [here](day1151-1200.md)</br>
**Day 1201 - 1250 Java | Python | Security | English** [here](day1201-1250.md)</br>
**Day 1251 - 1300 Java | Python | Security | English | Soft-Skills** [here](day1251-1300.md)</br>
**Day 1301 - 1350 Java | Python | Spark | Microservices** [here](day1301-1350.md)</br>
**Day 1351 - 1400 Java | Python | Design Patterns | Microservices** [here](day1351-1400.md)</br>

