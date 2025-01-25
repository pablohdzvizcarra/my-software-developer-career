# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

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

Today I started a new project. The main is to create a DAG that every day looks in this repository to check the last commit, if the last commit have the format dayXXXX, the DAG will extract the README.md file information and next serialize the README.md file in a Python object format, the idea is extract the last day skills learned entry like this entry and use a LLM to extract the skills learned that day. I want to storage the entries in a SQL database to know which technologies I learned that day. My goal is to continue learning Data Engineering, Airflow, DAG development and AI. You can see the general idea of the project in the next link: https://github.com/user-attachments/assets/ff3312e6-e9f9-46c3-979d-a50aa717a850  

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

Today I read a Substack article about how to growth from a mid-level software engineer to Senior (Article)[https://newsletter.eng-leadership.com/p/how-to-grow-from-mid-level-to-senior?utm_source=publication-search]. The Article was very good, I want this year be promoted in my current company, so I am looking for ways to grow and be a better software engineer. Also I started with the `Plus One` problem, I know that this problem is an Easy question, but well LeetCode says that I answered this problem 1 year ago, but at this moment I don't remember how to solve it, so I started to solve it again. The problem is very simple, you have an array of integers that represent a number, you need to add one to this number and return the result as an array. I will need to continue practicing DSA.

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