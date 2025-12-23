# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is
invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2260-61-62-63: JNI and C Code

During these days I continue learning more about JNI Java framework, how to compile Java and C code using JNI. Also I started a new C project to put in practice all my learned knowledge on C building a Java/JNI/C project.

### Day 2259: Java JNI Issues

Today I learned more about the JNI interface. The Java JNI is used to use C code in Java code, with the JNI you can create a C library to perform X task, and next you can use that library with Java. This JNI library is a little complicated because you will need to compile the Java and C code in a compatible way. I will need to continue learning more about Java JNI.

### Day 2258: Organizing Task as a Software Engineer

I decided to take a break from software engineering for the last two weeks of the 2025 year, I want to use this time to review my completed learning materials, start to do reflections about my 2025 year as a software engineer, organize my pending learning tasks, like books/courses, organize my notes, etc. The next week I will have vacation time from work, so I want to appreciate my last days of 2025 work dates. I have pending to read some non-technical books, this is a good time to read it.

### Day 2257: Back to DSA?

Today I don't know why but I want to try to solve a DSA problem. I attempted to solve the algorithm `Partition Point in the Array
`, this is an easy algorithm and I felt very bad because I could not solve it in the 20 minutes of time that I want to spend. Tomorrow I will need to. continue solving the algorithm, really do DSA more frequently no matters if you are a experience engineer, DSA is a skill that requires continues practicing to avoid forget it or maybe just I am not very smart.

### Day 2255-56: Memory Management

Over the weekend I continue learning more about Operating system Memory Management. I focused in the Direct Memory Access (DMA) feature in an operating system to allow a process to read data from memory faster. The problem when you need to read bytes from a peripheral device like a network card or disk, and if you follow the normal flow `IO Device -> CPU -> Memory` is because the CPU needs to work as a mediator between the Main Memory and the IO Device, and most of the times do nothing with the bytes just pass through. DMA allows you to bypass the CPU mediator, so your process can read bytes from an IO device directly, without the extra CPU step. This is nice design that scale, but this contains some trade-offs like security concerns.

### Day 2254: Distributed Systems Issues

One of the main problems when having a distributed systems is coordination, how you ensure that the processes within the system works in synchronize and how to avoid the happens-before issues, this is one of the main problems with Distributed Systems. I was working today into understand the happens-before events that needs to be executed in the correct order for a distributed system, because if one of this event is not executed in the correct order, the processes communication is lost and a new connection needs to be established.

### Day 2252-2253: Java Object Oriented Programming

Today I learned how you can create software abstractions from hardware components. I was modeling some Java classes to represent hardware components, this was a very interesting exercise to learn how to abstract things. Also I write some `Perl` code, yes Perl code, to create some scripts. Perl looks like an interesting programming language, but one of the main problems that I am facing is Perl contains a lot of abstractions for text manipulation and other things, and you can do much thing with just 3 lines of code.  

### Day 2251: Debugging Code

Today was a hard day, I spend all my date debugging legacy code. Debugging legacy code is a spend task most of the times, when you need to work in a codebase without design, architecture and when the code is poor documented and leak of unit tests. I just can say, good luck when you need to debug legacy codebases.

### Day 2250: Coupling Components

Today I was learning the trade-offs about execute a component in the same JVM from the main application rather than runs the component separate as a separate application and communicate with the server like using Sockets. One of the main trade-offs is coupling, really this is a very hard problem, because if the component maintained by another team, starts to have issues (and really in some point every code have bugs) could be complicated which is the responsible about the issues. Maybe the bug is in the embedded code, but because runs together with the server code, looks like the problem here is the server. Another problem can be performance issues, that maybe can happen when the application start to receive more users that were planned.

### Day 2248-49: Memory Management

Over the weekend I continue learning about Memory management. It is interesting how the RAM memories have been evolving during the years to be more efficient and have better performance. I learned how the operating system interact with the RAM memory through the Memory Controller that is a special component to manage the memory. Also I learned interesting techniques to start to create programs with good performance, for example in Java how you order the properties/fields within an object matters when you do operations on that elements using next to each others or when you do multithreading programming. Another very interesting thing is how the RAM memory is builded, a RAM memory have N numbers of Banks, each bank have N numbers of Rows, each row contains columns and each column contains N number of Cells. Really the engineers that design all this stuff are very smart.

### Day 2247: Debugging a Live Process

Today I learned that you can see how a running process is distributed in different data segment sections, first you need to know the `PID` Process ID, you can get that PID using commands like `top` and `ps -ef`. I learned that when you know the PID on Linux you can use th `cat` command to know the data segments of the process like `cat /proc/PID(process ID)/maps`. The output of these cat command is how the process is divided in different data segments and the size of the data segments. It is very interesting how all this stuff works, really interesting.

### Day 2246: Wrapper Pattern

Today I was debugging some Java code that use a lot of wrappers to encapsulate the real code implementation. I am facing and issue to understand the code because the public class uses a wrapper, and that wrapper uses another wrapper and so on, I am not understanding why the code was created with this complicated pattern. A real example about how sometimes over-engineering can cause issues.

### Day 2245: Continue Reading Book

Today I continue reading the chapter about C Types. For the moment the lecture and the code exercises are very basic, this is the second chapter so I hope that with the next chapters will be more challenge. An interesting thing of C is compilers can compile and interpret the code in different ways, it is very important the compiler used to compile the code and also consider the host that runs the application.

### Day 2244: Continue with C book

Today I continue reading the Effective C book. For the moment its bored to read the book because I am reading the second chapter, and as a second chapter the code examples are very basic, but sometimes I face problems to understand the book content due to the low-level stuff.

### Day 2243: Command Execution Monitoring

Today, I worked on creating a logic to monitor how much time an external library requires to process a command. Some commands require forwarding to an external library for execution. One of the most common errors we see is that the library sometimes takes a long time to execute a command, resulting in errors. The main problem is that we do not own the library, and it is no longer supported. As an improvement, we want to monitor how long it takes to process commands to know when the library is working slowly. With this code, we can at least know when something goes wrong and attempt to discover a pattern.

### Day 2241-42: Java Proxy & New Book

During the weekend I studied and did a little code example about Java Proxies. A Java proxy works like a wrapper for another object, for example you have a Person object and you want that when your person object executes a method like `buyArticle()`, you want to log a trace for audit purpose, so you will need to create an special class that implements the `InvocationHandler` interface, and next use that class to create a proxy, the common behavior is when you execute a method on the proxy, this proxy uses the invocation handler, next the invocation handler do X thing to finally forward the request to the real object (Person). In the past I never use this pattern while coding, but in the work we use this pattern in some parts of the application. In other topics, I am giving up on learning computer science from video tutorials. I don't know why, but I find them boring. I prefer reading books and writing side projects to learn new things. I just started reading the Effective C book to expand my knowledge of C.

### Day 2240: Bit & Bytes

Today I started the Bitwise operations course section. I am very interesting on this section because on my work we do a lot fo bit manipulation operations with Java in our code to talk with the low-level components, I know that the course that I am doing is with C, but the concepts are abstract.

### Day 2239: Learning the Volatile Type Qualifier

Today I learned about the volatile type qualifier on C. This type qualifier is used to tell the compiler that the value of the variable will be storage on the main memory, this behavior is used to avoid problems when storing the variable on CPU registers or the Caches and changing the value in another agent running within the application like another thread.

### Day 2238: Designated Initializers

Designers initializers are a way on C to create an array or a struct with some values defined in the creation time, like creating an array of 50 elements and initializing the first 20 elements to 20 or creating an instance of a struct and initializing the name. This feature on C works like Constructors on Java when you can create an instance of an object with multiple constructors.

### Day 2237: Encryption Stuff

Today I learned about Encryption stuff like symmetric encryption, asymmetric encryption, encryption algorithms, ciphers, digest, hash functions, etc. Learning all of this concepts is very complicated for me, I don't have much knowledge about encryptions and their mathematical formulas.

### Day 2235-36: Heap Segment and C Layout App

Over the weekend, I learned more about the memory layout of a running process. I learned that the heap segment is used to store bytes allocated by the process, such as those allocated using malloc in a C application. Other programming languages, such as Java and Python, use garbage collectors, which automatically manage allocation and deallocation. I created a basic C application to see how it stores different parts of the code in different sections. It's interesting how all this stuff works, and how an operating system executes a process. It's amazing!

### Day 2234: Data Segment or Data Section

Today I studied that the Data Segment is a special space created within the RAM memory to store process constants and static variables. When a process is initialized, the program loader moves all this data into this special section called the Data Segment. When the code needs some bytes, it retrieves them directly from the Data Segment, using a simple memory address. The Data Segment is conceptually divided into different categories: read-only (like string literals) for values that must not change after loading, and read-write for mutable values like global and static variables that can be modified by the process

### Day 2233: Networking Issues

Today I was debugging a code issue related with a client losses the connection to a server for an unknown reason. The client is connecting to the server through a TCP socket connection, sometimes the connection is closed and the client is unable to reconnect with the server. I don't like networking issues because I don't have much knowledge about this stuff.

### Day 2232: Working with Length Array on C

Today I learned how to create dynamic arrays on C. I did some code exercises to declare an array and require the length of the array by user input in stdin, when the user enters the desired length, the array is created and some elements are added to the same array. It is interesting how in C you will need to create an array just with a defined length rather than in Java that you can create a List and add any quantity of elements that you want. Also I learned that you can create a dynamic array inside a `struct`, and next you will need to allocate memory for the array member within the structure like using `malloc`.

### Day 2231: Stack in Process

Today I studied how the operating system uses the Stack data structures to know how is process needs to be executed. The Stack used have a high to low mechanism, where the high value is the main function for a C application, and the lowest value is the final source code. When a process is executed, the Stack configure multiple pointers like Base Pointer and Previous pointer to know where the process execution is and which instructions currently are executed. It is interesting how the Stack uses just pointers to manage all the process execution.

### Day 2230: File Truncate Logic

Today I was reviewing a code logic to truncate a log file to reduce their physical size when the limit is reached. This truncation logic is very strange because when the log file reach the limit size, the code free some bytes in chunks of 1024 bytes. The logic uses a file stream to do the file operations and uses something called seek to position into the first bytes from the file, I remember that in C you can use the `fseek` function to move the pointer to any position within the file.

### Day 2229: Define C Preprocessor

Today, I studied the #define preprocessor in C. It is used to define symbolic constants that can be used throughout an entire application. It's similar to creating a static variable in Java that can be used to create configuration properties and other variables. I want to continue learning the C programming language by taking a course and doing exercises and applications.

### Day 2228: Process on Memory

Today, I learned that when a process is loaded into memory, it interacts with registers, L-caches, RAM, and SSD/HDD disks. The first step is to load the process into RAM. When the process is loaded, it sets up an internal process counter that maintains a pointer to the current instruction being executed. The process also stores variables in the code into the L-caches, depending on the data usage. The data is placed in the L1, L2, or L3 caches, and if a chunk of data is used less than others, it is moved to the main memory to free up space for other processes. It's interesting how efficient the CPU is at executing processes. Many algorithms must be used to optimize CPU usage.

### Day 2227: Program vs Process

Today I learned the basic differences between a program and a process. A program is the executable file that contains the instructions to be executed, in the other hand a process is an instance of the program that is being executed. Thinking in Java a program is a class file and a process is a Java object. Also I did some interesting test, testing a C application with the `lldb` debugger, I visualize how a process looks like when is loaded in memory, I see a lot of hexadecimal values on the debugger, really learning operating system while doing C code is really interesting.

### Day 2226: Learning about User vs Kernel Space

Today while doing my course, I learned about the Kernel and User space. The user space is where applications like your browser, code editor, your Java applications works, theses applications use resources from the operating system, and this resources can be shared with other applications. The kernel space is where the operating system works, as a C example, if you want to communicate with the network card, you will need to use a system call to the kernel to request access to the network card, because the kernel have direct access to the hardware resources. The kernel space have more privileges than the user space, this is because if an application in user space crash, it will not affect the kernel space, but if an application in kernel space crash, it can affect all the system. It is interesting how operating systems works.

### Day 2225: Learning about Cache on CPU

Today I was learning about the CPU have some caches called L1, L2 and L3, some CPUs have the L4 cache level. The general idea is the CPU can store data that is frequent access on these caches to fast retrieve the data rather than go to the main memory (RAM) to get the data. These level of caches are faster than the RAM memory. It is interesting how a CPU works when you study these concepts. I am doing a course about how operating systems works because I am tired of don't understand some conversations in my work when I talk with Hardware engineers, I spec that practicing C code can help me to understand all this stuff.

### Day 2224: Performance Issues

Today I worked into fix a code issue related with a logging module and how a bug cause performance issues in the code execution. It is interesting how a simple algorithm to append a new entry into an in memory logger can cause performance issues when the logs are saved into a physical file on disk rather tha in the memory buffer, the algorithm to append new log entries for the in memory buffer is classic append to an array, if we reach the size of the array, we need to remove the first element, next move the other elements to the left, to finally make room for the new element at the end. Working with files with C for the continues confusing for me and manipulating bytes also is a little funny.

### Day 2223: Throttle Mechanism

Today I worked into implement a throttle mechanism in code, A throttle mechanism (often called throttling) is a control technique used to limit the number of a process, function or action can be executed in a time window. For example we want to execute a heavy function just 10 times oer minute, so we need to configure a throttle mechanism to ensure the function can only be called the number allowed executions during the time window. This technique is very used in the industry and sometimes is confused with rate limit.

### Day 2219-20-21: Just Reading

Over the weekend, I focused on finishing a non-technical book. I also reviewed and analyzed my current software engineering goals for 2025. The end of the year is approaching, and I am thinking about what I need to do for my last moves of the year. I will continue studying distributed systems and applying the concepts to my current job. At work, we apply multiple distributed systems patterns and face complicated problems.

### Day 2218: Event Generators

Today I have been debugging an event generator code, this application design is very strange, we have this event generator that add events to a queue, next we have another component an event poller, that poll the events from the queue. I understand that this design is to do separation of concerns and maybe do the code moe reusable because we have N number of event generators. I want to continue exploring this pattern over the weekend and maybe do some C code to practice this.

### Day 2217: Complete C Project

Today finally I completed my SQLite database clone project. This project was amazing and learning a lot of things about C and databases, specially how works local database like SQLie. For the moment I don't know which will be my next step, but for the following days, I want to continue reading my non-technical book.

### Day 2216: Continue with C Project

Today I have been working on my C project to build a SQLite database clone with C. I am debugging a code issue in my `select` statement code logic; for an unknown reason, the select command is not working correctly—it shows rows with strange characters, such as numbers or bytes instead of strings. This suggests there may be an issue with data encoding, memory handling, or string formatting in the select or insert code logic.

### Day 2215: Performance Issues

Today I worked into fix a code issue that is related with poor performance in a logger feature. The problem with this code was does not implement truncation logic for the logs files, the coe just removed N number of bytes at the start fo the file and next append the new entries. This coe behavior generate performance issues and because we use a lock mechanism every time we want to append a new entry to the log, you ca imagine the bottleneck in a high throughput environment. I fixed the truncation logic and with this change the code works as expected.

### Day 2212-13-14: Weekend Break

During the weekend I take a break from coding activities. I just read non-technical books and today Monday I continue working on my current learning tasks. I have the plan to complete my current learning activities and next start with a very big new one.

### Day 2211: Coding Tired

Today I don't know why I could only code for some time, I felt really tired and without desire of code, I continue working on my C project and for the moment I am having multiple code issues related with the logic to split and create leaf nodes for root nodes inside the binary tree data structure.

### Day 2210: C Macros and Preprocessor Directives

Today I learned what are C macros and how you can compile your code to be compiled in different ways using preprocess directives. A macro is just piece of code that is replaced before the compilation process for the text content, we can define a Macro using the `#define` directive, normally macros are used to define constant values, but also we can create inline functions as Macros. Also with Macros we can use preprocessor compilation directives using the `#ifdef` directive to check if a directive was defined in the compilation process.

### Day 2209: Versioned Value

Today I read the chapter to learn about the versioned value pattern. On this pattern the general idea is have N number of versions for a value in a Key Value distributed data store, for example for the key=0090 and value="John" if we want to update their value from John to Mark, we store something like key=0090, version=1 and value="John", we can update the value for the key and increment the version to 1. Using this pattern clients can retrieve the value for a key with their historical values, this technique is very useful when you want to check old values for a key. Implementing this pattern with code, requires a data structure that supports this operation and the usage of locks working in a multithreading environment.

### Day 2207-08: Learning about Kernel and User Space

Today I was learning about the Kernel and User space in Linux systems. The kernel space in a linux system is used to executed application directly in the kernel, these applications runs with special privileges and have direct interaction with the kernel. The other applications like web browser, the terminal, the file explorer runs on the User space, this space is designed to execute applications in a secure way. For the moment I have just a little knowledge about this two amazing concepts, but I will continue studying these topics.

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
