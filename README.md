# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2013: Graphs Time Complexity

Today I continue reading and studying my DSA book. I continue reading the chapter dedicated to the Graph data structure, for the moment I implemented the two algorithms most used to search for an element within Graph Breadth-first search and Deep-first search. Also I remember that a Graph have a `O(V + E)` time complexity that means V for the number of vertices and E for the number of Edges within the Graph. I have the plan to continue studying this DS for some days more.

### Day 2012: Dealing with Segmentation Fault C Errors

Today I continue working on my project about designing my own protocol over TCP for a client-server communication. Working on the feature to encode the message to hexadecimal values in the client before send the message to the server I face some C issues related with the memory usage. Working with C is difficult at the start because you will need to allocate to memory every array and also you are responsible to free the memory after used it.

### Day 2011: C Project

Today I worked on a C project. I am creating a Chat application in C with a basic client-server communication sending and receiving messages.

### Day 2010: BFS Breadth-First Search

Today I studied the BFS algorithm to traverse all nodes within a Graph DS. The core of BFS is traverse the Graph node by node using recursion. The first step is to review if the node is already placed in another DS (normally a Map) to maintain a registry if the node was visited. If the node was not visited we add the node to the Map and use recursion to visit the adjacent nodes, the general idea about have a Map DS is to avoid visit again nodes because remember in a Graph the nodes can have cycles. During the weekend I want to build a C project for fun and learning. 

### Day 2009: Graph Data Structure

Today I started to study about Graph data structure. I started with the theory about how is represented a Graph. A `Graph` can contains N numbers of vertex, vertex is like a node in a Tree. This Vertices are connected by edges and when two vertices are connected to each other are called that the two vertices are adjacent to each other. Graph theory is interesting and in my current project we use it in some algorithms. 

### Day 2008: Building autocorrect Feature

Today I completed a algorithm for an autocorrect feature for my `Trie`. The general idea was developer an autocorrect feature that fix a word with a typo issue like working needs to be changed by working. The algorithm follow basic steps, first we iterate over each character of the prefix argument, next we look if the character is present as a key for a node and if it's present we continue with the next character if it is not present, we choice the first replacement node for that key and continue working the word from that node. At the end we finish with a complete word. I feel good because I completed this algorithm from myself, I only read the steps and I figure out how to make the algorithm and code.

### Day 2007: Complete `collectAllWords` algorithm

Today I continue developing he algorithm to collect all the words from a `Trie` that starts with X prefix. I created one method that receives a prefix and returns a `List<String>` with all the words that start with that prefix. The algorithm use recursion to review the N number of nodes that start with the prefix.

### Day 2006: Trie Data Structure

Today I continue studying the `Trie` data structure. I created the insert and search functionalities only reading the steps to create those algorithms, I feel very good because I can understand the algorithm steps and next implement them with Java code. Also I am very happy because I am following TDD while writing code, so for me my code practice is working good good because my code is tested. Tomorrow I will continue working on an algorithm to collect all the words of a `Trie` that starts with X prefix.  

### Day 2005: Organizing Goals

Today I studied in the morning some C code, this time I started to create an application to review my current processes running in my ubuntu server. As a feature I printed in console the number of the process in bit representation. Also I did a review to my current 2025 goals and also my career goals, I completed to organize my April goals, on this month I want to focus on completed my DSA book, advance in my English course, learning more things required for my job and continue reding software engineering books.

### Day 2004: Low-Level Concepts

Today I studied some low-level things like bit, bytes, 16-bits, 32-bits, 64-bits and review the Java types available to represent numbers. A `bit` is the smallest unit of digital information and can be only 0 or 1, a `byte` is composed for 6 bits and can contain a value between `-128` to `127`, next we have the 16-bits that is only 16 bits grouped together that represent some value between `0 to 65,535`, also we have other types of bits groups like 32 and 64 bits, these quantity of bits are used to represent larger values like 1_000_000 million. Remember that computers only understand 0 and 1, so if you want to execute a instruction, you will need to send only bits as information, the compiler or the interpreter is the responsible to parse the numbers, strings, boolean etc into their bit representation.˝˝

### Day 2003: Coding and TDD

Today I worked in a code algorithm to deserialize a `byte[]` into a Java object. The interesting thing on this deserialization process is I am manipulating the byte[] by indexes, for example to extract the name value from the byte array, I will need to extract the 23-40 bytes, and next pase these bytes into a String. For me work on this code is an interesting thing because I never worked with bytes offsets in the past. I am following TDD for this code algorithm because the code have a lot of logic, TDD looks like a great option for create a good algorithm and made future code changes without break existing functionalities. 

### Day 2002: Sockets & C

Today I continue working on my little C project, for the moment I am doing a research about how to handle a socket client connection into a separate thread, my code now is following an approach about open a client connection -> receive the message from the client -> send a response to client -> close the socket. The problem with this approach is we need to open/close the socket connection to send and receive only a single message, and I want to only open the connection and maintains active after the client or server closes it.

### Day 2001: Completed Reflection Course

Today I completed my Java advance Reflection course. Really I learned a lot of things working on this course, the last part of the course was about best scenarios to implement Reflection, common errors implementing reflection like not create Reflection generic code and some security considerations.

### Day 2000: 2 Thousand Days of Code

Today I achieved 2000 days of coding. Really, this is a big milestone for me. This has been a good and large travel, but it is only the start of the journey. Amazing things are coming like C, Storage Systems, Java Advanced Topics, Concurrency, Networking, Test-Driven Development, Performance, and more fun. 

### Day 1999: Java Reflection Proxy

Today I learned how to implement the `Proxy` pattern in Java. A proxy object is like a wrapper that adds some extra functionality like logging, caching, etc., operations to a class without modifying the class itself. The main proxy idea is to have a class that contains an instance of another class by composition. Next, when the proxy class receives a request, it executes the extra functionality and then delegates the execution to the real object. Proxy + Reflection is a powerful technique. You can easily wrap any type of class with a proxy and reflection.

### Day 1998: Reading

Today I completed to read the **Tidy First** book. This lecture was good, I learned some tips and tricks to write better code and also I understand a little more why most of the times the company does not care of their code bases and why is most important for the company write fast code to deliver to the market that write good quality code.

### Day 1997: Reading Multiple Annotations

Today I learned how to mark a method with multiple annotations of the same type. To read all the annotations from a method, you can use the `getAnnotationsByType` method; this method returns an array of annotations or an empty array if there are no annotations. One example of having the same annotation multiple times in a method is when you want to schedule the method execution at some different frequencies.

### Day 1996: Reding Fields Java Annotations

Today I learned and practice how to know if a Field is marked with some annotation and how to read the annotation for the Field. This pattern of mark fields from a class with an annotation and next execute some specific behavior if the fields has X annotation is frequently used in mappers and builders, for example when you want to serialize/deserialize a JSON into a Java object or when you want to build a SQL query from a Java object. Also I continue learning C.

### Day 1995: Continue with Reflection and C Code

Today I continue studying reflection, this time I build an application that read the parameter methods `Annotations` and execute the method with their parameters with Reflection like building a dependency graph, for example you have a method A that takes the result of method B as a parameter, so with Reflection and Annotations you can generate a dependency graph and execute a method, next pass the result method as a parameter of other method with Reflection. This is very useful when you want to execute N numbers of tasks in some order and you want to avoid calling directly it. In other topics I created a basic C program to list all my current local network address from my Mac. I started to lean C because I want to understand low-level concepts like working and manipulate bytes. 

### Day 1994: Implementing Retry Method Feature With Reflection

Today I created an annotation called `RetryOperation`, this annotation can be used in methods that you want to retry their execution if an exception occurs in the method execution. The annotation have some annotation elements that you can customize to increase the number of retries or the delay between the retries, the main is annotate a method this annotation and with Java reflection, read the annotation elements, create code logic for the retry in case of an error and invoke the method with Reflection. 

### Day 1992-93: Reading Java Annotations with Reflection

During these two days I continue learning about Reflection. This I am learning how to read annotations from `Fields`, `Methods` and `Class` using reflection. I started to work on a code exercises in which I analyze all the classes inside a X java package to find which classes and methods are noted with some special Annotations, the idea is when a Class and Method have X annotation, we execute the method from the class with Reflection. The last technique is very useful when you want to initialize something in your code automatically like database connections, create caches, create a server connection, etc. I am having issues with this code exercises because the code cannot parse correctly a package name in String to a valid Java `URI` object. 

### Day 1990-91: Continue with Reflection

Over the Weekend I continue studying Reflection in Java. This time I created an implementation of a test framework, with some basic functionalities like analyzing all the methods declared in a Test class. First the test framework review all the methods declared in the class, every method that starts with a prefix `test` is considered a test method, and also the framework supports others test specified methods like `beforeClass`, `beforeEach` and `afterClass`. I have fun implementing this framework and know I understand how testing frameworks like `Jupyter` works.   

### Day 1989: Learning to Analyze Methods with Reflection

Today I learned how to analyze the method from a X class using reflection. The Java reflection API allows us to analyze the methods from a class with a good interface, for example with the `Class.getMethods()` method we can get all the methods from a class, with the `Method.getName()` we can get the method name. I created a basic code logic to validate if a data class (A class that needs to have only getters methods for the class fields) is correct every field have a getter method, with the code logic: `String getterName = "get" + field.getName().substring(0, 1).toUpperCase() + field.getName().substring(1);` we can build the getter method name for a field.

### Day 1988: Configuration File Parser

Today I did a little code exercise in which I create a `ConfigurationCreator` class with one method to create a config object from a file. The idea is to read a .cfg file, next use reflection to create a Java object with the .cfg file information. I used a Java `Scanner` to read the file information, also I created some unit tests to validate the code.

### Day 1987: Reflection Exercise

Today I continue studying reflection with a code exercise. I needed to add the logic to serialize an array of objects into a JSON string. I liked the final result because I could reuse the previous code created to serialize a single object into a JSON string.

### Day 1986: Arrays and Reflection

Today I learned how to detect if a `Field` from a `Class` is an array, also I implemented some code to read the values from the array one-by-one and at the end create a string JSON representation of the array. We can review if a `Field` is an array with the next code: `field.getType().isArray()`.

### Day 1985: JSON Serializer and Calculate Space Object

Today I continue learning and practicing Reflection with two exercises, one was to create a JSON serializer algorithm that takes any `Object` and serialize into a JSON. The algorithm is simple, and works with primitives values like `int`, `boolean`, `char`, `short`, etc. Also I work into another exercise in which I calculate the memory that an object consumes in `bytes` in memory using Reflection. Sometimes I feel a little bored about Reflection, but I know that I need to know it for my current project.

### Day 1984: Reading Class Fields with Reflection

Today I learned and practice how to read the fields of a class using Reflection. With Reflection we can read the declared fields of a class in Runtime with their current values, I discovered that the JVM generates some special fields called **Synthetic** fields for internal class purposes, for example when we have a nested class, that class will have a synthetic field that points to the outer class. I also discovered that the JVM generates a field called `this$0` that points to the outer class, this field is used to access the outer class fields from the inner class. 

### Day 1983: Reflection & Dependency Injection

Today I practice Reflection creating a little program that instantiate a class using Reflection, the class have as a dependencies multiple classes added as parameters and also that parameter classes can have other dependencies, so the idea was use Reflection and recursion to create an object for that class with all their dependencies. I am in the 1983 day learning computer science, please listen the next song called **1983** really is called like that https://www.youtube.com/watch?v=j51LRUjIdnE

### Day 1982: Continue with Reflection

Today I continue studying about Reflection. I created a Java application that analyze any object that you send as a parameter, from this object I extract the type, name, package name and also if the objects implements n number of interfaces, also I discovered that some IDE plugins use Reflection to show to the user the `Class` information when hover a class name, is interesting how Reflection in Java is used for a lot of tasks.

### Day 1981: Java Reflection

Today I started to study and refresh my Java Reflection knowledge. In my current project we have a lot of reflection code and also Reflection is a lot used on the project, I feel a little lost when read this code, and also lost while I attempt to understand how the code works, for that reason I started a Udemy course about Reflection in Java.

### Day 1980: Importance of the Last Node Problem in Heap Trees

Today studying about Heaps, I understand why the Last Node is very important for heaps and why an array is the best data structure to implement it. The last node of the heap is crucial for operations like deletion and insertion, for deletion we always move the last node as the new heap root and for insertion we always add the new node as the last node. The last node is very important to meet the heap property.

### Day 1979: Heap Binary Trees

Today I studied about the Heap Binary Tree data structure. First I read the theory of this data structure behind the insertion and deletion operations, I learned that this two operations have a `O(log N)` time complexity. Looks like that Heap trees are a good choice when you need to execute for example some operations or have the as a first element the element with the highest priority, also I read about *The last node problem* and how the binary tree trust on this operation to implement the others. Tomorrow I will continue studying this DS, Tress and recursion comes together and I have low knowledge with both concepts.

### Day 1977-78: Studying and Break

Yesterday I took a break from coding, I just read a few pages from the Tidy First book. Today I practiced with a Binary Search Tree code exercise. I had problems to solve the problem by myself, in the end I had to look for the code solution after several failed attempts. I need to practice more with recursion and trees.

### Day 1976: Code Exercises and Java Question of the Week

Today I continue solving code exercises related with Binary Search Trees, in other topics I answer the question of the week about how can we read the content of a file in Java. Answering these questions is a good exercises to learn and master concepts, maybe you think that well I know how to read a file in JKava, but you are not aware about the performance implications of the different ways to read that file.

### Day 1975: Continue with Binary Search Tree

Today I continue studying Binary Search Trees. I solved some problems related with data structure and also I completed the book chapter about that. Tomorrow I have the plan to create a blog post about Java.

### Day 1974: Writing Deletion Operation for Binary Search Tree

Today I started to study and implement the deletion operation for the Binary Search Tree. For the moment I am having problems to understand how the operation works, the operation is very complex because we need to consider multiple scenarios to delete a node from the tree. I will need to continue studying this operation tomorrow.

### Day 1973: Binary Search Tree

Today I started to study this data structure in my DSA book. I am happy with my progress, I could implement the search and insertion operations from scratch only reading the logic steps from the book. Really practice is the key to master DSA, recursion, algorithms and all these complicated stuff. Tomorrow I have the plan to continue working with the Binary Search Tree currently I am stuck to write the method to `print` all the node values by level.

### Day 1972: Practicing Linked List Algorithms

Today I practiced solving some Linked List problems. I started the part of the book in which we review the Binary Search Tree but before start to review it, I want to solve some problems with the first Node-based data structure learned in the book.

### Day 1971: Java `wait()` and `notify()`

Today I studied this two Java methods to execute concurrent code. The `wait()` method blocks the current thread execution until another thread calls `notify()` in the same object. The `notify()` method wakes up the first thread that called `wait()` in the same object. Imagine that you are waiting to receive some data from a server, you start to read the data in a separate thread to avoid block the main application thread, but the data is not available yet, so you trigger `wait()` to tell the current thread to wait until the data is available, when the data is available the server thread calls `notify()` to wake up the thread that is waiting for the data. I read that these technique used in Java is very old, but in my work we use this technique with concurrent code.

### Day 1970: Continue learning about Concurrency

Today I continue with my study of concurrency with Java. For the moment I am practicing with execute some Java processes in separated threads, accepting connections from multiple clients to my application and learning how to manage these clients concurrently.

### Day 1969: Java Threads, Concurrency and Sockets

Today I practiced creating a Java application that listen for incoming connections through a `Socket` connection. The project idea was easy, created a Java application server that listen for incoming client connections, each client connections needs to be operated in a separate thread to avoid block the main thread, when the client send a message to the server, the server process this message and send it to a `Priority Queue`, next the message will be send to different clients connected. Work with threads and concurrency in Java is a little bit difficult, for the moment I am having problems to understand how to create concurrent code like this because I am not familiar with this type of code.

### Day 1968: Linked List Code Exercises

Today I continue developing some common linked list operations like print all the values in a list, reverse a linked list, get the last node of a linked list, etc. These exercises are a very good way to practice with the Linked List and Doubly Linked list data structures, I had some problems to understand the logic behind the reverse a linked list algorithm, but after some time I could understand how it works. I will continue practicing with these exercises tomorrow.

### Day 1967: Double Linked List

Today continue studying the Linked List data structure, I started to study the **Double Linked List**. This data structure is a good choice when you need to delete and insert elements frequently because offers a `O(1)` time complexity for insert an elements in the start and end to the list and for delete an element requires a `O(N)` steps. I will continue studying this data structure tomorrow.

### Day 1966: Linked List

Today I started to study about Linked List in my DSA book. This time I am doing a different approach about write the Linked List operations like read, search and insert from myself. I want to to build these stuff from myself to understand how to manipulate a Linked List. For the moment I wrote the `read` and `search` operations, but I am having some problems to understand how to write the `insert` operation.

### Day 1965: Continue Studying DSA

Today I continued studying DSA reading the book. I solve some exercises in which we first sort an array and next we need to perform some action in the sorted array, which this technique I could to solve the problems with a `O(n log N)` time complexity. I also used a Greedy approach to solve some problems, the Greedy approach is a technique to solve problems in which we make the best choice at the moment, without thinking about the future.

### Day 1964: QuickSort and QuickSelect

Today I studied the QuickSort and QuickSelect algorithms. I started to study the logic behind the two algorithms an next implement them with Java code, the problem is I could not understand in a good way both algorithms. Recursion is a problem for me because write and read recursion code continues be a hard task for me. I will need to continue practicing these algorithms to understand how they work.

### Day 1963: Storage Virtualization RAID 0

Today I studied about the RAID storage virtualization technique creating Java code to simulate the RAID 0 configuration. For the moment I have an issue while the code is attempting to read the metadata file with the file from information. I am using an approach about storage the file metadata in a physical file using a Java `Serialization` class, but I am having problems at the moment to deserialize the file into a Java object.  

### Day 1962: DSA and Java SE 17 Test

Today I continue studying my DSA book, I am learning how implement the QuickSort algorithm, for the moment I am not understanding much because this algorithm is divided into three different main steps, first step is to find the **pivot** in the array to be sorted, second is divide the array by the half and use recursion to sort this half of the array and divide by the half again the same same and is the same for the other half of the original array. Really this algorithm is confuse at the start. In other topics I did the Java SE 17 Skill IQ from PluralSight to measure my Java 17 skills, I got an average score, so that means I have good knowledge about how to work with Java 17 but I will need to improve to reach the  **over average** or **expert** score.

### Day 1961: Recursion and Dynamic Programming Exercises

Today I practiced recursion and dynamic programming solving some exercises. For the moment these way of solve problems using recursion and Dynamic programming is not making click in my head. Sometimes is really difficult to understand how recursion works, how the functions calls are storage in the stack call and how these function calls are called, and well how the result is build in the stack call. I will need to continue practicing more these techniques.

### Day 1960: Dynamic Programming

Today I studied one of the hardest concepts in computer science that is **Dynamic Programming**. Dynamic Programming is a technique to solve problems by breaking them into smaller sub-problems and storing the results of these sub-problems to avoid solving them multiple times. The main idea is to solve the problem dividing this problem into sub-problems and store the results of the sub-problems in some place to avoid call the same sub-problem multiple times. Memoization is a common technique in dynamic problem to memorize the sub-problems results. I did some code exercises to refactor recursion functions and apply DP to improve the algorithm efficiency.

### Day 1959: RAID Virtualization Technology

Today I learned about RAID Virtualization Technology. RAId is a technology that allows to combine multiple flash-drives or HDDs into one logical disk. Imagine that you have 10 SDDs disk and you want to combine them into one disk, so using RAId you can combine them into 1 disk and the host system like a PC or server looks only one disk. RAID offers another important features and have some different configurations like `RAID 0`, `RAID 1`, `RAID 5`, `RAID 6` and `RAID 10`(I don't know yet if a configuration is the correct word). These different configurations offers different features and have different performance capabilities. If you want to have data replication you can use `RAID 1`, if you want to have faster write/read operations you cna use `RAID 0`, all these things are new for me are interesting because is more focused on computer science topics and not learn a new framework to build something.

### Day 1958: Why Recursion is So Hard?

Today I continued practicing recursion with some exercises. I completed the unique paths problem, I can discover the base case and start the algorithm but to completed it, I needed some help from Google. The main problem with this recursion problems is that the function needs to call itself multiple times, with multiple parameters and the return value of the function is the result of one of the previous function. This is very difficult to understand for me, but well my approach to continue learning recursion is more practice, I will need to continue solving more problems, creating recursion algorithms to master this skill.

### Day 1957: Continue Practicing Recursion

Today I learned one of foundations recursion principles. The principe is if your functions needs to return a value, you need to return a value in the base case and in any return statement within the function. I discover this while writing the flatten nested arrays function. I needed to return an `[]` in the base case and in the another return statements concatenate the result of the previous function call with the current value. Also It's very important to return always the same type of element in non-static coding languages like JavaScript, because if you return a `number` in the base case and a `string` in another return statement, you will get an error. I want to continue practicing recursion for more some time because I feel that I need to practice more to understand how recursion works.  

### Day 1955 & 56: Recursion Functions that Generates Values

Over the weekend I practiced recursion, focusing on recursive functions that generate a result like a list and then add items to that list in consequence executions. Yes, I continue with not understanding this type of functions well, I continue with problems about how to merge the return in a recursive function with the next executions, especially when the recursive function returns more than one value, is very strange to me, looks like some dark magic. But the good news is that with every day of practice it looks less complicated. Practice == mastery.

### Day 1954: Debugging Recursion

Today I spend most of my time debugging Recursion functions. I am using the VSC debugger to understand how the recursion works, One of my main current recursion problems is understand how the results are build in the recursion stack, the top-bottom approach is easier to understand rather than the bottom-up approach. Also the concept about solve sub-problems and combine the results to get the final solution is a little bit difficult to understand.

### Day 1953: Top Down Recursion

Today I learned and practiced about the top-down recursion technique. This technique looks like magic to me, the idea is to start with the final solution and divide the problem into smaller sub-problems. Sounds crazy think about the function is already written and you only need to implement the sub-problems. I did some code exercises t practice this Recursion technique, I will need to continue practicing this technique tomorrow because continues looks like a magic thing for me.

### Day 1952: Recursion Repeatedly Execute

Today while studying recursion, I learned that recursion functions can be categorized in some categories. The idea about identify the category of a recursion function is to know how to read it and write it. The **Repeatedly Execute** is a recursion function in which in each function call a task is performed, maybe you want to print something into console, increment a counter or any type of other things.

### Day 1947, 48, 49, 50, 51: Sick, IBM Cloud Advocate and Recursion in Binary Trees

These days were bad. I was sick since Friday and I could not code anything, I had a very bad headache and I was very tired. I was out for four days.
The good news are today I approved the IBM Cloud Advocate certification exam, I am very happy with this achievement. I started to practice and study Recursion focusing on Binary Trees, today I have a lot of problems to print the value of the Node with the corresponding level of depth in the Tree.

### Day 1946: Continue with Algorithms

Today I begun my day solving LeetCode questions. I solved some problems related with two pointers, sliding window, a min stack problem about build a Stack that support the operation to `getMin()` value with a `O(1)` time complexity. I also solved the yesterday problem about implement the binary search algorithm. I discover a new list of problems to solve called [Grind 75](https://www.techinterviewhandbook.org/grind75/) looks like this list of problems is very acceptable by the community.

### Day 1945: Practice LeetCode Problems

Today I have been practicing solving leetCode problems, currently I am working into implement the Binary Search algorithm <https://leetcode.com/problems/binary-search/> for the moment I am stuck about how to implement them, in the past I remember I implement this algorithm following a tutorial but now I want to solve the problem by myself. I will continue working into this problem tomorrow.

### Day 1944: Reading DSA Book and Stack Data Structure

Today I continue reading my DSA book, I completed the chapter 10 exercises about **Recursion**. In this chapter I did some exercises to practice how to read and write recursive code, for the moment I want to understand how **Recursion** works again and also practice more the *divider and conquer* technique to solve problems. I completed some algorithms exercises in GeekForGeeks about Stack, the last chapter of the book was about stacks and queues so I needed to practice with the stack data structure. I prefer GeekForGeeks rather than LeetCode, I know that LeetCode is better but in GeekForGeeks you can found better explanations of the Data Structures and Algorithms for free, LeetCode also have some good courses about this but most of them are paid.

### Day 1943: DAG Development and Stateful Sequential Processing

Today I continue working on my Airflow DAG to process my entry journals in this repository to extract the skills learned every day. I completed the regular DAG, now I am working in the reload DAG to process the old entries. I am working in the logic to process 130 entries daily because the Azure AI service has a day limit of 150 HTTP request. In other thing I learned about the **Stateful Sequential Processing** technique/design, I will need use this technique to process the entire dataset with all the entries.

### Day 1942: Issues in my Ubuntu Server

Today I had an interesting issue in my Ubuntu server. For an unknown reason, there were no internet connection for external sources inside the server, for example I can't access to my Airflow instance from my laptop and download python packages from pypi to my server. I needed to investigate the issue, I started to check the network configuration, the virtual public network configured in my cloud provider but everything looks fine. Investigating more I found that sometimes after upgrade the Ubuntu server, you will problems with the ufw firewall and the ip-tables, I needed to restart the server, restore and configure the iptables to finally activate the ufw firewall. After this the server works fine. Networking issues always are a nightmare for developers, specially if you don't much knowledge about networking.

### Day 1941: Continue with DAG Development and Ubuntu Server Upgrade

Today I upgraded my ubuntu server from 22.4 to 24.04.1, in this server I had my Airflow environment configured and some applications running in Containers. Also I continue worked on my Airflow DAG about processing the entry journals to extract the skills learned that day. I write some python code to extract the skills and completed the Azure AI service integration. I am following the practice to measure the time complexity of the code that I wrote, to practice my DSA and algorithms skills.

### Day 1940: Continue with DAG Development

Today I have been working on my Airflow DAG to extract from this entry journals the skills learned related with Computer Science and Software Engineering. I started the task to process the entry journal with the Azure AI service using the Python SDK to interact with LLMs, I created the Python logic and some algorithms to achieve this task. One of the problems that I am facing right now is to write unit test for the Python code because there are many levels of abstraction in the code, I need to think how to test the code in a way that I can ensure that the code works as expected while mocking the external dependencies like the Azure AI service. I will continue working into this task tomorrow.

### Day 1939: Recursion

Today I started to study recursion again. I am reading the book chapters about Recursion for the moment I did some basic exercises to practice how to write and read recursion code.

### Day 1938: Building A Javascript Linter Logic

Today I started to work into create a function that checks if a string is a valid javascript code, the general idea is to review the opening and closing braces like `()[]{}` and validates if there are a correct order and number of braces. I am using a Stack to manage the curly braces order. I will need to continue working into this algorithm tomorrow.

### Day 1937: Continue Reading and Doing Exercises

Today I continue reading my DSA book, I completed the chapter 8 and I did the code exercises, for the moment I am doing the code exercises following a test-driven development methodology, I want to continue improving my TDD and testing skills.

### Day 1936: Hash Map and Bubble Sort

Today I have been studying about Hash Maps, I am reading the book chapter about the Hash Map/Hash table data structure. I want to review how a Hash Map is designed and build with Java because there are some interesting things to consider to design a good Hash Map, like a relationship with how many cells or memory the hash mp will have considering the number of elements storage on it. In another topics I studied again the bubble sort algorithm.

### Day 1935: Fixing Airflow Issue and Configuring GitHub Action

Today I fixed the Airflow issue about configure a directory as a module to be used in Airflow. I needed to setup a environment variable within the container to configure the directory path. In other topics I created a GitHub action to execute my unit test everything I create a pull request to the main branch. I am using a GitHub project to manage the development of my Airflow DAG, the idea in this project is to create task for new features. next create a separate branch to develop that feature and at the end merge that branch to the main branch and close the task, I want to follow this basic development workflow to continue practicing this skill and also I can measure how much time I require to complete X feature.  

### Day 1934: Software Engineering Skills DAG

Today I continue with the development of the Airflow DAG that looks for the last commit in this repository and extracts the skills learned that day. I completed the task that extract the README.md file from the code repository, and started the task that parse the extracted README.md file into a personalized data structure. The idea behind create a data structure to represent the data is to have easy access to the data. I created a method called get_last_entry that get the last entry journal in a dict format. Tomorrow if I have some free time I will need to fix an issue with Airflow related with use some modules in the DAG file.

### Day 1933: Hash Table

Today reading my DAS book, I started the part in which we study the Hash Table. A Hash Table data structure is a data structure in which the data is stored in key-value pairs, the main idea is you can get a value with a key from the Hash Map. The Hash Map uses a hash function to convert the key into a number, this process of converting something to a number is called hashing. An important thing about the has function is always needs to return the same number for the same key.

### Day 1932: Big O in Everyday Code

Today I practice with some common algorithms that we use in our daily activities, the idea is measure the code efficiency with Big O for common algorithms like look for an user within a list of elements. When you think about every piece of code that you write to solve a problem is an algorithm and also you can measure the efficiency of this code with Big O it's a good moment in your developer career. I think that is a good practice to measure the efficiency of your code, because you can know if your code is efficient or not. Also it's funny well, for me is funny.

### Day 1931: Studying the Average Case Time Complexity

Today reading the DSA book, I learned about the average case time complexity. We know that Big O only consider the worst-case scenario to determinate the time complexity, but most of the times the worst-case scenario is not the common scenario. It's more common to have the average scenario in daily code implementations, so maybe you have two algorithms that have a `N^2` complexity but one of them have a `N^2 / 2` complexity in the average case.

### Day 1930: Data Completeness and Completed Insertion Sort Algorithm

Today I learned about data completeness. Data completeness is a data quality metric that measures that the there are no missing data in a dataset, for example if we extract data from an API and the API returns a JSON with 100 elements, we need to store the exact 100 elements in our dataset to have the data completed. Sometimes when transforming and loading data to the target system, we can miss data and if we don't have a way to know how much elements we get in the extraction phase and compare with the loading phase we can lose data. In other topics, I completed the Insertion Sort algorithm implementation in JavaScript, really sometimes I feel that I cannot complete id but I take the approach to solve the entire algorithm in small steps, like first ensure the inner while loop is working as expected. Breaking the problem into small steps helps me to complete the algorithm. Tomorrow I will continue reading my DSA book.

### Day 1929: Insertion Sort Algorithm

Today I have been studying the Insertion Sort algorithm. I am reading the chapter in the book that talks about consider the non-worse cases scenarios for algorithm. Maybe you have two algorithms with a O(N^2) but one of them can be twice faster than the other. I started with the code implementation of the insertion sort algorithm, however I cannot completed it. I am having problems to translate the algorithm description into code. I will continue tomorrow with the code implementation.

### Day 1928: Airflow Project Folder Structure

Today I learned techniques to structure an Airflow project. I am developing an Airflow DAG so I need to learn where is the best place to put the files with functions and classes to use in the DAG. For example where we need to add the files like helper functions? Well, I found a StackOverflow post that explains the best practices to structure an Airflow project.

### Day 1927: GitHub Software Engineering Skills DAG

Today I started a new project. The main is to create a DAG that every day looks in this repository to check the last commit, if the last commit have the format dayXXXX, the DAG will extract the README.md file information and next serialize the README.md file in a Python object format, the idea is extract the last day skills learned entry like this entry and use a LLM to extract the skills learned that day. I want to storage the entries in a SQL database to know which technologies I learned that day. My goal is to continue learning Data Engineering, Airflow, DAG development and AI. You can see the general idea of the project in the next link: <https://github.com/user-attachments/assets/ff3312e6-e9f9-46c3-979d-a50aa717a850>  

### Day 1926: Looking for Duplicate Data with Spark

Today I was discovered how to detect duplicate data in a Spark parquet file, the problem is we extract data from an API and sometimes the API returns duplicated data, so we need to detect this duplicated data and remove it from the response to avoid add it to the parquet file. The problem is we store the data in a parquet file if we store the data in a SQL database like PostgreSQL, detecting the data will be a simple query, but with Spark, we need to do some transformations to detect the duplicated data. I have the plan to continue learning more techniques to remove duplicate data from a parquet file.

### Day 1925: Bubble Sort

Today I studied the Bubble Sort algorithm. I implemented it in JavaScript and used Jest for unit testing. I only needed to read the algorithm description to figure out the implementation. When my tests passed, I felt very good. It was a great moment for me. I am in the book part in which we study this sorting algorithm and we review the quadratic time complexity. I am happy with my progress. I will continue studying DSA and solving problems in LeetCode and GeekForGeeks.

### Day 1924: Data Integrity with Spark

Today I spend some time analyzing data integrity in some parquet files. The problem is we lose some information from the files processing the files with Spark for an unknown reason. I am following a backup approach for the moment to backup daily the data and if the issue happens again, I have a fresh copy of the data. I am investigating the possible ways in which the data is lost with Spark and Spark leave the files with less data but with a non-corrupt state.

### Day 1923: Partition Keys

Today I learned about partitions keys, I needed to do a little research about what are partitions keys and how works. I am working in a Data Engineering in which I see an example of a usage of a partition key in a parquet file, we use a parquet file to storage data and this data is modified frequently, so we need to backup this data weekly to have a copy of the data in case of a failure or our parquet finish in a corrupt state. One strategy that a team follows is have the data backup in an another parquet file and they use a partition key to store the data in a way that is easy to query and retrieve the data. So this parquet backup data contains partitions of weekly backups, so if you need to retrieve the data from a specific week, you only need to query the partition key with the week that you need to retrieve the data. I think that this is a good strategy to backup data, the trade-off is the storage required. Storage in these days is cheap.

### Day 1922: Solving LeetCode Problems

Today I have continue solving some LeetCode problems related with arrays and use Map to lookup faster for elements. I continue reading my DSA book, for the moment I completed the book part about the Binary search algorithm, and how is more efficient to look for an element in an ordered array rather than a normal array. For the moment I fell good with my progress, I want to continue studying DSA and solving problems in LeetCode and GeekForGeeks.

### Day 1920-21: Continue with Data Structures and Algorithms

Today I continue studying DSA, I was studying again how the time complexities differs from a normal array and a ordered array. I created an implementation of a function that inserts a value within an sorted and maintain the sorted property. I also started to study the `Binary Search` algorithm, I remember that this algorithm is very useful when you need to find a value in a sorted array, the time complexity of this algorithm is `O(log n)`, I will continue studying this algorithm tomorrow. This time I am studying slowly and deeply this concepts and techniques, really I want to understand how the algorithms works and how to implement them.

### Day 1919: Creating a Python AI Application

Today I experiment with something new, I created a Python Chat AI application the user can interacts with the Granite, Llama and Mixtral LLM models to talk. The application have a basic web app interface with Flask and HTML, the user can write a message and the AI model will respond with a message. I learned some interesting prompts properties like special Tokens to indicate the model where the conversation starts, the role that the model will play in the conversation. I enjoyed creating this application.

### Day 1918: DSA and Data Backup Strategies

Today I continue reading my book about DSA, I am in the part in which we review the Array Data Structure, its amazing how when you read and practice something again, you can learn new things also I practice with some array problems. In other topics I started to study about Data Backup Strategies, I am working in a project in which sometimes we lose data from our parquet files, I think that the data lost is related with some Spark errors when writing the content of the Dataframe into a file in disk. I hate to guess the things,but for the moment I don't have a clear idea about what is happening, so for the moment the idea is perform frequent backups while working into investigate the issue.  

### Day 1917: Spark Write Modes

Today I learned the different ways to save a dataframe into a physical file like CSV, JSON, Parquet into disk with Spark.
Spark manages the next write modes: `overwrite`, `error`, `ignore` and `append`. The default write mode is error, that means if you try to save a dataframe into a file that already exists you will get an error, ignore is like *save if not exists*, overwrite is to replace the current file with the new dataframe and last append is used to add the new dataframe to the file, like combine these two DF into one final version.

### Day 1916: DSA and Amortized Analysis

Today I learned what is the **Amortized Analysis**. Amortized analysis is a technique use to discover if the cost of a expensive operation like sorting an array `n(nlogn)` leaves the data structure in a way that the next operations are cheaper. This technique I think that is useful when you need to sort and array and next you can use the sorted array to do some operations that are cheaper and less expensive, compared to perform the same operations with the original array. Tomorrow I have the plan to look for some algorithms in which apply this technique is a good choice.

### Day 1915: Array Problems

Today I solved the One plus problem that I started yesterday. Although it was an easy question, I had some difficulties solving it. The main idea is to check if we still have a `carry = 1` after iterating over the entire array. If we do, we need to add a 1 at the start of the list. I also worked on other array problems. Unfortunately, I couldn't read my algorithm book today because my morning study time was replaced by commute time as I had to go to the office again.

### Day 1914: Reading and DSA

Today I read a Substack article about how to growth from a mid-level software engineer to Senior [Article](https://newsletter.eng-leadership.com/p/how-to-grow-from-mid-level-to-senior?utm_source=publication-search). The Article was very good, I want this year be promoted in my current company, so I am looking for ways to grow and be a better software engineer. Also I started with the `Plus One` problem, I know that this problem is an Easy question, but well LeetCode says that I answered this problem 1 year ago, but at this moment I don't remember how to solve it, so I started to solve it again. The problem is very simple, you have an array of integers that represent a number, you need to add one to this number and return the result as an array. I will need to continue practicing DSA.

### Day 1913: DSA and Python Layered Architecture App

Today I continue studying DSA, in the morning I continue reading my book and studying more about DSA, also I solve an algorithm to reverse an Array in place, I remember that this algorithm in the past was very difficult, but today looks easy. In the afternoon I created a Python project for fun, to learn Software Architecture, I practiced creating a REST API Python application with a layered architecture, the project includes the Presentation, Service(Business), Data Access (Repository) and Database layers.

### Day 1912: Continue studying DSA

Today I studied some interesting topics about DSA like Analysis of Algorithms, Rate Growth, Asymptotic Notation, and Big-O notation. I am doing deep dive on these topics to build a good knowledge.

### Day 1911 Factory Method Design Pattern and Data Types

Today I worked into refactor some Python code implementing the Factory Method Design Pattern. I notice that my code have some if statements, statements that can be refactored because with the value of a variable, the code behaves in different ways, like work calling this API, but with this value call this other API. I refactored the code using the Factory Method Pattern now my client code don't need to worry about how call the API for a given value, the code needs to call one object method and get the API result. Also reading my new algorithm book, I begin to study DSA in deep, for the moment I learned the two main Data Types: System-defined and User-defined Data Types. A data type in programming language is a set of data with predefined values, like `integers`, `strings`, etc. We now that for an `integer` data type, we only can store integer values. System-defined data types are those that are defined by the programming language itself and the user-defined data types are those that are defined by the user like `Classes` in Java or `structs` in Go.

### Day 1906-07-08-09-10: Break, Reading and Practicing DSA

I take a little new years break, at the end of the year I only relax during the day and start again to practice DSA. I know that DSA is a must-have skill for a Software Engineer is like English, if you want to work on big tech companies (Netflix here we go), you need to have a good DSA skills. One of my goals for this year is focus in DSA and start to apply to other big tech companies like Microsoft, Amazon or Oracle. I solved some Easy and Medium problems in GeekForGeeks, GeekForGeeks is a good platform to practice and learn DSA, I have the plan to continue studying, learning and practicing DSA in this platform for the moment.

### Day 1905: Manipulating Dataframes with PySpark

Today I worked in a task related with modify a column value in a PySpark dataframe, first I filter the dataframe to get the rows that I need to modify, next I crated some logic to modify the value of a specific column, I have some problems at the start because the column have a string value with a date format and I want o to modify the value applying a logic to update the column values with a timestamp greater than X date. I needed to think how to do this, for the moment I have problems to write clean code related with this little task, because with a few lines of code with Python and PySpark you can do a lot of things, but you need to think how to do this.

### Day 1901-02-03-04: Christmas Break, Book Completed and LeetCode

I take a Christmas break to rest and enjoy the time with the family. However, I could not relax without learning something new. I completed the Software Engineering at Google book, finally I completed it, after three months reading this book. Also I started to retake LeetCode problems, the next year I want to focus on Data Structures and Algorithms and my University degree.

**Day 1 - 50 HTML - CSS - Javascript** [here](./day0-500/day0-50.md)</br>
**Day 51 - 100 Javascript** [here](./day0-500/day51-100.md)</br>
**Day 101 - 150 Javascript** [here](./day0-500/day101-150.md)</br>
**Day 151 - 200 Javascript** [here](./day0-500/day151-200.md)</br>
**Day 201 - 250 Javascript and start React JS** [here](./day0-500/day201-250.md)</br>
**Day 251 - 300 Javascript - React JS** [here](./day0-500/day251-300.md)</br>
**Day 301 - 350 Javascript - React JS and start Node JS** [here](./day0-500/day301-350.md)</br>
**Day 351 - 400 Start learn MERN stack** [here](./day0-500/day351-400.md)</br>
**Day 401 - 450 MERN stack - Docker - Typescript - TDD** [here](./day0-500/day401-450.md)</br>
**Day 451 - 500 Object Oriented Programming** [here](./day0-500/day451-500.md)</br>
**Day 501 - 550 Data Structures and Algorithms** [here](./day501-1000/day501-550.md)</br>
**Day 551 - 600 Java**</br>
**Day 601 - 650 Java** [here](./day501-1000/day601-650.md)</br>
**Day 651 - 700 Java and Spring Boot** [here](./day501-1000/day651-700.md)</br>
**Day 701 - 750 Java | Spring Boot | MySQL** [here](./day501-1000/day701-750.md)</br>
**Day 751 - 800 Java | Spring Boot | MySQL** [here](./day501-1000/day751-800.md)</br>
**Day 801 - 850 Java | Spring Boot | OCI** [here](./day501-1000/day801-850.md)</br>
**Day 851 - 900 Java | Design Patterns** [here](./day501-1000/day851-900.md)</br>
**Day 901 - 950 Java | Design Patterns** [here](/day501-1000/day901-950.md)</br>
**Day 951 - 1000 Java | Design Patterns** [here](./day501-1000/day951-1000.md)</br>
**Day 1001 - 1050 Java | New Job** [here](./day1001-1500/day1001-1050.md)</br>
**Day 1051 - 1100 Java | Python | Cloud Computing** [here](./day1001-1500/day1051-1100.md)</br>
**Day 1101 - 1150 Java | Containers | Cloud Native Development | OpenShift** [here](./day1001-1500/day1101-1150.md)</br>
**Day 1151 - 1200 Java | Containers | Python | Security** [here](./day1001-1500/day1151-1200.md)</br>
**Day 1201 - 1250 Java | Python | Security | English** [here](./day1001-1500/day1201-1250.md)</br>
**Day 1251 - 1300 Java | Python | Security | English | Soft-Skills** [here](./day1001-1500/day1251-1300.md)</br>
**Day 1301 - 1350 Java | Python | Spark | Microservices** [here](./day1001-1500/day1301-1350.md)</br>
**Day 1351 - 1400 Java | Python | Design Patterns | Microservices** [here](./day1001-1500/day1351-1400.md)</br>
**Day 1401 - 1450 Java | Design Patterns | CI/CD** [here](./day1001-1500/day1401-1450.md)</br>
**Day 1451 - 1500 Java | Design Patterns | CI/CD** [here](./day1001-1500/day1451-1500.md)</br>
**Day 1501 - 1550 Java | Python | Data Analytics | CI/CD** [here](./day1501-2000/day1501-1550.md)</br>
**Day 1551 - 1600 Java | Python | Data Analytics | CI/CD** [here](./day1501-2000/day1551-1600.md)</br>
**Day 1601 - 1700 Java | Python | ReactJS | Data Structures and Algorithms** [here](./day1501-2000/day1601-1705.md)</br>
**Day 1701 - 1750 Java | Go | DSA | A Common-Sense Guide to DSA Book** [here](./day1501-2000/day1706-1750.md)</br>
**Day 1751 - 1800 Java | Python | DSA | AWS Cloud Practitioner | Data Engineering** [here](./day1501-2000/day1751-1800.md)</br>
**Day 1801 - 1850 Java | Python | Airflow | AWS Cloud Practitioner | Data Engineering** [here](./day1501-2000/day1801-1850.md)</br>
**Day 1851 - 1900 Python | Airflow Certification | Cloud certifications | Data Engineering | Spark** [here](./day1501-2000/day1851-1900.md)
