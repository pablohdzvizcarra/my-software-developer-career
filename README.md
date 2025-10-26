# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is
invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2206: Idempotent Receiver

Today I learned the idempotent receiver pattern to ensure that receiver only process one time a request. In distributed system when we have more than one node for an application, it is very important that receivers (nodes) only process client's request at least one time to ensure consistency, imagine the issue when receiving request on server A, next this server forward request to server B, but server B crashes before acknowledge server A that the response was completed, if we have retry mechanism to send again the request for a missing acknowledge, server A sends again request to Server B and server B if it is not capable of skip duplicated request, will process again the request and terminates in an inconsistent state. Idempotent receiver have the ability to not process again a request that was proceeded.

### Day 2205: Continue with C Project

Today I continue working on my C tutorial project to build an SQLite database clone. I started to used Eclipse IDE with C because I use this IDE for Java and well for the moment is working good, it is better than VSC.

### Day 2204: Creating a Java Library

Today I continue working into create a personalized Java library to do some authentication logic. One of the main problems that are faced with this activity was my lack of knowledge on this are of the java world, in the past I never have the need to create my own library to do X task, but now I needed to do this. This exercise is helping me to understand modularity in software engineering. When you have clean and not dependent modules in your project, you can easily separate them as external libraries or separate packages.

### Day 2203: Eventual Consistency

Today I was studying the design of a technology that uses eventual consistency to ensure the data was copied to the target in some point in the future. Eventual consistency is a design technique used on distributed systems to ensure the data from one node is replicated to another node asynchronously to avoid application delays when copying the data. It is interesting that if you know the distributed system patterns you can understand how some technologies works in a high level way.

### Day 2202: How to Package Java Files

Today I learned how to package java compiled classes `.class` into a JAR file and next use the .jar file in another application. I learned that a .jar file is like a `ZIP` file that contains just files, and a MANIFEST.MF file that acts as metadata. You can create a .jar file with the following code `jar cf example.jar -C sourcecode .` where example.jar is the filename for the JAR and -C contains the compiled java classes to .class files, also this command respect directory structure so if you have something like `sourcecode/com/Funny.class` you create a .jar file with the same exact path, and next you can use the compiled java jar in another application like `java -cp "funny.jar:appdst" appa/src/TestingApp`. It is interesting how at the end everything is simple in the Java world, the only thing that you need is curiosity and use the terminal to compile and execute java application rather than use the IDE tools.

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
| 2151-2200 | C, Distributed Systems, Java, Networking (Sockets, TCP), Binary Protocols, Database Internals (SQLite clone, B-Tree), C++, Ansible | Building an SQLite clone in C; Deep dive into Distributed Systems patterns & C fundamentals | [View](./day2001-2500/day2151-2200.md) |
