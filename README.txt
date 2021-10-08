CRUD Application - SPRING BOOT, SPRING SECURITY AND THYMELEAF
==========================================
An Employee Directory application. This version makes use of JDBC Authentication with encrypted passwords.

This Spring Boot project will make use of two different datasources
1. Main datasource for the app. This is for accessing the "employee" database
2. Another datasource for the application security. This is for accessing the security info database.
3. The database configs are in the file: application.properties


DISPLAY CONTENT BASED ON USER ROLE
==================================

In the application, the content is displayed based on the user role.

- Employee role: users in this role will only be allowed to list employees.
- Manager role: users in this role will be allowed to list, add and update employees.
- Admin role: users in this role will be allowed to list, add, update and delete employees. 

The role based links are also made to  hide or display . For example, if the user has only the "EMPLOYEE" role, then the user gets only the links available for "EMPLOYEE" role.
Links for "MANAGER" and "ADMIN" role should not be displayed for the "EMPLOYEE".

TEST THE APPLICATION
====================
1. Before running the application, make sure the database tables are set up (via SQL files).  Also, be sure to update application.properties for database connection (url, userid, pass)
 
2. Run the Spring Boot application: ThymeleafdemoApplication.java

3. Open a web browser for the app: http://localhost:8080

4. Log in using one of the accounts

+---------+----------+-----------------------------+
| user id | password |            roles            |
+---------+----------+-----------------------------+
| john    | fun123   | ROLE_EMPLOYEE               |
| mary    | fun123   | ROLE_EMPLOYEE, ROLE_MANAGER |
| susan   | fun123   | ROLE_EMPLOYEE, ROLE_ADMIN   |
+---------+----------+-----------------------------+

4. Confirm that you can login and access data based on the roles.

SQL Table
=========
There is a table needed in database for this application. Below is the sample table that was used while building this project.
The SQL scripts have been added in this project. You can either use that or create a custom table.

+---------+----------+-----------------------------+
| user id | password |            roles            |
+---------+----------+-----------------------------+
| john    | fun123   | ROLE_EMPLOYEE               |
| mary    | fun123   | ROLE_EMPLOYEE, ROLE_MANAGER |
| susan   | fun123   | ROLE_EMPLOYEE, ROLE_ADMIN   |
+---------+----------+-----------------------------+
 					
Screenshots: 

![Test Image 1](https://github.com/Maninderjeet31/CRUD-Applications---Employees/blob/main/java%20crud%20project/1.%20Login.png?raw=true) 


Reference: https://www.udemy.com/course/spring-hibernate-tutorial/
