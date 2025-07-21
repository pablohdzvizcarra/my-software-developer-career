# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is
invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

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
