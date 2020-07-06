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
