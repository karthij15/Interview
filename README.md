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
