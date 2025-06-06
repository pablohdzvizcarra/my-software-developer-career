# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2065: Completed Java Concurrency and Multithreading Course

Today I completed the **Java Multithreading, Concurrency, and Performance** Udemy course. This course was good, and you need to have a Java Intermediate-Advanced level for the coding exercises because some of them are very technical. During the course, I learned a lot of things related to the JVM tools that we have to create multithreading and performance applications. I learned what virtual threads are, how to work with them, and the differences between a normal OS thread and a virtual thread. At this moment, I never work with virtual threads in my work. I have the plan to continue investigating more concurrency and multithreading patterns that Kubernetes uses and create applications following those patterns to practice the concepts learned on the weekend. You can found the course link in the [Courses Completed](./courses-completed.md) file, I have the plan to register my future learning activities in separate markdown files.

### Day 2064: Making Simple Mistakes

Today while debugging an issue in an application, I made the basic mistake that connects to a different server by SSH and start with the debugging; this cause me to lose sometime because I don't understand why I don't see the application logs if was connected to the correct server, so please next time that you need to connect to a server, ensure that the server is the correct. In other topics I learned the trade-offs about Non-Blocking IO operations in software, and the biggest trade-off is the code maintenance. One of the most common issues with the Callbacks is the `Callback Hell`, when you have multiple callbacks and the next callback depends on the answer of the previous and so on. Multithreading applications are arduous to debug and sometimes to read, and a Multithreading application that uses Reflection is doubly the hard to read and understand.

### Day 2063: Message Order

Today I worked on an interesting issue. The main problem of the issue is the code expects to receive some messages in a specific order. For example, the first message with a wrong response, the second is correct and the third is wrong, what happens if the code only waits until receive two responses, the normal flow is first wrong, second correct, but if the third message is received as a second? The code ends up with an issue due to this bad logic. I am investigating architectures that fixes this problem, maybe validating if the messages are correct rather than skip of configure the code wait for more responses. 

### Day 2062: Thread-Per-Task/Response Pattern

Today I studied the `Thread-Per-Task` concurrency pattern. This pattern is used when you want to execute multiple tasks concurrently to avoid having Clients waiting for a long time because maybe your application needs to execute an IO operation. IO operations are expensive to be executed, and most of the time you want to process multiple requests for an IO operation at the same time. The `Thread-Per-Task` pattern is used to execute a task in a separate thread, the rule is you needed to use the same number of threads equal to the same number of available cores in the host. You can create `N` number of threads you want depending on your computer resources, if you create a lot of threads and your computer can't support them, you will get a Memory exception. Sometimes if you create a lot of threads, your application performance will be bad rather than having only one thread executing all the tasks; this is for the context switch problem.       

### Day 2061: Networking Communication by Peers

Today I studied the Peer concept in networking. A peer in just one of the elements in a network connection, for example, you have more than 1 TCP sockets that are sending messages between them by the network; each TCP socket is Peer in the network connection. Most of the time when you need to ensure that all the messages were sent to the other peers, you use an `Acknowledge` mechanism, and to know who is the peer that send that message you use a Peer ID, this Peer ID is the way to you know which TCP socket sends the message and also what message do you want to validate. Studying all these concepts is very confused sometimes, there are a lot of things to learn in networking. 

### Day 2060: Back to Jetbrains IDEs

Today I apply refactoring to this code repository. I had my history entries in the bottom of the file in a basic format; to have a better look, I organize them in a table with four columns. Organizing my history entries, I felt good with my progress over the years studying and working as a Software Engineer. It is a pleasure to see your hard work generate incredible results.

### Day 2059: Studying Kubernetes Architecture

Today I studied the Kubernetes concurrency and multithreading architecture. I completed the Java concurrency & Multithreading section 8 course learning about some concurrency and patterns and common issues working in multithreading environments. I learned two interesting concepts. The first is how Kubernetes manages a Controller-Manager pattern, that is, we have a manager and this manager needs to sleep until a number of controllers are ready to work, like the Services and Node controller. To be able to use this pattern with Java, we can use the `wait()`, `notify()`, and `notifyAll()` methods. The second pattern was the Slow Critical Section issues working with multiple threads. When you have a block to some shared resource, but for example, thread A needs 2 minutes to complete the action, and another thread needs to wait until thread A completes its process. We can fix this issue by isolating and reducing the code that is inside the block in Java. Learning about the Kubernetes architecture is opening my mind in a new way.

### Day 2058: Back Pressure

Today I learned the **back pressure** concept in software design. This concept is used to describe when we have a producer pushing messages to a queue and the queue has a consumer reading the message, but for example, the producer pushes 10/s messages and the consumer reads 2/s. In this scenario, the queue grows to a good size to handle all the messages. To avoid this bad design, we need to apply a limit to the queue and stop the producer for some time after the consumers leave the queue empty. Learning about Java multithreading will be good and hard at the same time.

### Day 2057: Failover Issues

Today I debugged an application issue. When something went wrong with Worker A, we needed to fail over to Worker B. For an unknown reason, Worker B could not successfully execute the request. This issue is strange because the two workers should work equally, and at any time, either worker can have the role of the main worker depending on the workload. Tomorrow I will continue investigating this pattern/architecture to better understand common problems with this design.

### Day 2055–56: Multithreading & Kubernetes Architecture

I continued studying about Java Multithreading. This time, I studied the Java `Semaphore` class. With the `Semaphore`, we can create multithreading applications easily. One of the most common usages of this pattern is in a producer-consumer architecture. We have N number of producers, and maybe we can wait until a consumer reads a message from a queue. So, we can use the `Semaphore.acquire()` method like a sleep until some condition is met. In this case, the condition is another thread executing the `Semaphore.release()` method. Looking for a real example in which this technique is applied, I discovered that Kubernetes uses this pattern when updating some objects using events that come from an API with a Bounded Blocking Work Queue. I am working on a code implementation of this pattern for learning purposes.  

### Day 2054: Ansible & Docker

Today I dockerized an Ansible workflow within a container running on RedHat UBI image. My general idea was to create a container environment to execute some Ansible playbooks; these playbooks require a specific Ansible, Python and Paramiko version to work properly. To avoid dependency issues in my machine and install a specific old version of a dependency, I decided to execute the Ansible playbooks inside a Container. The final result was good, I can execute the playbooks within the container, and I learned multiple things about RedHat UBI images.

### Day 2051-52-53: Watchdog

During that time, I continued working on the Java Multithreading and Concurrency course on Udemy. One of the main things I learned was the watchdog mechanism, which monitors systems and detects lockdowns or dead systems. I had never used this concept before, but I will implement it with Java code in my current project to detect when the system is down or when there are deadlocked threads. I created a basic implementation of the system using Java code to simulate deadlock states in some threads, leaving the watchdog to detect those threads and recreate or destroy them. I have completed 60% of the course, and I will continue working on it in the coming days.

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

