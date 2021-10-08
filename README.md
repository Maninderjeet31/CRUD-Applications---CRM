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

<img width="639" alt="Screenshot 2021-10-08 at 4 10 35 PM" src="https://user-images.githubusercontent.com/38119046/136619457-119de6d5-d2bc-4637-bebc-e2d8c99dc6d8.png">

5. Confirm that you can login and access data based on the roles.

SQL Table
=========
There is a table needed in database for this application. Below is the sample table that was used while building this project.
The SQL scripts have been added in this project. You can either use that or create a custom table.

<img width="639" alt="Screenshot 2021-10-08 at 4 11 23 PM" src="https://user-images.githubusercontent.com/38119046/136619533-75146a72-b15f-4128-b4d3-0724403cd7be.png">
 					
Screenshots: 

1. Login screen:
<img width="1790" alt="first" src="https://user-images.githubusercontent.com/38119046/136618582-59b8f8d3-b6b9-4400-b551-5353767f4ac3.png">

2.Employee page
<img width="1790" alt="second" src="https://user-images.githubusercontent.com/38119046/136618655-6e86431a-9061-4bb3-be1f-4c3fd3e81185.png">

3.Employee Search function
<img width="1790" alt="third" src="https://user-images.githubusercontent.com/38119046/136618717-38a21604-ad2f-467f-a811-d982527cfbd4.png">

4.User-role based access authorization
<img width="1790" alt="fourth" src="https://user-images.githubusercontent.com/38119046/136618733-e31aa2da-25a8-49ed-a47b-9078d45ab91e.png">

5.Manager page
<img width="1790" alt="fifth" src="https://user-images.githubusercontent.com/38119046/136618763-26f596e3-0a76-46c4-b9ca-a460b048f859.png">

6.Manager page: Update an existing employee
<img width="1790" alt="sixth" src="https://user-images.githubusercontent.com/38119046/136618813-ef0a9545-d5ec-4579-a0ef-ff36076ea943.png">

7.Manager page: Create a new employee
<img width="1790" alt="seventh" src="https://user-images.githubusercontent.com/38119046/136618825-f5823c63-64ac-4399-8dc5-5e2b097f8b49.png">

8.Admin page
<img width="1790" alt="eighth" src="https://user-images.githubusercontent.com/38119046/136618839-ffde7dea-0f22-4432-9daf-968af87b7d93.png">

9.Admin page: delete employee link
<img width="1790" alt="nineth" src="https://user-images.githubusercontent.com/38119046/136618860-257d256c-064f-4c95-8107-678b4d298fe6.png">

10.Logout screen
<img width="1790" alt="tenth" src="https://user-images.githubusercontent.com/38119046/136618878-df9ea7d6-3e3d-4406-90e8-d755978fd4b9.png">

Reference: https://www.udemy.com/course/spring-hibernate-tutorial/
