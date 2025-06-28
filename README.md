# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is
invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2086: Coordination

Today I started with the study about the Coordination in distributed systems. One important thing in distributed system is the system model. System model is a way to describe how the systems behaves in the processes, communication links and timings.
One of the communication link models is: **Reliable link model**, this model guarantees that the message between two nodes always reach their destination. If an error occurred an one Node don't receive the message, the message needs to be retransmitted until it is acknowledge. Process Fault models: **Crash recovery model** is a model designed to restart the node when something wrong happens, the Node crash but have the ability to restart itself. Timing models: the **Synchronous** model manage the communication between the Nodes directly and in a synchronous way, that means if Node A sends a request to Node B, Node A wait until Node B response. For me the general idea about theses models is describe how your system behaves, what you can expect of the system, and because any system is trade-offs free, you will need to choice how model is better for your system. For example in a video game the **Reliable Link Model** could not be good, because if some package is lost is better to process the next packages rather than attempts to process stale packages.

### Day 2085: TCP, TLS, UDP, DNS, HTTP

Today I completed to read the first chapters of the book that covers the basics of networking and the TCP, TLS, UDP, DNS and HTTP protocols. There is a lot of stuff to learn about networking, after fours years working as a Software Engineer, I can say that I am beginning to understand what happens with a simple request like `https://www.google.com`. Also the next time that I see a Socket connection error or exception I think again about what demons is happening now.

### Day 2084: Domain Name System (DNS)

Today I studied the Domain Name System (DNS) reading the Understanding Distributed Systems book. The DNS is a distributed system
that translates URLs into IP addresses. Do you know what happens when you type a URL in your browser like `https://www.google.com`?
The browser needs to know the IP address of the server that host the website. To get the correct IP address, there are multiple steps involved, from the browser site only it's a call to the DNS server, and next the DNS needs to make multiple recursive calls to other systems to get the correct IP address. A normal flow can be like this: [Browser] -> [DNS Server] -> [Root DNS Server] -> [TLD DNS Server] -> [Authoritative DNS Server]. I know there is a lot of stuff to learn here, but is really interesting.

### Day 2083: Congestion Window

Today reading the Understanding distributed systems book, I found an interesting concept that was hard to learn: the Congestion Window.
The `Congestion Window` is a TCP concept that defines how many bytes can be in flight at a given time. Bytes be in flight means how many bytes we can send to the receiver without receive an acknowledgment from the receiver. There are some magic things to understand about the `Congestion Window`. The congestion window size is calculated dynamically depending of how many bytes the receiver is acknowledging to the server, if the receiver is acknowledging a lot of bytes, the congestion window size will increase, but if the receiver is not acknowledging the bytes, the congestion window size will decrease. The primary functionality of the congestion window is avoid the network congestion.

### Day 2082: Network

Today, I began learning about networking by reading the Understanding Distributed Systems book. In the past, networking was one of those things I tried to avoid because understanding some of the concepts requires time and effort. Learning a new framework is more fun than learning what a TCP packet is, what the packet headers are, and how two applications can communicate through the TCP protocol. Now, I understand that these concepts are very useful, especially in my current team.

### Day 2081: Understanding Distributed Systems

To learn more about working with distributed systems, I started reading the book Understanding Distributed Systems today. I love how complex it is because there's always something new to learn: a new pattern, architectural design, bug, interesting decision, or obscure code. The downside is that it's sometimes difficult to understand how things work, and it's impossible for me to maintain a mental model of each component in a distributed environment. Most of the time, I create a diagram to understand a big, complex system like Kubernetes.

### Day 2080: This Doesn't Work

Today, I will continue working on my shell project. I'm facing a strange issue that's preventing me from continuing to develop the shell. I don't know why, but the environment in which I'm testing my shell is not functioning properly. The course provider manages this environment, and the problem is that the unit tests are not working properly. I am creating my shell using Test-Driven Development. My shell project is fully tested in my local environment, and the test case that fails in the course environment passes without issue. Today, I tried many times to get it to work, but was unsuccessful. I will spend more time on it tomorrow. Maybe I can fix the test case. If not, then maybe I will leave the course. I don't know yet. I just want to say that this sucks.

### Day 2079: Learning How to Work With Files in Golang

Today I learned how to work with files in Go. I needed to start with the implementation of the redirection operations in my shell project.
I am doing TDD, so I needed how to design my code to be testable. I learned basic operations like create a file, check if a file exists,
and write an string to a file. I begin to work on the `>` operator, for the moment this operator is the easiest to implement because
it only needs to redirect the output of a command to a file.

### Day 2078: Completed Quoting in Lexer

Today I completed the quoting logic in my Lexer. The Lexer now supports single quotes, double quotes, escape
characters, and backslashes. I don't know why but when I completed the third section, the remainder 3 sections
works with the same code logic. I am learning a lot about how a shell works internally, how a Lexer works, and how
to parse a string and split a string into a command and arguments. Tomorrow I will continue with the shell project,
the next module to be implemented is the redirection of the command output to a file.

### Day 2077: Continue with Issues in Lexer

Today I continue fixing some issue sin my Lexer. For the moment if the user inserts a strange string input like
`"echo /tmp/data/f'/'89 /tmp/dog/f'88"`, my Lexer logic is having problems to parse the `/tmp/data/f'/'89` chunk,
I fixed this issue adding another `if` statement in the logic, but I continue with issues when the user input have
multiple escape characters, single and double quotes, backslashes, etc.

### Day 2076: Issues While Supporting Escape Characters in Shell Project

Today I had a lot of issues adding the support to escape characters in my shell project. The problem is in the lexer
logic you need to add some rules to detect when the user inserts an escape character in any part of the input string.
If the user inserts the escape character `\` outside quotes, the character needs to be ignored, but if the user inserts
between single or double quotes, you will need to include it in the final result. Imagine the problem when you have a
command like the next: `echo \java\ "is the \best programming 'language' in the \world"`, you will need to have good
state rules to parse the user input into a valid command.

### Day 2075: Supporting Single Quotes and Literal Strings

Today I supported the usage of single quotes inside the input string in the shell. Working on this feature was
complicated because I needed to refactor my `Lexer.Tokenizer` function to detect when the user input contains a single
quote. For example, a user sent as input a string like: `echo hello 'world  friends'`, for the previous user input, the
lexer needs to read the first chunk using whitespace as delimiter. The left elements after the command are known as the
arguments, and the Lexer logic needs to create two arguments, one is `hello` and the seconds is `world  friends`.
For the moment my `Tokenize` function returns a struct that only contains a `Command string` and `Arguments string[]`.  

### Day 2073–74: Building a Lexer for my Shell Project

During the weekend I started to build a Lexer for my shell project. I started with the coding part for the lexer, for
the moment I support parse basic strings into command and argument like `echo hello`, supporting this behavior was some
easy because I only needed to a logic to first get the command from the string and second read the argument or
arguments and because I am following TDD while writing the code, was very easy refactor the usage of the Golang
`strings` package for my Lexer. Supporting the Literal string values like echo 'hello    world' was more complicated
and make my brain in pain for some time, but in the end I can implement the feature without using AI to write the code.
I am feeling with my progress because I am using only AI (Gemini) for basic code Golang tasks.

### Day 2072: Supporting CD and Relative Paths

Today I added the support for the `cd` command in my own shell, HOME path and relative paths. To implement the `cd`
command I used the `os.Chdir` function, with this golang function you can support the command in your shell.
This command also supports relative paths, so you need little effort to add this feature. Supporting the `PATH` took
more steps, first you will need to read the PATH value from te operating systems. Second when you read the value you
also can use the `os.Chdir` function to move to the destination dir. Also, I refactored my unit tests following the
Table-Driven Test pattern, following this pattern is very, very great, you can add a new test easily and fast.

### Day 2071: Support PWD Command in Shell

Today I completed the support for the PWD command in my shell project. The `pwd` can be very tricky to implement because
in your PATH directory you can have the `pwd` executable and if you don't manage the pwd command as a builtin, you can
delegate the functionality to the executable. Creating the `pwd` functionality in your shell can be straightforward
because you only need to read the current working directory and send the absolute path to the stout to be consumed
by the client. Also, I learned that **builtin** commands are executed by the shell, the shell is responsible for the
command behavior.

### Day 2070: Completed Redirect Commands to Executables

Today I completed the feature in which the use inserts a command to the shell, and the shell validates if there is an
executable configured in the `PATH` directory, the command execution is redirected to that executable. I reviewed one of
my functions because it is huge, and my guess is, the function meets the Single Responsibility Function but can be
refactored internally dividing the function into short steps. Working on this project is teaching me how a shell works
internally; for me, it is great to understand these concepts.

### Day 2069: Building type and Redirect Command Execution to OS Binaries

Today I completed the `type` command in my custom shell. For the moment if the user inserts something like `type curl`
commands, my shell look if one of the directories in the `PATH` contains a binary that can be executed, fi the binary
exists my shell sends to the user the output like `curl is /usr/bin/curl`. Also, I worked into implement the feature to
delegate the command execution to the OS binaries using the `exec.Command` golang function.

### Day 2067–68: Starting a new Project

I decide to take a rest from Java, Concurrency, and Multithreading to build a project for fun. I am working into create
a Shell that accepts commands like `echo`, `cat`, etc. with Go. The shell needs to work like a REPL program and execute
the provided commands with builtin instructions or delegate the command execution to the operating system.

### Day 2066: How to Group Objects

Today I learned multiple logical configurations techniques to group `Objects` that represent Physical Drives in a
Storage System. In a Storage System or Software you can have `N` number of physical or virtual disks to save data, these
disks need to be grouped into logical representations for better administration of them. We group these disks in fixed
groups like 16 elements, 32, and so on. With Java, we can have multiple options to store elements in Data Structures
like Arrays, Queues, Stacks, Trees, Map, etc.

### Day 2065: Completed Java Concurrency and Multithreading Course

Today I completed the **Java Multithreading, Concurrency, and Performance** Udemy course. This course was good, and you
need to have a Java Intermediate-Advanced level for the coding exercises because some of them are very technical. During
the course, I learned a lot of things related to the JVM tools that we have to create multithreading and performance
applications. I learned what virtual threads are, how to work with them, and the differences between a normal OS thread
and a virtual thread. At this moment, I never work with virtual threads in my work. I have the plan to continue
investigating more concurrency and multithreading patterns that Kubernetes uses and create applications following those
patterns to practice the concepts learned on the weekend. You can found the course link in
the [Courses Completed](./courses-completed.md) file; I have the plan to register my future learning activities to
separate Markdown files.

### Day 2064: Making Simple Mistakes

Today while debugging an issue in an application, I made the basic mistake that connects to a different server by SSH
and start with the debugging; this cause me to lose sometime because I don't understand why I don't see the application
logs if was connected to the correct server, so please next time that you need to connect to a server, ensure that the
server is the correct. In other topics I learned the trade-offs about Non-Blocking IO operations in software, and the
biggest trade-off is the code maintenance. One of the most common issues with the Callbacks is the `Callback Hell`, when
you have multiple callbacks and the next callback depends on the answer of the previous and so on. Multithreading
applications are arduous to debug and sometimes to read, and a Multithreading application that uses Reflection is doubly
hard to read and understand.

### Day 2063: Message Order

Today I worked on an interesting issue. The main problem of the issue is the code expects to receive some messages in a
specific order. For example, the first message with a wrong response, the second is correct, and the third is wrong,
what
happens if the code only waits until receive two responses. The normal flow is first wrong, second correct, but if the
third message is received as a second? The code ends up with an issue due to this bad logic. I am investigating
architectures that fix this problem, maybe validating if the messages are correct rather than skip of configure the
code wait for more responses.

### Day 2062: Thread-Per-Task/Response Pattern

Today I studied the `Thread-Per-Task` concurrency pattern. This pattern is used when you want to execute multiple tasks
concurrently to avoid having Clients waiting for a long time because maybe your application needs to execute an IO
operation. IO operations are expensive to be executed, and most of the time you want to process multiple requests for an
IO operation at the same time. The `Thread-Per-Task` pattern is used to execute a task in a separate thread, the rule is
you needed to use the same number of threads equal to the same number of available cores in the host. You can create `N`
number of threads you want depending on your computer resources, if you create a lot of threads and your computer can't
support them, you will get a Memory exception. Sometimes if you create a lot of threads, your application performance
will be bad rather than having only one thread executing all the tasks; this is for the context switch problem.

### Day 2061: Networking Communication by Peers

Today I studied the Peer concept in networking. A peer in just one of the elements in a network connection, for example,
you have more than 1 TCP sockets that are sending messages between them by the network; each TCP socket is Peer in the
network connection. Most of the time when you need to ensure that all the messages were sent to the other peers, you use
an `Acknowledge` mechanism, and to know who is the peer that send that message you use a Peer ID, this Peer ID is the
way to you know which TCP socket sends the message and also what message do you want to validate. Studying all these
concepts is very confused sometimes, there are a lot of things to learn in networking.

### Day 2060: Back to Jetbrains IDEs

Today I apply refactoring to this code repository. I had my history entries in the bottom of the file in a basic format;
to have a better look, I organize them in a table with four columns. Organizing my history entries, I felt good with my
progress over the years studying and working as a Software Engineer. It is a pleasure to see your hard work generate
incredible results.

### Day 2059: Studying Kubernetes Architecture

Today I studied the Kubernetes concurrency and multithreading architecture. I completed the Java concurrency &
Multithreading section 8 course learning about some concurrency and patterns and common issues working in multithreading
environments. I learned two interesting concepts. The first is how Kubernetes manages a Controller-Manager pattern, that
is, we have a manager and this manager needs to sleep until a number of controllers are ready to work, like the Services
and Node controller. To be able to use this pattern with Java, we can use the `wait()`, `notify()`, and `notifyAll()`
methods. The second pattern was the Slow Critical Section issues working with multiple threads. When you have a block to
some shared resource, but for example, thread A needs 2 minutes to complete the action, and another thread needs to wait
until thread A completes its process. We can fix this issue by isolating and reducing the code that is inside the block
in Java. Learning about the Kubernetes architecture is opening my mind in a new way.

### Day 2058: Back Pressure

Today I learned the **back pressure** concept in software design. This concept is used to describe when we have a
producer pushing messages to a queue and the queue has a consumer reading the message, but for example, the producer
pushes 10/s messages and the consumer reads 2/s. In this scenario, the queue grows to a good size to handle all the
messages. To avoid this bad design, we need to apply a limit to the queue and stop the producer for some time after the
consumers leave the queue empty. Learning about Java multithreading will be good and hard at the same time.

### Day 2057: Failover Issues

Today I debugged an application issue. When something went wrong with Worker A, we needed to fail over to Worker B. For
an unknown reason, Worker B could not successfully execute the request. This issue is strange because the two workers
should work equally, and at any time, either worker can have the role of the main worker depending on the workload.
Tomorrow I will continue investigating this pattern/architecture to better understand common problems with this design.

### Day 2055–56: Multithreading & Kubernetes Architecture

I continued studying about Java Multithreading. This time, I studied the Java `Semaphore` class. With the `Semaphore`,
we can create multithreading applications easily. One of the most common usages of this pattern is in a
producer-consumer architecture. We have N number of producers, and maybe we can wait until a consumer reads a message
from a queue. So, we can use the `Semaphore.acquire()` method like a sleep until some condition is met. In this case,
the condition is another thread executing the `Semaphore.release()` method. Looking for a real example in which this
technique is applied, I discovered that Kubernetes uses this pattern when updating some objects using events that come
from an API with a Bounded Blocking Work Queue. I am working on a code implementation of this pattern for learning
purposes.

### Day 2054: Ansible & Docker

Today I dockerized an Ansible workflow within a container running on RedHat UBI image. My general idea was to create a
container environment to execute some Ansible playbooks; these playbooks require a specific Ansible, Python, and
Paramiko version to work properly. To avoid dependency issues in my machine and install a specific old version of a
dependency, I decided to execute the Ansible playbooks inside a Container. The final result was good, I can execute the
playbooks within the container, and I learned multiple things about RedHat UBI images.

### Day 2051-52-53: Watchdog

During that time, I continued working on the Java Multithreading and Concurrency course on Udemy. One of the main things
I learned was the watchdog mechanism, which monitors systems and detects lockdowns or dead systems. I had never used
this concept before, but I will implement it with Java code in my current project to detect when the system is down or
when there are deadlocked threads. I created a basic implementation of the system using Java code to simulate deadlock
states in some threads, leaving the watchdog to detect those threads and recreate or destroy them. I have completed 60%
of the course, and I will continue working on it in the coming days.

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
