 
 # Portfolio

![port](https://github.com/user-attachments/assets/85420238-d454-4ef7-b39e-f7a1ee5d9efb)

<h2>Installation</h2>

- **Node**: Node.js to run JavaScript and use npm start to launch your application. [official website](https://nodejs.org/en)
- **Linux**: use `npm start` to run applications. [official website](https://apps.microsoft.com/detail/9n9tngvndl3q?rtc=1&hl=en-au&gl=AU)


- **Clone the Repository**:
   ```bash
   git https://github.com/ChungmanPARK12/DataStructure-and-Algorithm.git
   cd <StudentEnrolmentSystem>
  

# Getting started
- **Running the server**
`node ace serve --wath`
- ![started](https://github.com/user-attachments/assets/31c1bf47-3c10-4252-956b-7fe64884397d)

# Architechture
<h2>StudentController.ts</h2>

Manages student records with methods to create (`store`), read(`show`), update (`update`), delete (`destroy`), and validate inputs, ensuring robust and secure CRUD operations.

* ### Example of Code [Click here](https://github.com/ChungmanPARK12/API/tree/09a744dac35c59aaa0aa071d3c258a9ffa979694/src/StudentController)

<h2>Students.ts</h2>

Represents student records, with properties like `StudentID`, `GivenName`, `LastName`, and `EmailAddress`, enabling database interactions and validation for CRUD operations.

* ### Example of Code [Click here](https://github.com/ChungmanPARK12/API/tree/09a744dac35c59aaa0aa071d3c258a9ffa979694/src/StudentsDefinition)

<h2>Routes.ts</h2>

Maps HTTP methods to `StudentsController` actions, defining `endpoints` for creating, reading, updating, and deleting student records, ensuring structured API interaction.

* ### Example of Code [Click here](https://github.com/ChungmanPARK12/API/tree/09a744dac35c59aaa0aa071d3c258a9ffa979694/src/Routes.ts)

# Postman(CRUD)

<h2>API Endpoint</h2>

**You can interact with the Student Management API using the following base URL**:

 ```http://127.0.0.1:3333/api/v1/students```
 
<h2>GET Student</h2>
 
Use the `GET` method to retrieve student details by ID or All of the lists.

* ### Result in Postman [Click here](https://github.com/ChungmanPARK12/API/tree/1f24ce91800993c18cc13a1f5f84533a348935ae/src/GetAllStudents)

<h2>POST Student</h2>
 
Use the `Update` method to create a new student record by sending student details in the request body.

* ### Result in Postman [Click here](https://github.com/ChungmanPARK12/API/tree/1f24ce91800993c18cc13a1f5f84533a348935ae/src/ResultOfPost)

<h2>DELETE Student</h2>
 
Use the `DELETE` method to remove a student record by providing specific criteria in the request body.

* ### Result in Postman [Click here](https://github.com/ChungmanPARK12/API/tree/b8f2241e0984719436e545670f87dc630cbb0832/src/ResultOfDelete)

<h2>UPDATE Student</h2>

Use the `PUT` method to update an existing student record by its ID, replacing all fields with new data.


* ### Result in Postman [Click here](https://github.com/ChungmanPARK12/API/tree/b8f2241e0984719436e545670f87dc630cbb0832/src/ResultOfPut)

Use the `PATCH` method to update specific fields of an existing student record without replacing the entire record.

* ### Result in Postman [Click here](https://github.com/ChungmanPARK12/API/tree/eea5c2d2e1281bcbcc4b0d3cca129ea43d80e15b/src/ResultOfPatch)

## Summary

The Student Management API allows for efficient management of student records through CRUD operations. Users can create, read, update, and delete student data using HTTP methods. The API ensures data integrity with validation and secure endpoints. Postman is used for testing and documentation, providing a reliable interface for interacting with the API.

## Thank you
Thank you for visiting my github :)

 
