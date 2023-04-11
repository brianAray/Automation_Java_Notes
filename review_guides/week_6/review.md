# Week 6 Review
## Topics:
- System Testing
- Acceptance Testing
- Handlers
- Configuration
- HTTP
- Javalin
- JSON
- Query Parameters
- Path Parameters
- Request Body
- Context Object
- REST API
- Exception Handling

## Notes
### System Testing
- Type of testing that verifies that the entire system or application is functioning correctly
- Test Plan: detailed document outlining the objectives, scope, and approach of system testing
- Objectives:
    - Verify that the system meets its requirements
    - Ensure the system is usable and meets user needs
    - Verify that the system performs well under expected and unexpected conditions
- Test Basis
    - the set of documents and artifacts used to plan and execute system testing
- Test Object
    - the system or application being tested
- Defects
    - issues found during testing that need to be addressed
- Functional Tests
    - tests that verify that the system performs the functions it is designed to perform
- Non-Functional Tests
    - tests that verify that the system meets non-functional requirements, such as performance, scalability, and security
- Test Progress Report
    - report outlining the progress of system testing
- Test Summary Report
    - report outlining the results of system testing and any remaining issues
### Acceptance Testing
- Type of testing that verifies that the system meets user requirements and is ready for deployment
- Test Plan: detailed document outlining the objectives, scope, and approach of acceptance testing
- Objectives:
    - Verify that the system meets user requirements
    - Ensure the system is usable and meets user needs
    - Verify that the system performs well under expected and unexpected conditions
- Test Basis
    - the set of documents and artifacts used to plan and execute acceptance testing
- Test Object
    - the system or application being tested
- Defects
    - issues found during testing that need to be addressed
- Functional Tests
    - tests that verify that the system performs the functions it is designed to perform
- Non-Functional Tests
    - tests that verify that the system meets non-functional requirements, such as performance, scalability, and security
- Test Progress Report
    - report outlining the progress of acceptance testing
- Test Summary Report
    - report outlining the results of acceptance testing and any remaining issues
### Handlers
- Functions that are responsible for handling HTTP requests in web applications
- Can be used to define the behavior of a web application for a given URL and HTTP method
- Handlers can receive data from the request (e.g., query parameters, path parameters, request body) and return a response to the client
### HTTP
- Hypertext Transfer Protocol (HTTP) is the primary protocol used for communication on the web
- HTTP Verbs
    - the different types of requests that can be sent over HTTP, including GET, POST, PUT, DELETE, etc.
- HTTP Status Codes
    - numerical codes sent by servers to indicate the status of an HTTP request, such as 200 (OK), 404 (Not Found), 500 (Internal Server Error)
### Javalin
- Lightweight web framework for Java
- Designed to be simple and easy to use
- Includes features such as handlers, filters, and routes
- Can be used for developing RESTful web services
### JSON
- JavaScript Object Notation (JSON) is a lightweight data interchange format
- Easy for humans to read and write, and easy for machines to parse and generate
- Commonly used for transmitting data between a server and a web application
### Query Parameters, Path Parameters, Request Body, Context Object
- Different ways that data can be sent in an HTTP request
- Query Parameters
    - data passed in the URL of an HTTP request, typically used for filtering or searching data
- Path Parameters
    - data passed in the URL of an HTTP request that identifies a specific resource or action
- Request Body
    - data passed in the body of an HTTP request, typically used for creating or updating data
- Context Object
    - an object in Javalin that provides access to information about the current request, including query parameters, path parameters, and the request body
### REST API
- Representational State Transfer (REST) is an architectural style for designing web services
- RESTful web services use HTTP verbs and URIs to interact with resources
- Resources are identified by URIs and can be manipulated using HTTP verbs such as GET, POST, PUT, DELETE, etc.
- REST APIs provide a standardized way to interact with web services, making it easier to integrate different systems
### Exception Handling
- The process of handling errors or exceptions that occur during the execution of a program
- Proper exception handling can help prevent crashes and improve the overall reliability of a system or application
- In Java, exceptions are objects that are thrown when an error or unexpected situation occurs
- Exception handling can be done using try-catch blocks, which allow code to gracefully handle exceptions and recover from errors.