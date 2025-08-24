# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is
invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2143: Update Message

Today I started to code the logic for my Block Storage application to support UPDATE messages. The UPDATe message logic looks like similar to the WRITE logic, the unique difference is first we need to delete the old blocks with the data and next write the new locks. Tomorrow I will need to investigate if rather than delete the entire blocks, I can only update with the new ones. A delta update something like that.

### Day 2142: Client Connections

Today I refactored how my Block Storage application manage the client connections. I created a Client registry in which every client that connects to my server is registered, for the moment the registry only supports client registration and maintain a list with all clients connected with basic information like Address, Connection time and Client ID. In the future I have the plan to add more functionalities like rate limit for clients, security, authorization, etc.

### Day 2140-41: Peer Registry & Handshake

These days I continue working implementing the protocol handshake for my Block Storage system. After start to receive messages for write/delete/read files, the application first needs to execute a handshake with the client to validate that both the client and server talks the same binary protocol, if the client handshake messages is not sent correct to the server, the server returns a bad response with format like: status(1 bute) - code error (2 bytes) - endChar(1 byte). I implemented the server handshake validation and created unit test for the feature.

### Day 2139: Designing Protocol Handshake

Today I begin to work on design the protocol handshake for my binary protocol used in my Block Storage application. For the moment the protocol structure is: 3 bytes as the magic protocol number, 1 byte for the protocol version, 8 reserver bytes for the moment setup to zeros, 1 byte for the client ID length, I am not sure the size of the client id yet, the client ID and finally the termination character `0x0A`. I added the protocol design to my protocol docs and start to code the logic to parse the client handshake into a Golang struct for easy manipulation.

### Day 2138: Software Common Failures

Today I read the *Common Failure Cases* book chapter. On this chapter I learned the most common errors that can happen in a software application like Configuration, Resource Leaks and load pressure errors. Configuration errors are one of the most common type of errors and if you look in the internet you will find multiple examples that an easy task like configure a certificate can cause a lot of issues and problems for an error. The resource leak error is also another error that I found working as a software engineer, I remember the time when we have a non-limit backlog for a Kafka topic and this backlog growths until use the entire server disk space. I believe that reading post-mortem documents and RCA are one of the bst ways to learn from this errors.  

### Day 2137: Organizing Goals & Free Time

Today I organized my monthly goals as a software engineer. I refactor some goals and setup target dates for the rest of the month, I want to continue focusing on my Block Storage project and learning more about distributed systems.

### Day 2136: Complete Delete Feature

Today I completed the delete feature in my block storage application. When a client wants to delete a file that exists, first the application validates that the files already exists, get the blocks addresses from the metadata file, to finally delete all the blocks for that file. I develop the code for this feature following TDD methodology. Also I return a status error and error code when the client wants to delete a file that does not exists.

### Day 2135: Golang Channels

Today I studied how works Golang channels to catch errors that can be happen inside a Goroutine. Channels are a powerful Golang feature to share data between Goroutine, you can send data to a channel in a Goroutine and receive it in another Goroutine.

### Day 2134: Problems Supporting Delete Operation

Today I was working into a code issue related about the logic to parse the `[]byte` frame into a delete message operation. The problem is the code is validating boundaries using and offset(index) and the total length of the frame, but sometimes my logic cause fail positives or negatives, it is complicated developing the protocol and clients be able to send a frame with the correct structure, clients can write their own sending logic. Tomorrow I will need to continue checking the logic and thinking more about these problems.

### Day 2133: Developing Delete Operation in STGBlock

Today I started to work on support the deleted operation in my block storage application. For the moment I define the design of the `DELETE` operation, which will allow clients to remove files from the storage. I write the design in my binary protocol docs and start to implement id in code.

### Day 2132: Configuring Threshold

Today I was working in a coding tasks that involves setup a threshold in a counter when a condition is meet. A threshold is a value that serves as a limit or boundary in applications, if the application is working below the threshold, that means the application is not exceeding expectations. The general idea was configure the threshold with some condition, and when we receive N number of errors greater than the threshold, we trigger an action. I needed to do some Java and Bash code to implement this feature.

### Day 2131: Integration Tests for Read Message Feature

Today I wrote the integration tests for the Read message feature in my stgblock object storage in Go. I created a test client with the Golang testing library to connect to my server to send a message, and I verified that the server response with the expected payload. Unit testing in Golang are very good, I love how golang integrate the unit tests library in the `testing` package and the integration that have with the Golang ecosystem.

### Day 2130: Organizing Goals

Today I just took some time organize my goals and plan my tasks for the upcoming month. I want to code today but I avoid it because I want to take some free coding activities time. Like watching TV, reading books and spend time with my family.

### Day 2129: Supporting Read Message in Project

Today I worked into support READ messages in my block storage project. My project for the moment support Write and Read message from clients. A client can connect to the application and start to save and read files using the binary protocol. I am thinking into implement a handshake between the Client and Server because for the moment the server does not verify if the client that is attempting to create the connection talk the same protocol.

### Day 2128: Studying Caching & Continue with Project

Today I studied cache techniques and cache policies. Also I continue working in my `Block Storage` golang application.
I want to work tomorrow into implement the READ functionality in my block storage app. For the moment my app support WRITE operations to save files as blocks in folders, but I have the plan to create volumes and in that volumes store the blocks like in a real application.

### Day 2127: Client Response & Partitioning

Today I continue working on my Block Storage project developing the feature to send a response to the client when a WRITE operation is completed in the application. I needed to design the Client response in my binary protocol, I am using 7 bytes header with the following structure: `[status 1 byte][errorCode 2 bytes][payload length 4 bytes][paylod]`. I learned a lot of things working on this project, I am thinking into continue or maybe finished when completes the READ operation. In other topics I will also study about Partitioning in distributed system to increase the service availability and performance focusing on how NoSQL databases follow this pattern.

### Day 2126: Logging in Golang

Today I worked into refactor my code logs to the standard `log/slog` package. The `log/slog` package in Golang is a the new version of the `log` package, this package is used to create structured logs in Golang applications. We can add key-values pairs to the logs, to print in the console any value from a variable and also supports INFO, DEBUG, WARN and ERROR tags for each log. I am continue working on my block storage Golang project, for the moment I am working into after save the file into disk, send back a response to the client to indicates everything was good.

### Day 2125: Unit Testing

Today I was working into create some unit tests to understand how. code logic works. I could not create an entire unit test for the class because it is impossible to instantiate the class because have a lot of dependencies and some of these are static classes. The approach that I follow was create a unit tests and copy-paste the individual functions that I want to test into the test class and next in the unit test class call the functions like the original class. This approach is not the best but for the moment I want to understand how the code works and create some unit tests to validate the logic of the functions.

### Day 2124: Working on Handle WRITE Messages

Today I worked on the `handler` module for my block storage product. The handler module has the responsibility of handle the client messages and dispatch to the appropriate storage function like handle a WRITE message and dispatch to the storage function that write the file from the WRITE message into a volume as a block. Working on this module I found and issue with the logic that load the metadata object from the disk, the problem was the code to load/write the metadata object was not thread-safe and we can have race conditions issues with this code. I fixed the issue adding a `Mutex` to the code that load/write the metadata object.

### Day 2123: Developing the Parse **Logic**

Today I continue working on my `Object Storage` application. I fixed some unit tests that broken after apply some modifications and adding more validations in my parse logic. The parse logic is responsible to serialize the `[]byte` with the client request into a Message object.

### Day 2122: Continue with Block Storage Project

Today I continue working on my Block Storage project. I added a TCP server to accept connections from clients, the idea is N number of clients can connect to the block storage application to write and read data. For the moment the project supports Client connections and I am working into develop the `Binary Protocol` to communicate with the block storage application. I am doing the project following TDD, I am happy coding with Golang and this type of complicated projects.

### Day 2121: How Works Block Storage

Today I studied how the `Block Storage` technology works while doing some Golang code to start with the `write` operation. The general idea of the block storage technology is save any type of file into chunks, a file is divided into N number of chunks, next these chunks are saved into the underlying hardware like an SSD, HDD, etc. I implemented the write function to accept any type of file, next split these file into 256 kilobytes chunks, to finally save the chunks into a folder concurrently. For the moment I am using a simple .json file to store a basic implementation of metadata, the metadata for the moment is only the filename and their list of chunks location. Tomorrow I will continue working on this amazing project.

### Day 2120: Over-Engineering in Code

Today I was working on a Java code base in which I think that is a classic example of over engineering in software engineering. The code base have multiple interfaces as a services, but these interfaces only have one implementation, I don't know why people like to create interfaces and their implementation if they only create one implementation, I understand that it is necessary with unit testing, but the project does not have any unit tests. Other example the service class, have another class with composition and this class is the responsible to execute the logic, the service only works as a wrapper for the other class with the business logic, but the service does not offer any other functionality, only delegates the method call to another method. This is one of the most common problems that I see as a Java developer.

### Day 2119: Studying the Copy-on-Write Technique

Today I started to study the `Copy-on-Write` resource management technique. This technique is used to create a copy-on-time between two storage systems like virtual volumes. The technique requires a source volume (the volume with the information that wants to copy) and a target volume (the destination volume to store the information). I am doing a code example with Golang just to understand more this technology.

### Day 2118: Networking Stuff

Today I studied the DNS load balancing, Transport Layer load balancing and the Application layer load balancing. The DNS load balancing is a load balancer that works at the CDN level, you can have a pool servers configured and waiting for incoming connections, the CDN manages this load balancer, one of the most common problems with the DNS load balancing is needs to add or remove servers from the list. `Transport Layer Load Balancing` works at the Layer 4 on TCP, this is the most faster of the three because works in a low layer, but the problem is perform operations different from load balancing the traffic is hard and sometimes impossible. `Application Layer Load Balancing` is one of the most popular, this load balancer offers some techniques like redirect the traffic to non-busy servers, TLS termination, Rate limits, etc. I want to code a basic example of these load balancer to practice and understand more.

### Day 2117: Studying File Storage Architecture

Today I studied the architecture of the Azure Storage service. This storage service is used like Amazon S3, you can save static files with high redundancy, availability, resilient, etc. The Azure Storage service have a global DNS service, to access to a file the URL of the file is composed by the account name and the name of the file. Another component called Stream Manager is the control plane that manage communication between the high level code and the low-level code. When you want to save a file in the storage system, this file is saved into a logical construct called `Stream`, a stream is only a logical piece that is composed by data chunks that are called `Extent`, and extent is a chunk of the original file, imagine that for save a a file with 1GB of size, you split this file into 4 256MB chunks. Each of this chunks is replicated into multiple nodes using `Chain Replication`. It is interesting study this type of architectures, maybe tomorrow I work on a basic code example.

### Day 2116: Goals As a Living Document

Today I learned about how to organize my career and personal goals as a live document. The idea is to have all your career in my case software engineering and life goals into a document, this document can be a word document, text, notion or markdown file. I have configured 10, 5, 1 years goals and also some little goals maybe monthly to be completed. For the moment I scheduled some weekly goals to be completed this week, so I want to continue be focus on the important things.

### Day 2115: Partitioning & Sharding

Today I studied why partitioning is important on distributed systems. I studied the Range partitioning and Sharing partitioning. Range partitioning is when you split the data into `Shards` for a range of elements, like the half of the alphabet in `Node A` and the other half on `Node B`. Hash Partitioning is a technique in which you apply a hash to a key, and based on the result of the hashing you assign the element into Node. Partitioning is very important in distributed systems to ensure high availability, fault tolerance, reliance and scalability. Imaging having all the YouTube videos into a single machine? that was very expensive on hardware and also you have performance issues.

### Day 2114: Outbox Pattern

Today I studied the `Outbox Pattern` used to replicate transactions to multiple data stores or services in an asynchronous way achieving `eventual consistency`. The outbox pattern is easy to understand, you have a service that needs to replicate the transactions to other services and you don't want to use a `Two-Phase Commit` protocol because is a blocking operation. First you save the record in the database, next in the same database you create a table/connection that normally is called the outbox. Another service called `Relay Service` detects that a new record was saved in the outbox table and process the record sending it to the end service. If you think this pattern is like a state machine because at the end you end with a set of services with the same state, you can see the outbox table as the log.

### Day 2113: Multi-Version Concurrency Control (MVCC)

Today I studied that the Multi-Version Concurrency Control is a technique used in database to create high available databases to ensure read-only transactions are lock-free. The database design is very interesting, you have multiple version of the data and for each version of that data you have a timestamp. When the client send a read transaction, the database assigns a timestamp to that transaction, the database next select the appropriate version of the data based on the timestamp and returns to the client. If you have a old read transaction thanks to the timestamp you can also read a old version of the data, if you think this is a very interesting solution for this problem. I will continue investigating more this technique because is great.

### Day 2112: Configuring Linux

Today I modified my `.bashrc` file to display only the current directory in my terminal rather than show the entire path in terminal.
This configuration was necessary because I was working in a directory in which due to the large path, the terminal requires an entire row to show the path. I am fascinating about how in Linux you can configure anything.

### Day 2111: Bash Scripts

Today I worked into modify some bash scripts. This scripts are used to initialize an application, the scripts contains multiple validations to review if the binary used to install the application exists in the machine, validate the application version and depending of the application version, the application needs to be initialized in some specific way. Working with these type of bash scripts are frustrating for me because I don't work with bash frequently.

### Day 2110: Two-Phase Commit Protocol

Today I studied the `Two-Phase Commit`, this protocol is used to ensure that a transaction can be performed by multiple components.  In the two-phase commit protocol we have a coordinator component called the `Actor` and other components called `Participants`. First the actor sends a `prepare` message to all participants to know if they are ready to perform the operation, if all participants are ready the Actor continues with the next step that is send the `Transaction` to the participants to commit it. If only one participant is not ready to process the transaction, this transaction will be aborted. I am doing a code exercise to apply this protocol in practice.

### Day 2108-09: Write-Ahead Log

During the weekend, I studied the `Write-Ahead Log pattern`, which is most commonly used in databases to apply atomicity operations. The write-ahead log pattern ensures that the database has a copy of the data in case of an error when the client sends the data to be saved and an internal error occurs within the database. The process is as follows: `Client --> Database --> (Issues)--> Data saved on disk`. The write-ahead log pattern first saves the data in a file or data structure called a log. Next, when the data has been saved to the log file, it can be saved as a real record or the real data can be updated. The general idea of having a log file containing client operations is that it can be used as a backup for the original data because it makes it easy to perform redo or undo operations in the database. Currently, I am reading the 'Atomicity' chapter of the book and plan to spend some time on this chapter, preferring to learn one concept per day rather than a set number of pages.

### Day 2107: Application with Low Performance

Today, I investigated a software issue in which the `client` sends a number of requests to a `server`. These requests have a timeout of only 120 seconds (two minutes). The problem is that the server requires more time to process them, but it manages 32 TPS for that type of request. It looks like something strange is happening within the server that is degrading its performance and requiring more time to process the requests. My initial assumption was that the server was overwhelmed with many different requests and was unable to process the additional requests within the required time frame. I will continue investigating this issue.

### Day 2106: Java Class Path

Today I continue studying more about how works the class path in Java. I continue with my Java project to learn how to configure the classpath for a Java application with Apache Ant and Java only using the command line to execute and build a Java application. It is interesting how platforms like Maven and Gradle automate all this stuff, but when you have to manually do some operations using only the CLI for compile and execute a Java application like a JAR or a class with a main method if you only have experience creating and running Java applications with these tools you will have some problems to understand some concepts and how is builded and executed a Java app.

### Day 2105: Sharding & Graceful Degradation

Today I studied the concept of `Sharding` in system design. This distributed system design is used to split something into little pieces called Shards. Imagine that you have a big database maybe to improve the TPS in your entire system, you use `Sharding` in your database and divide the entire database into 10 smaller databases, with this technique your database will have better response times because you reduce the work that a single database needs to do like having more workers to do the job. We use this technique to have two instances of a service and divide the load that the client sends to these two services.

### Day 2104: Transactions in Distributed Systems

Today I studied about transactions in distributed systems. A transaction is a group of operations that needs to performed together to ensure data consistency. The most common example is you have an operation to add 50 dollars to a bank account and you will need to execute another operation for the same account to withdraw 100 hundred dollars from the same bank account, what happens if the account balance is 80 dollars, and for an error the 50 dollars operation does not happens-before the withdraw? The user could not withdraw the money. Most of the databases offers a set of properties know as `ACID` to ensure a transaction is executed in the correct order and were executed at least one time. `ACID` means, Atomicity, Consistency, Isolation and Durability. There are a lot of theory behind the `ACID` properties. Another important concept is `Concurrency Control`. Concurrency control are a set of protocols that ensure the data is good in a concurrency environment when multiple services can execute multiple transactions at the same time using the same target data.

### Day 2103: Read Repair and Replicate Synchronization

Today I studied the `Read Repair` and `Replicate Synchronization` models for replication in distributed systems. The Read repair is used when a manager request to read some data from a node, when the data arrives the manager send again that data to all nodes, the nodes next to review if the data state is equal for the copy they have, if the data is not equal the nodes can replace with the correct data version, this pattern is very interesting because work in a reactive way, nodes review their data state only when a Client ask for that data. In the other hand the Replicate Synchronization model works like a cron job, that sends the data state to all other nodes every N number of seconds, minutes and hours. Each of these models have their trade-offs and benefits.

### Day 2102: Free Code Day

Today I take a free code date. I want to take a free date because my brain needs some rest from code and software engineering topics. I watched some parts of the LexFridman podcast with DHH (creator of ruby on rails) one of the best programmers in the world for me and also a father of three like me.

### Day 2101: Memory Addresses and Pointers

Today while coding in C I learned something interesting. Working with strings in C can be a little tricky, for example if you have a string and you use that string to create a copy into another variable like: `char *new_data = old_data;`, that works but the `old_data` and `new_data` variables points to the same memory address, and if you clean up the `old_data` variable like `free(old_data);` you end having a `new_data` variable with a empty value, that was surprised for me because the compiler and the application continues working without issues with this behavior. I know that changing the value of a variable like in java `String data = null;` its possible but well I will need to learn the differences and how the C manage the objects in the stack and memory. For the moment I continue learning C and coding more stuff.

## History

| Days      | Main Topics / Technologies                                                                                  | Highlights                                   | Link                                   |
| --------- | ----------------------------------------------------------------------------------------------------------- | -------------------------------------------- | -------------------------------------- |
| 1-50      | HTML, CSS, JavaScript                                                                                       |                                              | [View](./day0-500/day0-50.md)          |
| 51-100    | JavaScript                                                                                                  |                                              | [View](./day0-500/day51-100.md)        |
| 101-150   | JavaScript                                                                                                  |                                              | [View](./day0-500/day101-150.md)       |
| 151-200   | JavaScript                                                                                                  |                                              | [View](./day0-500/day151-200.md)       |
| 201-250   | JavaScript, React JS                                                                                        |                                              | [View](./day0-500/day201-250.md)       |
| 251-300   | JavaScript, React JS                                                                                        |                                              | [View](./day0-500/day251-300.md)       |
| 301-350   | JavaScript, React JS, Node JS                                                                               | Learning MERN Stack                          | [View](./day0-500/day301-350.md)       |
| 351-400   | MERN Stack                                                                                                  |                                              | [View](./day0-500/day351-400.md)       |
| 401-450   | MERN Stack, Docker, TypeScript, TDD                                                                         |                                              | [View](./day0-500/day401-450.md)       |
| 451-500   | Object Oriented Programming                                                                                 |                                              | [View](./day0-500/day451-500.md)       |
| 501-550   | Data Structures and Algorithms                                                                              |                                              | [View](./day501-1000/day501-550.md)    |
| 551-600   | Java                                                                                                        |                                              |                                        |
| 601-650   | Java                                                                                                        |                                              | [View](./day501-1000/day601-650.md)    |
| 651-700   | Java, Spring Boot                                                                                           |                                              | [View](./day501-1000/day651-700.md)    |
| 701-750   | Java, Spring Boot, MySQL                                                                                    |                                              | [View](./day501-1000/day701-750.md)    |
| 751-800   | Java, Spring Boot, MySQL                                                                                    |                                              | [View](./day501-1000/day751-800.md)    |
| 801-850   | Java, Spring Boot, Oracle Cloud                                                                             |                                              | [View](./day501-1000/day801-850.md)    |
| 851-900   | Java, Design Patterns                                                                                       | First developer job                          | [View](./day501-1000/day851-900.md)    |
| 901-950   | Java, Design Patterns                                                                                       |                                              | [View](/day501-1000/day901-950.md)     |
| 951-1000  | Java, Design Patterns                                                                                       |                                              | [View](./day501-1000/day951-1000.md)   |
| 1001-1050 | Java                                                                                                        | New Job in a Big Tech Company                | [View](./day1001-1500/day1001-1050.md) |
| 1051-1100 | Java, Python, Cloud Computing                                                                               |                                              | [View](./day1001-1500/day1051-1100.md) |
| 1101-1150 | Java, Containers, Cloud Native Development, OpenShift                                                       |                                              | [View](./day1001-1500/day1101-1150.md) |
| 1151-1200 | Java, Containers, Python, Security                                                                          |                                              | [View](./day1001-1500/day1151-1200.md) |
| 1201-1250 | Java, Python, Security, English                                                                             |                                              | [View](./day1001-1500/day1201-1250.md) |
| 1251-1300 | Java, Python, Security, English, Soft Skills                                                                |                                              | [View](./day1001-1500/day1251-1300.md) |
| 1301-1350 | Java, Python, Spark, Microservices                                                                          |                                              | [View](./day1001-1500/day1301-1350.md) |
| 1351-1400 | Java, Python, Design Patterns, Microservices                                                                |                                              | [View](./day1001-1500/day1351-1400.md) |
| 1401-1450 | Java, Design Patterns, CI/CD                                                                                |                                              | [View](./day1001-1500/day1401-1450.md) |
| 1451-1500 | Java, Design Patterns, CI/CD                                                                                |                                              | [View](./day1001-1500/day1451-1500.md) |
| 1501-1550 | Java, Python, Data Analytics, CI/CD                                                                         |                                              | [View](./day1501-2000/day1501-1550.md) |
| 1551-1600 | Java, Python, Data Analytics, CI/CD                                                                         |                                              | [View](./day1501-2000/day1551-1600.md) |
| 1601-1700 | Java, Python, ReactFS, DSA                                                                                  |                                              | [View](./day1501-2000/day1601-1705.md) |
| 1701-1750 | Java, Go, DSA                                                                                               | DSA book                                     | [View](./day1501-2000/day1706-1750.md) |
| 1751-1800 | Java, Python, DSA, AWS Cloud Practitioner, Data Engineering                                                 | Data Engineering Learning                    | [View](./day1501-2000/day1751-1800.md) |
| 1801-1850 | Java, Python, Airflow, AWS, Data Engineering                                                                |                                              | [View](./day1501-2000/day1801-1850.md) |
| 1851-1900 | Python, Airflow, Cloud Computing, Data Engineering, Spark                                                   | Apache Airflow Certification                 | [View](./day1501-2000/day1851-1900.md) |
| 1900-1950 | IBM Cloud, Parquet Files, DSA, Python, Java, SQL, Spark, Airflow                                            | IBM Cloud Practitioner Certification         | [View](./day1501-2000/day1900-1950.md) |
| 1951-2000 | Java, DSA, Java Reflection, Concurrency, OOP, Networking, Storage Systems, Unit Testing                     | New Project and Team                         | [View](./day1501-2000/day1951-2000.md) |
| 2001-2050 | Java, Byte/Bit Manipulation, DSA, Concurrency, Multithreading, TDD, C, Networking, Makefiles, Sockets & TCP | Study Computer Science & Java Advance Topics | [View](./day2001-2500/day2001-2050.md) |
| 2051-2100 | Java, Golang, C, Concurrency, Multithreading, Networking, Distributed Systems, TDD, JVM, Java Dumps, JNI, Sockets, TCP, BitTorrent Protocol, Binary Protocols, Kubernetes Architecture, Docker, Ansible | Build a Shell & BitTorrent client with Go; Deep dive into Java Internals & Distributed Systems | [View](./day2001-2500/day2051-2100.md) |
