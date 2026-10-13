PHP Signup Form Project on AWS
1. Introduction

The PHP Signup Form Project is a web-based application developed using HTML, PHP, and MariaDB. It allows users to enter their personal information through a signup form and submit the details to a backend PHP script.

The submitted information is stored in a MariaDB database. After successful submission, the application displays a confirmation message along with the submitted information.

This project is deployed on an AWS EC2 instance and demonstrates the integration of a web server, PHP application, and relational database.

2. Project Objectives
To develop a user-friendly signup form using HTML.
To process form data using PHP.
To connect PHP with a MariaDB database.
To store user information in a database table.
To display a successful submission message.
To understand web application deployment on AWS EC2.
3. Technologies Used
Technology	Purpose
HTML	Creates the signup form
PHP	Processes submitted form data
MariaDB	Stores user information
Apache HTTP Server	Hosts the web application
AWS EC2	Provides the cloud server
Linux	Operating system for the EC2 instance
Google Chrome	Accesses the web application
4. Project Architecture Diagram

The following diagram illustrates the architecture and data flow of the application.

flowchart TD
    A[User / Web Browser]
    B[AWS EC2 Instance]
    C[Apache Web Server]
    D[HTML Signup Form]
    E[PHP Submit Script]
    F[MariaDB Database]
    G[Success Result Page]

    A -->|HTTP Request| B
    B --> C
    C --> D
    D -->|Form Submission| E
    E -->|Insert User Data| F
    F -->|Successful Insert| E
    E --> G
    G -->|Display Confirmation| A

Architecture Explanation
User: Enters name, email, website, comment, and gender in the signup form.
AWS EC2: Hosts the application on a Linux-based cloud instance.
Apache Web Server: Serves the HTML page and executes PHP through the configured PHP integration.
PHP Script: Receives and processes the submitted form values.
MariaDB Database: Stores the submitted details in the users table of the FCT database.
Result Page: Displays a success message and the submitted information.
5. Input Screenshot — Signup Form

The signup form accepts the following information:

Name
Email
Website
Comment
Gender

The user enters the details and clicks the Submit button to send the form data to the PHP backend.

!PHP Signup Form Input Screenshot

Figure 1: Signup form displayed in the web browser.

6. Output Screenshot — Successful Form Submission

After submitting the form, the submit.php script processes the information and displays a confirmation message.

The output confirms that a new record was created successfully. It also displays the submitted name, email, website, comment, and gender.

!PHP Signup Form Output Screenshot

Figure 2: Successful form submission and displayed user information.

7. Database Verification Screenshot

The MariaDB database is used to store the signup information.

The database was accessed through the MariaDB command-line interface, and the following SQL commands were executed:

USE FCT;

SELECT * FROM users;


The query output confirms that the submitted record exists in the users table.

The table contains the following columns:

id
name
email
website
comment
gender

!MariaDB Database Verification Screenshot

Figure 3: Verification of the submitted record in the MariaDB database.

8. Application Workflow
The user opens the signup page in a web browser.
The user enters the required information.
The form submits the data to submit.php.
PHP processes the submitted values.
PHP connects to MariaDB and inserts the data into the users table.
The application displays a success message.
The database record is verified using an SQL query.
9. AWS Deployment Details

The application is hosted on an AWS EC2 instance running Linux.

The deployment involves the following components:

An EC2 instance to run the web application.
Apache to serve web requests.
PHP to process form submissions.
MariaDB to store submitted records.
A security group configured to allow the required network traffic.

The application is accessed through the EC2 instance's configured IP address or domain name.

Security note: For production deployments, use HTTPS, validate and sanitize all form inputs, use prepared SQL statements, protect database credentials, and restrict database access. Avoid exposing MariaDB's port publicly.

10. Conclusion

The PHP Signup Form Project successfully demonstrates the development and deployment of a dynamic web application using HTML, PHP, and MariaDB on AWS EC2.

The application accepts user information, processes form submissions, stores the data in a database, and displays a successful submission message. The database query further verifies that the submitted record has been stored.

This project provides practical experience with cloud computing, Linux server administration, web server configuration, PHP programming, and database connectivity.

It also establishes a foundation for developing more advanced web applications on AWS.

Project Status: Successfully tested with form submission and database record verification.

Repository: PHP Signup Form Project on AWS EC2
