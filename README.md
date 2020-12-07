# Interview
Some of the Interview Questions

# Optum Insight - Chennai

## First Round: Online f to f

1. Is it possible for an abstract class to extend another abstract class?
2. how many interface can one interface extend?
3. Is constructor present in abstract class
4. is it possible to create an object for an abstract class?
5. write a sql query to find the users who are not logged in more than 7 days.
   consider two tables  
    Users:  
      userid  
      firstaname  
      lastname  
      emailid  
      password hash  
      passowrd  
  
    userloginHistory:  
      userid  
      logintimestamp  
6. Write a function boolean sumOf2(int[] arr, int sum) which returns true if there is a pair of numbers in arr that add up to sum.
7. find number of rotation performed in roated sorted array. 

## Second Round: Online f to f
1. int[] arr = new int[]{12, 34, 56, 789, 567, 345, 234 ,123}; - Array of integers ordered as increasing and starts decreasing. 
   Find the maximum element.

2. String str = #A@FT%S#GHU;
   Reverse the string and maintain the index of the special characters.
   
3. Difference between abstract classes and interfaces.
4. Advantages of Spring Boot over Vanilla Spring.
5. How Spring Beans work internally?
6. Explain about Apache Solr.
7. Explain about Apache Kafka.
8. How google search works, How the data was stored and which data structures was used.
9. Difference between REST and Kafka, Which one do we have to prefer on what scenario?
10. Explain about GC? which algorithm used in it.

## Third Round: Online f to f
1. what is docker? how you deploy your application in the machine.
2. what is kubernetes? how it differs from docker?
3. Difference between RabbitMQ and Kafka
4. What is API Gateway?
5. What is Service Registry and Service Discovery in Microservices.
6. Explain circuit breaker
7. How two microservices communicate to each other? 
8. SQL Query to get list of credited and debited details having amount greater than 500 group by userid
   incoming                         outgoing
    - user id                    - user id
    - amount                     - amount
    - date                       - date
    
    total incoming
    total outcoming
    for each day
    amount > 500

## Third Round Second Time online f to f - Optum Advisory Board
1. How much volume of data you have migrated in your project?
2. Server capacity and memory allocation for your servers in production for the proposed volume of data.
3. How sharding can be done for mongodb? 
4. Design a system to input a large file containing book tiles and response query for word search.
   why you use solr and mongo? what's the purpose of mongo over here>.
5. Replace a request of stock results for company to a request takes multipe stock request for different companies and responds the results without affecting the time. 
it should response results as quick as the previous ones. 
6. How you will process a large set of files. For example take a log system having terra bytes of data in singe file process the file, mask the desired data in the log text and write back to a file.
7. how will you merge the chunks without data overlapping.
8. Have you trained any junior resources before.
9. which spring boot version are you using?


# Glovo - Spain

## First Round - Screening
1. pros and cons of using microservices agains monolith. Difference, advantages and disadvantages of Monolith and microservice architectures.  
2. Time complexity to get an element in array and list. 
3. Difference between MySQL and NoSQL - Explain CAP Theorem. 
4. Explain about JVM. 
5. Explain Time and Space Complexity. 
6. Explain CI/CD 
7. Explain your TDD Process. 
8. Horizontal vs Vertical Scaling. 
9. Explain SOLID Principles. 
10. Difference between Process and Threads. 

## Second Round - Coding in Codility

1. Find the first repeating character in a String. Order of the character to be considered.  
   Ex: ABCA - A  
       Glovol - l  
       
       ```
               public String findFirstRepeatingCharacter(String s) {
            LinkedHashMap<Integer, Integer> charOccuranceMap = new LinkedHashMap();
    
            char[] charArr = s.toCharArray();
    
            for(int idx = 0; idx < charArr.length; idx++) {
                // System.out.println("" + (char)charArr[idx]);
                // Character c = (char)charArr[idx];
                int occuranceCount = 1;
                Integer charVal = (int)charArr[idx];
    
                if(charOccuranceMap.containsKey(charVal)) {
                    occuranceCount = charOccuranceMap.get(charVal);
                    occuranceCount++;
                }
                charOccuranceMap.put(charVal, occuranceCount);
            }
    
            for(Map.Entry<Integer, Integer> entry : charOccuranceMap.entrySet()) {
                //int cInt = entry.getKey();
                //System.out.println( ((char)cInt) + " " + entry.getValue()) ;
    
                if(entry.getValue() > 1) {
                    int cInt = entry.getKey();
                    return "" + (char)cInt;
                }
    
            }
    
            return "";
    
            /*
            int[] HASH = new int[256];
    
            char[] charArr = s.toCharArray();
    
            int idx = 0;
    
            while(idx < charArr.length) {
                HASH[charArr[idx]]++;
    
                if(HASH[charArr[idx]] > 1)
                    return "" + charArr[idx];
    
                idx++;
            }
    
            return "";
            */
        }
       ```

2. Paranthesis Match.  
   ()[]{} - true  
   ([]) - false  
   
   ```
           public boolean isParanthesisBalanced(String s) {
            
            char[] charArr = s.toCharArray();
            
            Stack<Character> charStack = new Stack();
            List<Character> openBracesList = Arrays.asList(new Character[]{'(', '[', '{'});
            List<Character> closeBracesList = Arrays.asList(new Character[]{')', ']', '}'});
            
            int indexOfChar = -1;
            
            for(int i = 0; i < charArr.length; i++) {
                if(openBracesList.contains(charArr[i])) {
                    indexOfChar = openBracesList.indexOf(charArr[i]);
                    charStack.push(charArr[i]);
                }
                
                if(closeBracesList.contains(charArr[i])) {
                    if(closeBracesList.indexOf(charArr[i]) != indexOfChar)
                        return false;

                    charStack.pop();
                }
            }
            
            System.out.println("--- isBalanced: " + charStack.isEmpty());
            return charStack.isEmpty();
        }
   ```
# Ericsson - Chennai
   
## First Round
1. Difference between an Abstract class and Interface. 
2. Can We have main() method in Abstract Class? 
3. How to remove duplicates in ArrayList?
4. Which is the preferred datatype for storign password?
5. Difference between HashMap and HashTable
6. Do you konw about Collections.synchronized() ?
7. Difference between Collections.synchronized(HashMap) and ConcurrentHashMap
8. What is the difference between an ordered and a sorted collection?
9. Consider We have a map having integer key and string value. Can you sort the Map withe ascending order of keys.
10. Can you explain overriding and overloading?
11. Is it possible to declare a variable final and not initializing values. ex: final int a;
12. StringBuffer vs StringBuilder
13. What is a memory leak?
14. Consider a system is having out of memory exception. How will you debug?
15. Consider there is a REST API Service, which you have to call from your java application. the REST Service will be down if more than 3 requests accessed at a time. Add rate limit in the java application.
16. First unique character in a String 
   ex: "ABCAAC"
   ans: "B"
17. Can you explain Singleton?
18. Can we declare a class Static in Java?
19. In java which are all stores in Stack memory and Heap memory.
20. can you differentiate == with equals method.
21. What is the contract between equals and hashcode method.

## Second Round
1. Find the largest two numbers in an Integer Array
2. JVM Memory Management
3. String, String Buffer and String Builder - Comparision, Which is Efficient?
4. When ArrayList compared to LinkedList which is best of read operation and which one for right operation?
5. Explain SOLID Principles
6. What is the Major advantages of Loosly Coupled System(Data Abstraction), Why We have to go with Dependency Injection.
7. What is Data Abstraction.
8. How to provide thread safety for a class having one variable and one method. without using Synchronization.
9. Explain Kafka, Partition? Why Partition is used how the partition limit was determined?
10. What is Hadoop? Explain Map-Reduce
11. Difference between Error and Exception
12. How to avoid Exception?
13. What is High Availability?
14. Explain o(LogN). Explain the search between ordered array and unordered array.
15. Explain about GC. Which one you are using?

## HR Manager Round
1. Why you are leaving your present company?
2. Are you willing to migrate?
3. how to deal with the client which continuously brings new requirement and want it for yesterday, etc
4. what is your goal in your life?
5. Explain one problem where you outwitted yourself.

# EMBL-EBI (EBI01693) Sofware Developer London

## Hacker Rank Round
1. what would be the output?  
```
	class Test {

	public static void main(String...args) {
		try {
			badMethod();
			System.out.println("A");
		} catch(Exception e) {
			System.out.println("B");
		} finally {
			System.out.println("C");
		}
			System.out.println("D");
		} 

		public static void badMethod() {
		}
	}

```
2. What would be the output ?

java Test -DopenDog=Roetweeler

```
		class Test {

			public static void main(String...args) {
			   Properties p = System.getProperties();
			   p.setProperty("dog", "scrunky");
			   String openDog = p.getPropert("openDog");
			   String dog = p.getProperty("dog");
			   dog += openDog;
			   System.out.println(dog);
			}
		}

```

3. What is the root(apex) of exception hierarrchy in Java?
4. How many return statements are allowed in python function?
5. Write a python program contains functions to remove vowels in a string and consonents in a string. print seperately.
6. Write default implementations for an interface in java
7. What would be the output of the below function
```
		a = 0
		for b in range(0, 10, 2):
			a += b + 1;

```
8. What would be the output of the below function
```
   def foo(a, b, c) : pass
```
9. A multiple choice question contains key value paris. Which of the below is the correct key value combination in hashtable.
10. select id, name from customer and sort the values by name ascending if two of the customer has same name then sort those by id asc.
11. A merchant has 1000 kg of sugar, part of which he sells at 8% profit and the rest at 18% profit. He gains 14% on the whole. The quantity sold at 18% profit is?
12.  What would be the output?
```
   int[] a = new int[]{1,2,5,2,3,7,9,1,2,6};
   add elements of array to a set
   add set values to a list and sort it by ascending 
```
13. REST constraints based question
14. FizzBuzz in Java (Sample Program) - runtime of the program should not exceed 4ms
Write a program that outputs the string representation of numbers from 1 to n.

But for multiples of three it should output “Fizz” instead of the number and for the multiples of five output “Buzz”. For numbers which are multiples of both three and five output “FizzBuzz”.


```
   public List<String> fizzBuzz(int n) {
        
        List<String> result = new ArrayList<>();
        
        if(n < 1) return result;
        
        for(int i = 1, fizz = 3, buzz = 5; i <= n; i++) {
        
            String addVal = null;
            
            if(i == fizz && i == buzz) {
                addVal = "FizzBuzz"; 
                fizz += 3;
                buzz += 5;
            } else if(i == fizz) {
                addVal = "Fizz";
                fizz += 3;
            } else if(i == buzz) {
                addVal ="Buzz";
                buzz += 5;
            } else
                addVal = String.valueOf(i);
            
            result.add(addVal); 
        }
        
        return result;
    }
```
15. URI constraints based question. (Sample)
16. Which of the following data structures can erase from its beginning or its end in O(1) time? (Sample)

# Auto1 German
1. Explain Yourself
2. Why are you switching job?
3. Why Auto1
4. REST - What is Itempotent methods?
5. Explain HTTP Methods
6. Which HTTP Methods are Safe? - An HTTP method is safe if it doesn't alter the state of the server. In other words, a method is safe if it leads to a read-only operation. Several common HTTP methods are safe: GET , HEAD , or OPTIONS . All safe methods are also idempotent,but not all idempotent methods are safe
7. Spring - Spring bean scopes
8. Spring - Which Spring bean scope is thread safe(Singleton not thread safe)
9. Types of Autowiring - (The autowiring functionality has four modes. These are ' no ', ' byName ', ' byType ' and ' constructor ')
10. Transaction propagation in spring - 
11. Java - contract between equals and hashcode method
12. Functional Interfaces - and its types
13. List which collections from java you've used
14. Super class for unchecked exception and for checked exception?
15. How long you need for relocation
16. Salary Expectation

# SquareShift - Chennai

## First Round
1. Air Plane Seating alogrithm : https://github.com/karthij15/squareshift

## Second Round
1. Drawbacks of Monolith
2. Explain a scenario which you come across related to data incosistency
3. How will you handle inventory out of stock scenario
4. How you will review a code? Review your submitted code.

# PayPal - Chennai

## First Round
1. Explain about yourself
2. Deep questions about previous projects
3. Few of My GitHub programs discussed LRUCache, RotateArray
4. Rotate characters in a string not using the above RotateArray approach (used string concat and substring)
5. Do left rotate and again right rotate the characters(cancel the repetetive approaches). Refactor the code.

## Second Round
1. 3 different array having elements in different sequential orders. combine in single array in ascending order
   S1 [1, 4, 9]
   S2 [2, 5, 7, 8]
   S3 [3, 6]
   
   Result [1, 2, 3, 4, 5, 6, 7, 8, 9]
  
2. Design a TinyURL System

### Third Round
1. Why Kafka Over ActiveMQ
2. What's your typical Day!
3. How are you managing your team
4. Given a sorted array of integers, find the starting and ending position of a given target value.
   If the target is not found in the array, return [-1, -1].
   Example:
   Given [5, 7, 7, 8, 8, 10]
   and target value 8,
   return [3, 4].
5. A [ 8, 23, 22, 16, 22, 7, 7, 27, 35, 27, 32, 20, 5, 1, 35, 28, 20, 6, 16, 26, 48, 34 ]
   Return the first lowest number lower than the current index
   The expected returned value :
   O: -1 8 8 8 16 -1 -1 7 27 7 27 7 -1 -1 1 1 1 1 6 16 26 26

# Altimetric - PayPal Interview

## Hacker Rank Round
### Program 1.
The longest palindromic substring of the the given input.
  Ex:  hackerrekcahbahh 
  Ans: hackerrekcah
### Program 2.
You just got a new job where you have to work exactly as many hours as you are told each week, working no more than a daily maximum number of hours per day. Some of the days, they tell you how many hours you will work. You get to choose the remainder of your schedule, within the limits.

A completed schedule consists of exactly 7 digits in the range 0 to 8 representing each day's hours to be worked. You will get a pattern string similar to the schedule, but with some of the digits replaced by a question mark, ?, (ascii 63 decimal). Given a maximum number of hours you can work in a day, replace the question marks with digits so that the sum of the scheduled hours is exactly the hours you must work in a week. Return a string array with all possible schedules you can create, ordered lexicographically.

For example, your partial schedule, pattern = 08??840, your required hours, work_hours = 24, and you can only work, at most, day_hours = 4 hours per day during the two days in question. You have two days on which you must work 24 - 20 = 4 more hours for the week. All of your possible schedules are listed below:

0804840
0813840
0822840
0831840
0840840
Function Description
Complete the function findSchedules in the editor below. The function must return an array of strings that represents all possible valid schedules. The strings must be ordered lexicographically.

findSchedules has the following parameter(s):

work_hours: an integer that represents the hours you must work in the week

day_hours: an integer that represents the maximum hours you may work in a day

pattern: a string that represents the partially completed schedule

Constraints
1 ≤ work_hours ≤ 56
1 ≤ day_hours ≤ 8
| pattern | = 7
Each character of pattern ∈ {0, 1,...,8}
There is at least one correct schedule.
Input Format For Custom Testing
The first line contains an integer, work_hours The second line contains an integer, day_hours The third line contains a string, pattern

Sample Case 0
Sample Input 0

56
8
???8???
Sample Output 0

8888888
Explanation 0

work_hours = 56
day_hours = 8
pattern = ???8???
There is only one way to work 56 hours in 7 days of 8 hours.

Sample Case 1

Sample Input 1

3
2
??2??00
Sample Output 1

0020100
0021000
0120000
1020000
Explanation 1

work_hours = 3
day_hours = 2
pattern = ??2??00
You only need to schedule 1 more hour for the week, and it can be on any one of the days in question.

### Program 3
Multiple processors running with different process, find processors, required

Given there are multiple processors available to execute the given program. Each program are split into multi process in such a way each process has some start time and end time based on the time it takes to run. Different process are feed to processors to execute, goal is to minimize the time taken and ensure the processors are completed with least time. Find out the minimum no of processors required to execute the given processes. No of process and its start time to execute the process is been provided. Use the compute method to find the minimum number of processors required to execute them..

Example

with the given starting time of the process, ending time of the processes as below need to identify the minimum number of processors required.

//as far remembered two array of times will be the input. expected output is an Integer
String[] start_time = new String["12.09.20:09:39", "09.09.20:09:39", "01.08.20:09:39"]
String[] end_time = new String["03.01.20:09:39", "02.09.20:09:39", "01.08.20:09:39"]

### Multiple Choice Questions
1. What would be the output?
```
int a = 260; 
byte b = (byte)a;
System.out.println(b);

```
2. What would be the output ?
```
int[] a = new int[] {1, 2, 3};
int[] o = Arrays.copyOf(a, 5);
int[] c = Arrays.copyOfRange(o, 0, 4); //line 3
for(int i : c) {
    System.out.println(i);
}
```

Compile Error: line 3 returns int not int[].

3. what would be the output?
```
int temp = 40;
if(temp == 30 && temp/0 == 4) {
	System.out.println(1);
} else {
	System.out.println(2);
}
```
4. What would be the output?
```
for(int i = 0; i > 5; ) {
   System.out.println("Hell0" + i);
}
System.out.println("Completed!");
```
5. what will be the output?
```
String temp = "10.87";
int a = Integer.parseInt(temp);
System.out.println(a);
```
Will throw a RunTime Error

6. What would be the output? 
```
String s1 = "java";
String s2 = s1.intern();
String s3 = "java";
String s4 = new String("java");
StringBuffer sb = new StringBuffer("java");
System.out.println((s1 == s2) + (s2==s3) + (s3 == s4) + (s1 == s4));
```
7. What would be the output?
```
int[] a = new int[10];
byte[] b = new byte[10];
char[] c = new char[10];
double[] d = new double[10];

System.out.println(a[0] + "" + b[0] + "" + c[0] + "" + d[0]);
```
8. What would be the output?
```
System.out.println(1 + 
		2==+
		3+
		+
		+5+ 
		++6 +
		--7);
```
9. What would be the output?
```
String a = "abc";
String b = "abc";

System.out.println(a == b);
```
10. what would be the output?
```
int b = 96;
System.out.println(b >>4);
System.out.println(b >>>4);
```
11. which of the below statement is wrong?
```
1.int a[][] = {{1,2},{12,2,22}};
2.int b[] = new int[2]{1,2};
3.int i[][] = {{1,2},{12,2,22}}, b = 2;
```
12. what would be the output?
```
public static int temp1  = 1;
private static int temp2 = 2;

private int temp4 = 4;

public static class inner {
	private static int getSumOf2() {
		return (temp1 + temp2);
	}

	private static int getSumOf4() {
		return (temp1 + temp4);
	}
}
```
13. Which line compiler will throw the error?
```
 public static int temp1 = 1; 
 public static int temp2 = 2;
 public int temp3 =	 3; 
 private int temp4 = 4;

 public class InnerClass { 
	 private static int getSum() 
	 {
		 return temp1 + temp2; 
	 }
 }
```
14. What would be the output?
```
class Test {

public static void main(String[] args) {
  int x = 30;
  System.out.println(x);
}

static {
 int x = 10;
 System.out.println(x);
}
}
```
15. Which of the following is correct recurrence for worst case of Binary Search?
(A) T(n) = 2T(n/2) + O(1) and T(1) = T(0) = O(1)
(B) T(n) = T(n-1) + O(1) and T(1) = T(0) = O(1)
(C) T(n) = T(n/2) + O(1) and T(1) = T(0) = O(1)
(D) T(n) = T(n-2) + O(1) and T(1) = T(0) = O(1)

Ans: C

16. Given a sorted array of integers, what can be the minimum worst case time complexity to find ceiling of a number x in given array? Ceiling of an element x is the smallest element present in array which is greater than or equal to x. Ceiling is not present if x is greater than the maximum element present in array. For example, if the given array is {12, 67, 90, 100, 300, 399} and x = 95, then output should be 100.
(A) O(LogLogn)
(B) O(n)
(C) O(Logn)
(D) O(Logn * Logn)

Answer: C

17. What would be the output?
```
public static void main(String[] args) {
    System.out.println("Hello");
    5<6?6:5;
}
```
18. What is the name of this tree?
```

       /       \  
     15         30  
    /  \        /  \
  40    50    100   40
 /  \   /
8   7  9 
```
a) Binary Tree
b) Binary Search Tree
c) Complete Tree
d) Full Tree

19. Level order Tree Traversal also known as _____________________
20. What is Widening Type convertion in Java?
21. Fill the blanks
A Java thread dump is a way of finding out what every thread in the ___________ is doing at a particular point in time. This is especially useful if your Java application sometimes seems to hang when running under load, as an analysis of the dump will show where the ___________ are stuck.

22. List of statements based question about ExecutorService in java, from which we have to identify which one is incorrect amoung them
23. List of statements based question about JVM Heap, PermGen, Xms, Xmx and Xmn in java, from which we have to identify which one is incorrect amoung them
24. List of statements based question about Packages in java, from which we have to identify which one is incorrect amoung them
25. List of statements based question about Generics in java, from which we have to identify which one is incorrect amoung them
    (generics are run time type correctness(X), A lower bounded wildcard is expressed using the wildcard character ('? '), following by the super keyword, (Y))
26. Which of the following is not true for garbage collection?
27. What would be the output?
```
import static java.lang.System.*;

public static void main(String[] args) {
   out.println("test");
}
```
28. Select ONE or MORE Rules manadatory for maitaining URL Standards
29. What would be the output?
```
class NewThread extends Thread {
	public void run() {
		for(int i = 0; i < 500; i ++) {
		System.out.println("i" + i);
		}
    	}
}

class Test {
	public static void main(String...args) {
		NewThread n = new NewThread();
		n.setDaemon(true);
		n.start();
		System.out.println("Completed");
	}
}
```
# Capgemini - Chennai

## First Round
1. Difference between Controller and Rest Controller
2. Difference between Monolith and Microservice
3. Explain some new features of Java 8

## Second Round
1. Explain advantages of Microservices
2. what is blue-green deplooyment
3. What is smart end-points and dumb pipes
4. Can you work as Individual Contributor or Leading a Team?
5. As a part of team lead, what are the qualities you expect to have?
6. What will be the one word, if we ask about you to your manager.
7. Why SpringBoot? advantages over Spring
8. Spring Bean lifecycle?
7. Design Pattern/Architectural pattern behind API-Gateway?

# Optum - Chennai

## First Round
1. Merge two arrays without duplicates
int[] a = new int[]{1, 2, 5};
int[] b = new int[]{3, 4, 6, 2};

output = {1,2,5,3,4,6}

2. Print all permutaions of a String
input a = "abc"

abc
acb
bca
cab
cba
bac

3. PreOrder traversal of a Binary Tree without recursion

4. SQL  queries
a table "product" with columns cost, category, and productname

1. print productname from product having same cost
2. print category from product having more than 3 items

