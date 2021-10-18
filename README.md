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
