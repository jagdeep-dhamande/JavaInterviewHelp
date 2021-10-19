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
