
## Ex 01 -Simple Web Server using Spring Boot
## NAME: V. POOJAA SREE
## REG NO: 212223040147
## AIM:
To develop a Simple Web Server using Spring Boot that can handle basic HTTP requests and return appropriate responses through RESTful endpoints.
## ALGORITHM:
Start a New Spring Boot Project:

Use Spring Initializr (https://start.spring.io/)

Select dependencies: Spring Web

Create the Main Application Class:

This class contains the main() method with @SpringBootApplication annotation to bootstrap the application.

Create a Controller Class:

Create a class annotated with @RestController.

Define one or more HTTP request handler methods using @GetMapping, @PostMapping, etc.

Write Endpoint Methods:

Inside the controller, define a simple method for handling GET requests (e.g., return “Hello World” when /hello is accessed).

Run the Application:

Run the application using your IDE or via the command line (mvn spring-boot:run or ./mvnw spring-boot:run).

Test the Endpoint:

Open a web browser or use Postman to visit:
http://localhost:8080/hello

You should see the output (e.g., "Hello World").

Stop the Server:

Stop the Spring Boot server once testing is complete.


## Program 
```
simple-web-server/
├── src/
│   └── main/
│       ├── java/
│       │   └── com.example.demo/
│       │       ├── DemoApplication.java
│       │       └── HelloController.java
│       └── resources/
│           └── application.properties
├── pom.xml
```
 ### Pom.xml
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>demo</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <name>demo</name>
    <description>Demo project for Spring Boot Web Server</description>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>3.1.2</version>
        <relativePath/>
    </parent>

    <dependencies>
        <!-- Spring Boot Web -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
</project>
```
### DemoApplication.java
```java
package com.example.demo;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

### HelloController.java
```java
package com.example.demo;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
@RequestMapping("/api")
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Spring Boot!";
    }
}
```

### application.properties:
```
 server.port=8080
```

### Output:
<img width="1567" height="473" alt="image" src="https://github.com/user-attachments/assets/ecd24251-053b-45e2-8214-3264620170c5" />

### Result:
Thus, the Simple Web Server was successfully developed using Spring Boot. The application was able to handle basic HTTP requests through RESTful endpoints and return appropriate responses for the requested URLs.





