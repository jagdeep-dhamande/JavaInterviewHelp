# JavaInterviewHelp

Here I will collect java interview questions and links to there answers

**Spring Boot**
1. How to configure RestTemplate to communicate with other microservice
2. How to create a spring boot application from scratch
3. What happens in background when you start a spring boot application ? 
    - Set up default configuration
    - Starts spring application context
    - Performs full class path scan
    - starts tomcat server
4. How environment configurations are managed for dev/prod/uat environment?
    - Profiles are used to manage environment configuration
    - Different application-<env>.properties are created for different environment
    - Active profile can be configured with "spring.profile.active" property or jvm argument -Dspring.profile.active
5. What is restTemplate ? How it is used ?
    restTemaplate is an implementation provided by spring to build and consume rest API. It provides simple functions to make different HttpMethod calls.
    To use restTemplate it must be automired in required service and its functions can be used directly to make different http method calls like getForObject(<id> , <type>)
    Note : Instance of the restTemplate will not be created automatically by spring , you need add instance function in applicatio class
6. How to avoid database save of model property ?
    Model property can be marked with anotation @Transient to avoid saving/adding in data base. This indicates JPA that property should not be used in any database operation
7. How to tell JPA/ORM that model should be mapped to table?
    Annotation @Entity can be used to indicate spring that model represents the database. 
8. How to map model property as primary key for corresponding database table ? and can it be autogenaretd ?
    With anotation @Id model property can be mapped as primary key of table and with @GeneratedValue its auto generation can be configured.for example
    @GeneratedValue (strategy = GenerationType.Identity)
9. What is CORS ? How it is used in Spring application
    CORS = Cross origin request sharing. In a distributed application  , services might have different domains or different platform written in different languages.
    So request comming to microservice might have different origin. With CORS we can define the verified request origin and also define support for different http methods.
    In spring this can be achieved with @CORSOrigin annotation
10. What are the important unit test annotations you have used in spring boot application ?
    <p>
       - @Mock 
       - @InjectMOck
       - @SpringBootTest = Searches for class having main method and initialises context required
       - @WebMvcTest = Used to test MVC controller , it creates MOck MVC environment and required spring security 
       - @MockBean = Its warpper around Mockito . It mocks all the dependencies for the class under test
        
 **Git**
        
 1. What are different git commands you have used ?
        checkout , branch , add , commit , push
 2. Which GUI based git tool you have used ? 
        Git Tortise , Integration provided in Intellij
 3. What is differnce between Fetch and Pull ? 
        - Fetch brings only list of file changed on remote repository as compared to local repository
        - Pull brings actaul changes to local repository
       
 4. What is difference between reset and revert ?
        <p>   
        reset gives option to move code back to a particular commit id . In this process changes/commits after that particular commit are lost
        <p>
        revert it undo changes done in earlier commit by removing the changes done earlier commit with a new commmit . No changes are lost in this process
 5. What is difference between git rebase and git merge ? when would you use rebase or merge ? 
       Both rebase and merge are used to merge changes of one repository into other . Major difference between both is about keeping the histroy of commits.
       In case of git rebase new commit is made for every commit in main and feature is moved to tip of main. In case of merge commit histroy is maintained and all commits are
       merged as single commit . In case of merge if main branch is very active multiple commits needs to be merged
        
    
            
**Jenkins**
  1) what is jenkins ? 
  2) What is CI/CD ? 
  3) How to write a jenkins file ? 
  4) What are steps to automate the deployment ? 
  5) How to pass params and input to jenkins build ?


**SQL/ Databse Questions**
1) What is order of execution of clause like where , having , group by and group function in sql query?
    1.  FROM
    2.  ON
    3.  JOIN
    4.  WHERE
    5.  GROUP BY
    6.  WITH CUBE or WITH ROLLUP
    7.  HAVING
    8.  SELECT
    9.  DISTINCT
    10. ORDER BY
    11. TOP
