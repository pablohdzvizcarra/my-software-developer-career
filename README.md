# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 2058: Back Pressure

Today I learned the **back pressure** concept in software design. This concept is used to describe when we have a producer pushing messages to a queue and the queue has a consumer that is reading the message, but for example, the producer pushes 10/s messages and the consumer reads 2/s. In this scenario, the queue grows to a good size to handle all the messages. To avoid this bad design, we need to apply a limit to the queue and stop the producer for some time after the consumers leave the queue empty. Learning about Java multithreading will be good and hard at the same time.

### Day 2057: Failover Issues

Today, I debugged an application issue. When something went wrong with Worker A, we needed to fail over to Worker B. For an unknown reason, Worker B could not successfully execute the request. This issue is strange because the two workers should work equally, and at any time, either worker can have the role of the main worker depending on the workload. Tomorrow, I will continue investigating this pattern/architecture to better understand common problems with this design.

### Day 2055-56: Multithreading & Kubernetes Architecture

I continued studying about Java Multithreading. This time, I studied the Java `Semaphore` class. With the `Semaphore`, we can create multithreading applications easily. One of the most common usages of this pattern is in a producer-consumer architecture. We have N number of producers, and maybe we can wait until a consumer reads a message from a queue. So, we can use the `Semaphore.acquire()` method like a sleep until some condition is met. In this case, the condition is another thread executing the `Semaphore.release()` method. Looking for a real example in which this technique is applied, I discovered that Kubernetes uses this pattern when updating some objects using events that come from an API with a Bounded Blocking Work Queue. I am working on a code implementation of this pattern for learning purposes.  

### Day 2054: Ansible & Docker

Today I dockerized an Ansible workflow within a container running on RedHat UBI image. My general idea was create a container environment to execute some Ansible playbooks, these playbooks requires a specific Ansible, Python and Paramiko version to work properly and to avoid dependencies issues in my machine and install a specific old version of a dependecy I decided to execute the Ansible playbooks inside a Container. The final result was good, I can execute the plabooks within the container and I learned multiple things about RedHat UBI images.

### Day 2051-52-53: Watchdog

During that time, I continued working on the Java Multithreading and Concurrency course on Udemy. One of the main things I learned was the watchdog mechanism, which monitors systems and detects lockdowns or dead systems. I had never used this concept before, but I will implement it with Java code in my current project to detect when the system is down or when there are deadlocked threads. I created a basic implementation of the system using Java code to simulate deadlock states in some threads, leaving the watchdog to detect those threads and recreate or destroy them. I have completed 60% of the course, and I will continue working on it in the coming days.

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
**Day 1851 - 1900 Python | Airflow Certification | Cloud certifications | Data Engineering | Spark** [here](./day1501-2000/day1851-1900.md)</br>
**Day 1900 - 1950 IBM Cloud Certification | Parquet Files | DSA | Python | Java | SQL | Apache Spark | Apache Airflow** [here](./day1501-2000/day1900-1950.mds) </br>
**Day 1951 - 2000:** Java | DSA | Reflection | Concurrency | OOP | Networking | Storage Systems | Testing [here](./day1501-2000/day1951-2000.md) </br>
**Day 2001 - 2050:** Java | Byte/Bit Manipulation | DSA | Concurrency & Multithreading | TDD | C | Networking | Makefiles | Sockets & TCP [here](./day2001-2500/day2001-2050.md)

