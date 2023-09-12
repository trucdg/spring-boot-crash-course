# Spring Boot Crash Course
- Spring Boot helps to simplify Java development.
- There are many features in Spring Boot, but the 3 popular ones are:
  - Spring Boot Starters
  - Auto Configuration
  - Production Ready

  ![image](https://github.com/trucdg/spring-boot-crash-course/assets/91285203/7b33f28e-5c53-4cf8-8aa1-567c8a78ef21)

## What are we building in this course?
![image](https://github.com/trucdg/spring-boot-crash-course/assets/91285203/b6e4c8b9-f020-46c8-8e21-d73a8600021c)

![image](https://github.com/trucdg/spring-boot-crash-course/assets/91285203/1d4ec4a3-c132-41d0-94da-99a39b35b1bc)

## 1. SPRING CORE:
1. **The IoC Container**:
   
1.1. **ApplicationContext**:
   - is an interface that represent the Spring IoC Containers
   - Similar to BeanFactory, it can load bean definitions, wire beans together, and dispense beans upon requests.
   - imagine: a container as a bin that stores all the classes, and we can ask the bin to give us the class/ component that we want.
     
1.2. **What is a Bean?**:
   - a Spring Bean is just **an instance of a class**, with some configuration.
     
1.3. **@Component**:
   - **class level annotation**
   - indicates that a class is a candidate for autodetection when using annotation-based configuration and classpath scanning.
     
```java
  @Component
  public class Message{
    public String sendMessage(){
        return "Hello there!";
    }
  }
```
     
1.4. **@Configuration** and **@Bean**:
   - **method level annotation**
   - indicates that a method produces a bean to be managed by the Spring Container
   ```java
   @Configuration
   public class AppConfig {
       @Bean
       public MyServiceImpl mySerVice(){
          return new MyServiceImpl();
       }
   }
   ```
