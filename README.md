# Spring security 

Spring Security is a powerful and highly customizable authentication and access-control framework. 

It is the de-facto standard for securing Spring-based applications.

Spring Security is a framework that focuses on providing both authentication and authorization to Java applications. 

the real power of Spring Security is found in how easily it can be extended to meet custom requirements
with the help of Spring Dependencies

Many comprehensive technologies can be added with minimal configuration and adding dependencies

 # Features
Comprehensive and extensible support for both Authentication and Authorization

Protection against attacks like session fixation, clickjacking, cross site request forgery, etc

Servlet API integration

Optional integration with Spring Web MVC

Much more…

It Handles Common Vulnerbality out of the box

- session fixation
- clickJacking
- Click site Rquest Forgery
- Widely adopted

## what can be done

- username/pswd authentication
- SSO like okta or LDAP
- App level Authorization
- OAuth 
- Microservice Security
  

## 5 Main concepts of Security

- Authentication
- Authorization
- Principal
- Granted Authority
- Roles
 
## **Authentication**

User Authentication For any Web application which can be configured for validating the correct user name and password
and various type of authentication are available such as 
LdapAuthentication
DaoAuthentication
inMemoryAuthentication
and more

## **Authorization**

Levels of Access In different end points can be controlled in Spring Boot with differentiating in Users providing them roles 
just Like Admin is a Role 
 


## **Principal**
Currently Logged in User . Application Remembers the currently Logged in User with there information Stored in runtime refered as Principal .


## **Granted Authority**

Permissions Given To Users For Specific Requests/operation In the application which can be configured In a List of Auuthorities Which have to be assigned to specific User 

## **Roles**
Group OF Authorities can be added for particular set of people which is Known AS roles.



# What Is Ldap

LDAP stands for Lightweight Directory Access Protocol. As the name suggests, it is a lightweight client-server protocol for accessing directory services .
LDAP directory servers are often used as an authentication repository, and are often used to store sensitive information like passwords and other account details.

# Why Ldap
The best part about using LDAP is that it is a well-defined protocol. Unlike the NoSQL database or RDBMS, LDAP is explicitly specified how clients should encode requests. When using the alternative technologies like NoSQL database, you’re you are likely to lock yourself into that one type of database as this has its protocol.
 
# Setup LDAP

* Add dependencies to the pom.xml
```

<!--Local ldap server--!>
<dependency>
   <groupId>com.unboundid</groupId>
   <artifactId>unboundid-ldapsdk</artifactId>
</dependency>

<!-- connection provider and implementaiton Spring  --!>
<dependency>
		<groupId>org.springframework.ldap</groupId>
		<artifactId>spring-ldap-core</artifactId>
</dependency>

<dependency>
		<groupId>org.springframework.security</groupId>
		<artifactId>spring-security-ldap</artifactId>
</dependency>

```
configure properties

spring.ldap.embedded.ldif=classpath:test-server.ldif
spring.ldap.embedded.base-dn=dc=springframework,dc=org
spring.ldap.embedded.port=8389

and test-server.ldif file

https://spring.io/guides/gs/authenticating-ldap/

https://github.com/kapil0jaiswal/SpringSecurity

benspassword