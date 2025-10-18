# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is
invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2198: Continue Studying about File Database like SQLite

Today I have been working how works databases that save their data into a physical local file like `SQLite`. One of the concepts that I studied today was the `Cursor` concept, a cursor is used to know the current row position within a table, also it is used to write data to the file without do the offset calculation.

### Day 2197: Refactoring Code to Support a new Library

Today, I updated some Java code to use a newer library version. I don't understand why, from version 8.6 to 8.8, the library underwent multiple changes, rendering our code incompatible with the new library APIs. The newer version was only a minor change, and I recall that minor changes usually don't break anything. However, the library maintainers apparently wanted to break the clients' code.

### Day 2196: Continue with C Project

Today I continue working on my C project, I completed the tutorial in which we create some unit tests for the application with Ruby. For the moment the SQLite database clone supports `insert` and `select` operations, but the data is saved only in memory, in the next section we will do the logic to persist the data into a physical file on disk.

### Day 2195: Fast Producer and Slow Consumer

Today, I was debugging a classic software engineering issue: a fast producer and a slow consumer. In this scenario, the most common errors are performance degradation and exhaustion of physical resources. My problem was related to the latter because our producer fills up a disk partition with data faster than our consumer cleans it up. Things always go wrong when you least expect it, so it's important to validate edge cases and performance.

### Day 2194: Do You Want Hard Things? Code Something on C

Today, I will continue working on my tutorial for building a SQLite clone in C. Most of the time, I have trouble understanding what the code is doing. C is a beautiful but difficult programming language. It's beautiful because you learn computer science fundamentals while coding in C. You are responsible for every variable you create and for managing your application's memory, such as allocating enough memory to create a type and deallocating it when it's no longer needed. This memory allocation stuff is really complicated at first, but it's amazing once you understand how it works. It's hard because most of the time, you need a lot of code to perform a simple function. With other languages, like Java, which have a lot of abstractions, you don't need to worry about most things. For me, learning C is a pleasure. I feel like a craftsman building something from scratch with only their own hands.

### Day 2193: New C Project

Today I started a new C project, I have the plan to build a basic SQL database like SQLite in C. I founded the following [tutorial](https://cstack.github.io/db_tutorial/) in which we build a SQLite database with basic features, I am having some problems to understand the code because I am not a good C programmer, buy at the sme time I feel like I am learning the Computer Science fundamentals while writing C code, memory allocation, pointers, bytes and other stuff are great.

### Day 2192: Reading Book

Today, I spent some time continuing to read the Patterns of Distributed Systems book. I reread the section on the Singular Update Queue pattern, which involves multiple producers adding messages to a queue and a single thread reading and processing those messages. This pattern ensures that messages added to the queue are executed in the order they were added.

### Day 2191: Pull Architecture

Today, I learned about pull systems. I have some code that sends a request to an HTTP server through a socket connection. The request is to perform a fast, asynchronous operation that only requires milliseconds. The client then needs to check if the operation was completed by sending commands to the server to ask for the operation status — a classic pull architecture.

### Day 2190: Replicated Log

Today I studied the `Replicated Log` technique used on distributed systems to ensure consistency in a cluster with N nodes. One of the main problems in distributed systems is that all the nodes that are part of the cluster, needs to have the same state, so any node can process client requests. Having a Log in which all the request are saved in the correct order, is a good way to have the same state for the nodes, but problems happens when the leader node fails and the new leader needs to ensure that the general state is the same in the remainder nodes, Paxos and Raft algorithms are a good solution for these problems. The replicated log technique is used to have a unique Log that is equal between all the nodes, so any node can use this log to terminate in the same state.

### Day 2189: Paxos Consensus Protocol

Today I studied the `Paxos Consensus Protocol`, used to achieve agreement in a distributed system, ensuring consistency and fault tolerance. Paxos it is very complicated to understand, the book explain how works the paxos protocol with multiple diagrams and examples. Paxos have different implementations that differ from the original, the protocol evolved during the time to continue adapting to the changes in the industry.

### Day 2188: High-Water Mark Pattern

Today I studied the `High-Water Mark` pattern used on distributed systems to know the last entry that was successful write to the Write-ahead log and was committed by the leader and the followers. This technique is used to after a node crash for any reason, when the cluster select a new leader, clients continue receiving valid responses because the nodes uses the last high-water mark index to know after each point the entries in their WAL file are valid.  

### Day 2187: Majority Quorum & Generation Clock

Today I studied the `Majority Quorum` and `Generation Clock` patterns. The majority quorum is used to determine how many nodes in a cluster needs to confirm that the request was processed to be successful, for example having a cluster of 5 nodes, we can say that the quorum is equal to 3 `Q = N / 2 + 1`, it is important to configure a correct quorum in a distributed system and also understand that a trade off for a high quorum is the application throughput, because if we setup a higher quorum a request require more time to be completed with success. The `Generation Clock` pattern is used to setup a correct events sequence, in a distributed system you could not rely on a digital or wall clock, you will need to ensure that the events needs to be processed in some sequence.

### Day 2185-86: Continue Studying Distributed Systems

Today, I will continue reading books on distributed systems. I learned that leader election algorithms, such as Raft and Paxos, are useful when you have a cluster with only a few nodes, such as 2-5. I also learned about the single queue update code pattern. In this pattern, we have a non-blocking queue to which multiple clients can send messages. The queue has one thread that polls and processes the messages. With this pattern, multiple threads can write to the queue, and the order of consumption is maintained. This queue is ideal for asynchronous environments where processing order is important.

### Day 2184: Cycle Buffer

Today I learned about the cycle buffer or circular buffer logging technique. This technique involves writing data to a file and when the file is reach their max size, replace the oldest entries, with the new ones. To achieve the circular buffer technique you will need to have two pointers, a head and a tail, when the buffer is full the oldest entry is deleted to be replaced with the new one, this ensure that the file never growths more than their limit.

### Day 2183: Continue With Log Rotation Techniques

Today I will continue learning about log segmentation and how to create a snapshot of a log file to clean up the file to continue adding more entries. One of the main problems with log into a file is in some point the file growths and having all the logs in the same file is not scalable, for this reason we apply the log segmentation technique to create smaller files but also in some point this smaller files growths indefinitely if we do not take attention to the file. The most used technique is create a snapshot of the entire file, and next clean up the source file. Low-Water mark is a technique to clean up log entries from a file when they are not needed.

### Day 2182: Segmented Log

Today I studied and create a code example about how works the segmented log pattern on distributes systems to avoid maintain one big log file that contains all the applications logs in one place. With the segmented log technique, we split the application logs into N number of log files, we need to establish a max segment size that indicates how many bytes can store the log file and when the log file exceeds this limit, we need to create a new log file. I see this pattern in some application in my past, but I don't know all the context and the reasons behind this until today.

### Day 2181: Firewall Rules and Ingress/Egress Traffic

Today I had some problems when attempting to deploy my C file-receiver application in my Oracle server. For an unknown reason my server is not allow to receive public TCP connections, inclusively I could not use the `ping` command to check if the server is live. I have been troubleshooting this error for some time without success, I am following the Oracle documentation to configure and allow the traffic for my virtual network, but this is not working.  

### Day 2180: Sending a Big File in Chunks

Today I start to work on the code logic to send a big file in chunks to the server using the Socket connection. For the code logic I am reading chunks with a 1024 bytes length, the idea is to read these limited chunks and send through the socket one-by-one until the whole file was sent, for the client side I am working in the logic to read the chunks and save them into a physical file on disk. This approach is the recommend and most used in programming for sending big files through socket connection.

### Day 2178-79: Continue Working on File Sender Project

I have been working on my C file sender application, the client is able to create connections to the server and send the filename for the file to be storage in the server side. I am having problems to send a header to the server that indicates the length of the file to be processed, this header length is required because the TCP server needs to know how many bytes read from the client connection.

### Day 2177: Working on File Sender Project

Today I started a C project to learn and practice how to work with Sockets and file operations. The general idea is to build a server application that receive client connections, when a client is connected to the server, the server receives a file to be saved into disk in the server side. For the client side, the client application can send any file from the PC to the remote server. I am building the server in my Oracle server and building the client in my MacBook, I want to complete this tiny project over the weekend.

### Day 2176: File Operations on C

Today I learned how to perform basic file operations in C. I practice and learned how to open and close files in C to perform operations like write, read and append. To read the content of a file in C, first we need to use the `fopen` and having the FILE* pointer, we can use the `fread` function to read characters from the file. It is interesting how in C to do some basic file operations you will need to do the steps one-by-one rather than Java in which you have multiple abstractions to perform this operations faster.

### Day 2175: Start to Work on Heartbeat Mechanism

Today I started to code the logic to send heartbeat messages to the server when a connection is established between a client-server. For the moment in the server side I am using a basic example, have a separate thread that review each client connected to the server, and review if the client sends a heartbeat message in a threshold time, if the client is not sending a heartbeat message, we will need to close the socket connection and show a log indicating the error. My design is the server every 30 seconds validates the client connections.

### Day 2174: Fix ObjectOutStream Issue

Today I understand and fixed the issue that was happening when I write an object through an ObjectOutputStream. After understand the root cause of the issue, I discovered that was a code issue related about how I have the code logic, the main problem was I was creating multiple instances of the output stream from the same socket connection, due to this I had the exception. I redesign my code and fixed the error, for the moment I am working into refactor my code continue working on the next features.

### Day 2173: Java Socket Issues

Today I had some issues with my Java application that is working as a load balancer, the main issue is I had the following exception when the code is reading and Object from the socket connection: `invalid type code: AC`, Investigating more looks like this is an issue related to have multiple instances of a `ObjectOutputStream` or `ObjectInputStream` from the same socket connection. Tomorrow I will continue checking this strange issue to know how to fix it.

### Day 2172: Rest and Reading

During the weekend I took some rest from my coding activities, and I only continue reading the Distributed systems book.

### Day 2171: Coding Business Logic and DAta Layer App

Today I continue working on my application that implements the business logic and data layer into two separate applications. I started to work on the code logic to create the application that wll work as the load balancer, for the moment I am having problems to coordinate how the clients sends heartbeat messages to the server to maintain the connection active.

### Day 2170: Business Logic and Data Layer Application Separation

Today I have been studying the Business Logic and Data Layer application separation to achieve reliability and fault tolerance in an application through replication and data partitioning. If you create an application in which the business logic is stateless, you can create N number of replicates of the application, having replicates is a common technique to have the application working in the presence of failures and achieve scalability because when the workload is increased, you can add more application replicates. Adding replicates of an application is an example of Horizontal Scalability. The data layer (database) also can be divided into multiple replicates if it is necessary because the data growths and having all the data in one server is very expensive. To be able to have N replicates of the data layer, the common approach is to partition the data in shards, a shard is only a portion of the full data. I am working in a Java code example to practice these concepts, I will create a blog posts with my code example after complete it.

### Day 2169: Changing for a New Book

Today I decided to stop to read the C book and start to read the `Patterns of Distributed Systems` book. I felt bored and useless while reading the C book, I work with C in my work, but most of the time we only need to read and understand the C code and modifying it is not a common task. In the other part distributed systems and software architecture, is my daily problems. Really of problems arise when you have a distributed system, complex issues, complex flows to understand, debugging is hard and if you are talking with technical people, mots of the times they use technical definitions to say something like we need to improve the consensus algorithm to have a better election. I am excited for this new book it is very interesting.

### Day 2168: Code Refactoring

Today I was working into refactor some Java code. I only did little refactors like change the name of some functions and their parameters to better names, improve the logging of the application for some features and removing non-used imports in the code.

### Day 2166-67: Rest & Reding

I had a long weekend thanks to a holiday. During my long weekend I took some rest of programming and only read a few pages of a Distributed Systems book. I will continue studying distributed systems for the rest of the year and maybe work on my block storage project.

### Day 2165: C Object Types

Today I studied some of the available Object types available in C. In C everything that needs to hold a value is an object, and we have different types to represent the objects. I studied the `Character`, `Arithmetic`, `Enum`, `Floating`, and `Void` types. The character type is used to represent letters, like simple tokens `a`, `b`, etc. Arithmetic types are used to represent numbers like integer and longs. It is curious how in C we have a lot of types and subtypes to represent values.  

### Day 2164: C Book

Today I begin to read the Effective C book. I want to read this book to acquire the skill to read and understand C code, to learn how to manipulate bytes, how works bitwise operations and many other low-level concepts.

### Day 2163: Ansible

Today I begin to build an Ansible playbook to execute some test in a server. I am trying to review some metrics from the server using Ansible and if the metrics reach a threshold execute some action.  It is interesting how Ansible can automate these types of tasks and also literally you can create any thing that you imagine.

### Day 2162: Manipulating Bytes with C

Today I was learning how to manipulate bytes with C. How to create an struct with C and next insert the struct values into a buffer. It is really amazing how in C you manipulate bytes directly rather than just using Objects or String like in Java. I am learning multiple low-level topics and I will continue practicing with this in the following days.

### Day 2161: Socket and Client App

Today I started a basic exercise to write a Client-Server application that sends bytes over a socket connection with C and C++ code.
It is interesting how in C/C++ open a single Socket connection and read/send bytes is sometimes complicated. You will need to setup some things manually like the variables/structures to hold the data, I am following the basic standard that is send a 4byte header first with the size of the payload and next send the payload to the client, one of the main problems in C is when you use `write` or `read` system calls there is no guarantee that all the bytes will be write/receive through the connection, you will need to ad a mechanism that handle this.

### Day 2160: Complete DELETE Operation

Today I completed to fix the `DELETE` operation on my binary protocol. After change the protocol design to be a length-prefixed, I will need to modify how the client sends messages to the server and how the server send response to include a header value that indicates how many a bytes the server/client needs to read in the next call. Now I am practicing networking programming like TCP sockets and Binary protocols with C and C++.

### Day 2159: Understanding Distributed Systems

Today I completed to read the Understanding Distributed Systems books. This book was very great and although I complete to read it, I have some pending homework. I will need to read the Research Papers mentioned in the book also. The author recommends to read the papers to build the habit of read technical documentation and Research papers to learn new things or make deep dive into concepts. Also the author recommend two more books to read related with these concepts. Learning about Distributed systems to understand some concepts in my work and build amazing applications will be amazing.

### Day 2158: Goals Review

Today I reviewed my current monthly/year goals as a software engineer. I organized my current goals and change the priority of one of them due to some unexpect events that happened during the week, it is interesting how health conditions can modify your goals and how you will need to reschedule your planned dates. During the rest of the year I will focus in two main concepts, `Distributed Systems` and `Storage Virtualization Technologies with Java, JNI and C`.

### Day 2157: Alignment & Padding in C

Today I studied the Alignment and Padding concepts on C. Alignment was a new concept for me because in Java, Python and Go I remember that I never needed to learn this concept. In a C `struct` the alignment concept refers that the members of a struct needs to have then same length like the largest member, for example if we have 2 members one is a char short and the other one is an int, the C compiler by default append 2 unused bytes to the short element to have the size equals between the members. In C the member order affects how the compiler compile the other members. I read that for modern compilers is faster to read data from the memory when it is allocated with the same size like 2-bytes due to this the C compiler optimize the memory allocation. Padding elements are the unused bytes inserted by the compiler.

### Day 2156: Continue Working on Block Storage Project

Today I continue working into fix the things that were broken when I change my binary protocol design. I completed to fix the UPDATE client message and the created unit tests to test that feature. Maybe during the weekend I will take some free time out of my project to code something with C and learn some pending concepts.

### Day 2155: Fix Read and Update Logic

Today I fixed the Read logic on my binary protocol for my Block storage application. Now when the server process a Read request, first response with a header byte that contains the length og the following Read response, with this change my client know how much bytes needs to read from the connection to get the Read response. I am working into standardize my request and response frame and also refactor the properties names to achieve consistency and symmetry in the protocol design. Tomorrow I will need to continue working on the Update logic.

### Day 2154: Fixing Protocol Logic

Today I was working into fix my code for support the WRITE message the problem was with the protocol design change to send first 4 bytes as a header that indicates the message length, I will need to change multiple files in my Block Storage application to change the Decode and Encode logic. The good news are thanks that I had unit tests this fix is easy to apply and validates that the logic is working. I estimate that it will take me three more days to fix the code to support the new protocol design.

### Day 2153: Protocol Symmetry

Today I changed how my binary protocol creates and send the responses to the clients to follow protocol symmetry also I learned what is this principle in binary protocols.
Protocol Symmetry is when your binary protocol have the same design for request and responses, for example for request client, first my protocol requires that clients sends a header integer (4 bytes) to know how many bytes the server needs to read next to read the full request. The same happens for responses, the server needs to send a header and clients needs to read the exact number of bytes as the header value. Modifying my protocol to have meet this principle it is being difficult because I am also fixing my current integration and unit tests.

### Day 2152: Monitoring

Today I read the Building distributed systems Monitoring chapter. The monitoring chapter describes the most common industry techniques to monitor the health of a software application, to have a healthy application you need to configure a mix of some features like Metrics, Service-level indicators, service-level objectives, alerts and dashboards. The chapter is focused on the importance of setup these features and the importance of automate the most possible actions to fix an unhealthy system.

### Day 2151: Completed 50 days

Today I created the table entry that contains the skills leader and practicing in the last 50 days. I feel good with my progress during these days I dedicated most of my time to build an application to learn new skills. This application is hard and the technical level is very good, is not a basic CRUD or a simple HTTP server.

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
| 2101-2150 | Golang, Distributed Systems, Networking, Binary Protocols, Storage Systems, C, Bash, TDD | Built a Block Storage application in Go; Deep dive into storage, networking & distributed systems concepts | [View](./day2001-2500/day2101-2150.md) |
