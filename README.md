# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer.
Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 1795-96 Machine Learning Services

I studied multiple AWS resources focused in machine learning that, Translator, Rekognition, Kendra, SageMaker, Comprehend and Forecast. It's good how AWS offers specialized services for specific tasks rather than offering a big service to meet all these tasks.  

### Day 1794 More AWS Services

Today I studied more AWS services focused in compliance and monitoring activities, services like AWS Config, Inspector, GuardDuty, Artifact, Secrets Manager and Certificate Manager (ACM). I feel sometimes bored while studying the course and reading the AWS docs to learn more about these services. I am studying the last part of the course approximately I completed the 70% of the course.

### Day 1793 Web Crawling and Software Engineering at Google

Today I began to create a WebCrawler to extract article information from a platform like Amazon. My idea is to create a dataset with product information and this dataset can be used for any purpose. I continue reading the Software Engineering at Google book is amazing how Google manage some software aspects in the company. 

### Day 1792 AWS Integration

Today I created an AWS integration using EventBridge and Lambda AWS services. I configured EventBridge as a cronjob to trigger a Lambda function, the lambda function only makes an HTTP request to an external API to extract information. Also I configured EvenBridge to catch the event when a user upload a file to a S3 bucket and then send a email notification with SNS.

### Day 1791 AWS SNS, MQ, Kinesis

Today I studied about the SNS, MQ and Kinesis AWs services, I created a simple SNS to send some messages by email to the subscribers. I love to work with messages brokers like RabbitMQ, Apache Kafka, ActiveMQ, etc. One of my possible areas of expertise can be Message Brokers.

### Day 1790 AWS SQS Simple Queue Service

Today I started to study one of the most important AWS services, I love work with message brokers like RabbitMQ, Apache Kafka, Nexus, ActiveMQ, etc. SQS is a simple message queue like a kafka topic, or a RabbitMQ queue. I want to build an ETL application to use SQS to push my data events to be processed by a consumer.

### Day 1789 CloudFront, Global Accelerator and more

Today, I continued studying for my AWS certification. I learned about interesting services like CloudFront and Global Accelerator. It’s amazing how AWS offers great cloud capabilities, such as the Global Accelerator, to improve application performance using AWS private resources like the private network and multiple edge locations around the world.

### Day 1788 Route53 & Latency

Today I learned about the AWS Route53 service, with this AWS service you can register a domain name and then configure the routing rules for the domain name. I don't want to register a domain name in Route53 because I am looking for other cheaper options, with AWS I have to pay for registering the domain name, $0.50 per month and the number of requests answered by Route53. In other things I learned about latency in networking related to servers close to your end users, I learned a wikipedia article about latency: [latency](https://en.wikipedia.org/wiki/Latency_(engineering)). In simple words latency is how much require a network package to be sended to the client like a web browser.

### Day 1787 More AWS Services and pyspark

Today I continue with my AWS certification studying services like CodeDeploy, CodeBuild, CodeArtifact, CodePipeline and System manager. I learned that AWS have services dedicated for specific problems like do you want to create a Java JAR for example or maybe a native executable, you will need to use CodeBuild for this tasks rather then other cloud providers that offers complete solutions the most common example is create a CI/CD pipeline to deploy an application, with AWS you can use separate services to achieve the task. Also I practiced pyspark a little, reading datasets from hugging face and manipulating them.

### Day 1786 AWS Infrastructure Services

Today I studied about the different AWS services to create resources in an easy way like infrastructure as a code.
I studied the CloudFormation, AWS Cloud Development Kit & Beanstalk. These services are created to create another services like EC2 instances, S3 buckets, Load Balancer, etc. For me CloudFormation is like terraform.

### Day 1785 AWS Lambda and Two Pointer Algorithms

Today I studied the AWS Lambda Service in my AWS course. AWS Lambda is a great free service, with Lambda you can run 1 million functions every month for free. I love that it provides a code editor for Java, Python, NodeJS and Ruby, so you can easily edit your Lambda functions in the same AWS console page. I solved a medium algorithm question related to two pointer technique, when I saw the problem I noticed that I solved this problem in the past with Java, so I solved this time with Python.

### Day 1783-84 AWS DynamoDB

Today I studied the Amazon DynamoDB, DynamoDB DAX and DynamoDb Global Tables. DynamoDB is a NoSQL database designed to offers low-latency and milliseconds operations. With DynamoDB DAX you can reduce the response time to microseconds, DAX is a in-memory cache service to create a layer between your DynamoDB tables and the application. If you want to have your data replicated across multiple locations in the world, DynamoDB global tables is the service that you need to use.

### Day 1782 Amazon RDS and Python

Today I started to learn about Amazon RDS in my AWS certification. Amazon RDS is a service that offers different SQL database engines to create a fully managed SQL database, engines like Oracle, MySQL, PostgreSQL, etc. I created a MySQL database and a python client application to perform basic SQL operations like, create a database, create a table, insert and read records. You can found the Python client in the next gist [client](https://gist.github.com/pablohdzvizcarra/19144156ffeb27e6932cb6401a9ac625). I want to test the Amazon Aurora database but is not available in the Amazon AWS free tier, Amazon Aurora offers better speed and performance that MySQL and PostgreSQL databases.

### Day 1781 Solving Algorithms

Today, I only practice solving two LeetCode problems. I have a goal to write my status in this repository every day and continue to practice my DSA skills, this is a commitment on my part to progress in my software engineering career and build discipline in my career and life.

### Day 1780 Continue with AWS Certification Fighting with Spark

Today I have been studying for my AWS certification, I completed the section 8 about S3. In other things I was attempting to execute
a Spark cluster in a Docker container in my remote server, however I can achieved this, I attempted multiple ways like using the bitnami version, some versions from the community and anything works. At the end I installed Spark in my local machine with homebrew. I needed to install Spark because in my job I start to work with this technology and Apache airflow, Data Engineering is coming.

### Day 1779 Amazon S3

Today I started to learn about S3 buckets in AWS. The S3 buckets for me are just digital pieces of software where you can store data.
In S3 buckets terminology all the files storage are called objects and each object have assigned and unique ID.
The rule that an S3 bucket must have a unique name and that this unique name must be unique across all AWS accounts was amazing to me.
I learned how to use an S3 bucket to host a website, I created an HTML web page and uploaded it to the bucket to be used by other users.

### Day 1778 AWS ELB & LeetCode 36 Problem

This morning I continued studying for my AWS certification, this time studying the different AWS Load Balancer options available.
For my DSA study I solved a medium algorithm problem, this problem was difficult at the beginning and I need to work on the problem for more than 1 hour,
I reviewed the better solutions to the problem, but for me these solutions were hard to understand, they used a lot of maths in the solution.
My implemented solution for me is easy to understand and works with great performance.

### Day 1777 Ephemeral Volumes

Today I learned the ephemeral storage options in AWS. I am learning about the different Storage options for EC2 instances like EBS, EFS, Amazon FSx and EC2 instance storage. EC2 instances storage offers a better performance than EBS but the trade-off is manage ephemeral storage this means if the instance is stopped or deleted you will lose all your data, also I learned that Amazon has an option for Windows File system because mots the Storage options are designed to work on Linux instances. I read the Kubernetes documentation about [ephemeral volumes](https://kubernetes.io/docs/concepts/storage/ephemeral-volumes/).

### Day 1776 Longest Consecutive Sequence & Product of Array Except Itself

Today I continue to solve algorithm problems. Today I solved two medium algorithms according to the roadmap, for the first algorithm I had to find the longest consecutive sequence in an array without sorting the array. Solving this without sorting the array was hard, I had to look on YouTube for some hints to solve the algorithm. The second was less complicated, but I also need to look for help to understand the problem. When I don't know how to continue with the X algorithm, I go to YouTube and look for an explanation of the problem and the general idea of how to solve it without seeing the code solution.

### Day 1775 Continue with AWS

Today I continue studying my AWS certification, I am studying a lot of stuff about EC2 AWS service it's amazing how AWS have a lot of different types of instances
and usage plans to adapt to any specific workload.

### Day 1774 Array & Hashing Algorithms

Today I continue to solve the array & hashing problems from the NeetCode roadmap [here](https://neetcode.io/roadmap). This roadmap is very good for me because
I did not have a clear idea how to study DSA, the author of this roadmap suggests it as a good starting point for the DSA world. In other videos other people
suggest to solve the **top interview 150** LeetCode problem list, my goal is to solve the roadmap first and then continue with the LeetCode specialized lists.

### Day 1773 AWS EC2

Today I have been studied and create an AWS EC2 instance. I learned multiple things about EC2, how we manage the
inbound and unbound network traffict to an EC2 instance using Security Groups, how to connect to an EC2 instance using SSH
with a private key, connect to to he instance with the Browser. AWS offers different types of EC2 instance for different types of workloads
like data science, data analytics, batch processing, caching, etc. I created today an EC2 instance and configure an apache HTTP server
with `httpd` and configure a default HTML page to show a basic web page to the end users.

### Day 1772 AWS IAM

Today I studied about the IAM (Identity and Access Management) AWS service to admin our AWS account access. I learned about the authentication and authorization flow.
Groups can have multiple users, the actions that a group can perfom are defined by Policies. For example we can a developers group and this group have access to use S3 buckets.
I am studying this concepts and refreshing my knowlegde of them, I remember in the past working in my Oracle Cloud certification, I learned all these topics, but in my jobs
as a software developer I never use a variable range of multiple Cloud services profesionally.

### Day 1771 Regions, Availability Zones, Data Centers and Edge Locations

Today I learned about Regions, Availability zones, data centers and edge locations in my AWS study. In the past I studied all off this
concepts making my Oracle Cloud certification but with the time I forgot it, in my current job my cloud computing usage is little, we only use a Database in the cloud
and the others services are out of the cloud. A Region is composed by some availability zones and an availability zone is composed for three or more data centers.
For the moment I am learning the basic concepts of cloud computing, and I am in the IAM part of the course.

### Day 1770 Studying Greedy Algorithms

Today I continued stuying about Cloud computing and solving some LeetCode question about Greedy algorithms.

### Day 1769 Cloud Computing Certifications

I am doing two cloud certifications, IBM Cloud Advocate and AWS Cloud Practitioner. In the work they have the inniciative to offer some certifications to make available for the employees. I signed up for these two and the study schedule starts this week.
I feel like in school because we have study groups and also every week we have a validation step to ensure we are studying the certification. I will have to reduce my DSA study to focus on this, I don't want to stop my DSA study because if you stop you require another effort to start again and remember the things.

### Day 1768 Brute Force Solutions

Today I solved two problesm with the **Brute Force** solution, the problem with this was the problems can pass all the test cases
due to the time complexity, I will need to think in a way to improve the time complexity for each problem. I see a YouTube about
how undertand the problems and the logic to solve with a better approach, it's amazing how if you type in Youtube any problem name
you find some videos with the explanations.

### Day 1767 Creating My RoadMap and Continue with DSA

Today I have created my career roadmap. My goal is to work in Netflix as a software engineer in the future, I know
I know that the journey to reach Netflix is very hard, like climbing a very inclined mountain with your hands.
When you have a goal defined and cleared for you, it is easy to maintain the focus towards that goal,
also it is important to do only the necessary things to achieve that goal. DSA is sometimes boring and having a goal is
important to face those boring moments.

### Day 1766 Medium Blog

Today I completed and pusblished a Medium blog post, you can read the post [here](https://medium.com/@pablohdzvizcarra/a-common-sense-guide-to-data-structures-and-algorithms-quick-book-resume-c1ca9d86a4f4).
The blog post is about my book review of the A Common-sense guide to data structures and algorithms book, that I finished to read some weeks ago. This book helped me to understand
DSA, teach me new things about DSA and refresh my current DSA knowledge. I continue with my DSA study solving LeetCode questions, I started a Udemy course about DSA [50 Days of LeetCode Questions with Python](https://www.udemy.com/course/leetcode-in-python-50-algorithms-coding-interview-questions/),
This course is amazing because first the teacher presents the problem, second explain the problem with simple words, also suggets the pattern to solve the problem and finally show the code solution.
For me see the two videos about the explanations are great and next attempt to solve the problem without see the solution, I want to have a course to continue study DSA because making random LeetCode problems for me is not fun.

### Day 1765 Pointers in Arrays

Today I have been solving some LeetCode problems realted with arrays. For solve some of them using a pointer an a while loop is better that the common
for loop approach. I feel sometimes not able to solve algorithms, is amazing how easy algorithms are hard at the start. Practice make the master I don't know if the phrase
is correct write on English, practice and learning is the way to achieve this.

### Day 1764 Kadane's Algorithm

Today I started to study the [Amazon SDE Sheet](https://www.geeksforgeeks.org/amazon-sde-sheet-interview-questions-and-answers/?ref=outind#Language) looking for a future work on Amazon.
I started with the beginning making an OOP test and with the first algorithm problem Find the maximum sum on a subarray, working on this code exercises I discovered the [Kadane's Algorithm](https://en.wikipedia.org/wiki/Maximum_subarray_problem)
If you can understand how to implement this algorithm with code, you can easily solve the problem. I discovered that in Java, if you use Math.max() with negative numbers, it returns the lesser number example: `Math.max(-1, -100) -> -1`.
It's amazing how we can think we know how something works after having an "aha" moment. I am studying for the moment 1 day DSA and the next advance in my Cloud certifications, and again, again. But when I feel bored I code something only for fun.

### Day 1763 Tired About Support in Work

Today, I felt tired working on support tasks at my job. It’s demotivating to work on a project that’s scheduled for sunset, where my role is solely maintaining the existing codebase without adding new features or improvements. I’m determined to find a way to change this situation because it’s driving me crazy. On a positive note, I recently learned how to package a Java application into a native executable using GraalVM. Although I encountered some issues with application dependencies, I managed to solve them by the end of the day.

### Day 1762 R and Scala Code

Today, I have been working on creating an application to generate a report from some information. I started learning R because I heard that it's one of the best programming languages for performing analytical operations on data. At first, R seemed strange since I come from a background in statically-typed languages like Java, which require a lot of boilerplate. However, I found that R is simpler than Python. I was able to complete the task and create the R application to generate the report. I will attempt to replicate this task with Scala because I love JVM languages, and for me, statically-typed languages like Scala are better

### Day 1761 Depth Level in a Tree

Today I learned how to know the know the depth level of a binary tree using BFS. I solved three problems related with binary trees using BFS, I needed to remember how the BFS algorithm works, and how implement them with Java. I continue having problems to solve medium leetcode problems, and also easy problems. for Java today I learned how to create a binary executable from a java JAR file, it's amazing how GraalVM can create binary executables from Java code.

### Day 1760 Overlaping Problems

Today I have been working on solving LeetCode questions related with Overlaps. I learned a new math concept Interval Coverage, this types of problems. I solved one problem related with timestamps, how do you know if within an array of intervals, two intervals have a conflict, normally we need to use greedy approach and consider edge cases to solve these type of problems.

### Day 1757-58-59 LeetCode Problems

During these days I continue on solving LeetCode problems, I attempted to solve some Medium problems without great results, Medium problems continues be complicated for me yet. Sometimes I also fight with some easy questions, really DSA is hard and fun at the same time. I attempted to feel motivated working on this, when I solve X problem I feel with super powers, is a very good sensation.

### Day 1756 Continue Solving Matrix Problems

Today I continue solving Matrix problems, I learn how to traverse the boundaries in a Matrix following the clockwise direction, it's interesting how with programming you can solve any type of problem, this simulation problems are helping me to understand other type of problems.

### Day 1755 Matrix Algorithms

Today I am solving matrix algorithm problems, solving a LeetCode problem yesterday I discovery that I have a lack of knowledge about matrix DSA and algorithms. I am studying about the Matrix DSA on GeekForGeeks [here]("https://www.geeksforgeeks.org/matrix/?ref=lbp"), this resource is very good to learn about DSA and have a lot of problems to solve practice.

### Day 1753-54 Completing the A Common Sense Guide to Data Structures and Algorithms Book

During the weekend I completed the book A Common Sense guide to DSA and algorithms, I am writing my book review in a Medium blog post. I am very happy to complete the book, I learned a lof things about DSA and algorithms and well I feel my Software Engineer skills are improving. The next step is continue studying these topics practicing with algorithms problems in LeetCode and GeekForGeeks.

### Day 1752 Counting Sort

Today I learned a new sorting algorithm called **Counting Sort**, this algorithm is great when we have a limit range of numbers to sort, the algorithm has a time complexity of `O(N + K)` where `N` is the number of elements to sort and `K` is the range of the numbers.

### Day 1751 Coding Exercises

Today I have been solving the final book exercises. This book exercises are designed to learn how to optimize algorithms, the problems starts with an explanation about the problem, and the worse time complexity to solve, the idea is use optimization techniques like lookup tables with Map, change the data structure and Greedy techniques to improve the time complexity.

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
**Day 1601 - 1700 Java | Go | Data Structures and Algorithms | A Common-Sense Guide to DSA Book** [here](./day1501-2000/day1706-1750.md)</br>
