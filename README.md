# Cinema-app
This is simple simulation of cinema service for reservation ticket, 
that supports registration, authentication and CRUD operation.
Program is developed in accordance with the REST concept using 
such technologies as Hibernate and Spring.

## Getting Started
* Install IntelliJ IdEA
* Clone project to your local machine
* Configure your Mysql database
  * Replace the values of the `YOUR_DRIVER`, `YOUR_DATABASE_URL`, `USER_NAME` and `PASSWORD` properties in db.properties
* Build the project using Maven: `mvn clean install`
* Deploy the WAR file to a servlet container such as Tomcat or other
* After deploying the project, you can use the web application using the link` http://localhost:8080/` and PostMan
* Default users:
  * For admin login: `admin@i.ua`, password: `admin123`
  * For user login: `user@gmail.com`, password: `user1234`

## Features
* Registration of users
* Authentication
* Authorization
  * ADMIN
    * Create and delete movies
    * Create and delete movie sessions
    * Create and delete cinema halls
    * View movies and their description
    * View movie sessions and in which cinema hall it will take place
  * USER
    * View movies and their description
    * View available movie sessions and in which cinema hall it will take place
    * View cinema halls
    * Choose available movie sessions and put your ticket in the cart
    * View user orders story

## Model structure
![structure.png](structure.png)

### Packages:
* **config** - stores Spring and App configuration
* **controller** - contains controllers for endpoints with different access depending on the role
* **dao** - data access layer (repository) with CRUD methods in the database
* **dto** - wrapper for model objects to unify the requests and responses in controllers
* **exception** - custom exception class for DAO's exceptions
* **lib** - contains email and password validators with its annotations
* **model** - contains models of entity for the database
* **service** - contains services that call repositories and perform business logic and mapper
* **util** - utility class used in a project to save DateTime pattern
* **resources** - contains properties for database

## Used technologies:
* Java v.17
* Maven v.3.1.1
* Spring v.5.3.20
* Spring Security v.5.6.10
* Hibernate v.5.6.14.Final
* MySql v.8.0.22
* Javax Servlets v.4.0.1
* Javax Annotations v.1.3
* Tomcat v.9.0.75

