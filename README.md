Skip to content
shreyashakanurakar
php-project1
Repository navigation
Code
Issues
Pull requests
Actions
Projects
Wiki
Security and quality
Insights
Settings
php-project1
/php_web_application_readme.md
Go to file
t
T
shreyashakanurakar
shreyashakanurakar
Update php_web_application_readme.md
d9dc7cb
 · 
now
php-project1
/php_web_application_readme.md

Preview

Code

Blame
89 lines (60 loc) · 4.77 KB
## 📌 Project Overview & Introduction
# PHP Signup Application on AWS EC2

This repository contains a simple PHP Web Application for user registration hosted on an **AWS EC2 instance** using Apache Web Server and **MariaDB Database**.

---

## 📌 Project Overview & Introduction

The primary objective of this project is to build and deploy a dynamic web application on AWS cloud infrastructure. The application provides a user signup form where users can submit their details (Name, Email, Website, Comments, and Gender). Upon form submission:

1. The submitted data is processed via PHP (`submit.php`).
2. Data is stored securely inside a **MariaDB** database (`FCT` database, `users` table) running on the AWS EC2 instance.
3. A confirmation page displays the successfully submitted information to the user.

---

## 🏗️ Architectural Diagram

```
+-----------------------------------------------------------------------------------+
|                                 AWS Cloud Environment                             |
|                                                                                   |
|   +---------------------------------------------------------------------------+   |
|   |                       AWS EC2 Instance (Linux Server)                     |   |
|   |                                                                           |   |
|   |   +------------------+     HTTP Request     +-------------------------+   |   |
|   |   |                  |  ----------------->  |                         |   |   |
|   |   |  Apache Web      |                      |  PHP Script             |   |   |
|   |   |  Server          |  <-----------------  |  (submit.php)           |   |   |
|   |   +------------------+     HTML Response    +------------+------------+   |   |
|   |            ^                                             |                |   |
|   +------------|---------------------------------------------|----------------+   |
|                |                                             | Database       |
|   User Browser | HTTP POST                                   v Connection     |
|   (Client)     |                                    +-----------------+       |
|                +----------------------------------> | MariaDB         |       |
|                                                     | Database (FCT)  |       |
|                                                     +-----------------+       |
+-----------------------------------------------------------------------------------+
```

### Architecture Details:
* **Client / Browser:** Accesses the web application over HTTP via the EC2 instance's IP address (`100.31.56.13`).
* **Apache Web Server:** Serves the HTML frontend (`signup.html`) and executes server-side PHP scripts.
* **PHP Application (`submit.php`):** Processes incoming user inputs and inserts them into the database.
* **MariaDB Database:** Manages relational data storage within the database named `FCT`.

---

## 📸 Input, Output & Database Screenshots

### 1. User Input Form (`signup.html`)
The user fills in fields such as Name, Email, Website, Comment, and Gender on the input form:

![Signup Form Input](./Screenshot%202026-10-08%20180644.png)<img width="1007" height="816" alt="Screenshot 2026-10-08 180644" src="https://github.com/user-attachments/assets/9b7d7023-a183-4a14-bd03-b4a720acc2a7" />


### 2. Form Submission Output Page (`submit.php`)
Upon submission, the PHP backend displays a success message ("New record created successfully!") along with the submitted data:


![Form Submission Output](./Screenshot%202026-10-08%20180541.png)<img width="1905" height="846" alt="Screenshot 2026-10-08 180541" src="https://github.com/user-attachments/assets/ec2206f9-18e9-43fc-ae1a-30adec389762" /> <img width="1490" height="983" alt="Screenshot 2026-10-08 181138" src="https://github.com/user-attachments/assets/6b09eb81-ff38-420c-b006-84856e46e5ff" />



### 3. Database Verification (MariaDB SQL Terminal)
Data successfully inserted into the `users` table inside MariaDB on the EC2 instance:
![Database Verification](./Screenshot%202026-10-08%20181138.png)

---

## 🛠️ Technology Stack

* **Cloud Infrastructure:** AWS EC2 (Amazon Elastic Compute Cloud)
* **Frontend:** HTML5, CSS
* **Backend:** PHP 8.x
* **Database:** MariaDB / MySQL Server
* **Web Server:** Apache HTTP Server (`httpd`)
* **Operating System:** Amazon Linux / CentOS

---



---

## 🎯 Conclusion

This project successfully demonstrates the deployment of a classic LAMP (Linux, Apache, MariaDB, PHP) stack on an AWS EC2 instance. By hosting the application on Amazon Web Services, it benefits from high availability, scalability, and secure cloud infrastructure. The application effectively handles client-side data submission, processes it through server-side PHP scripts, and permanently persists the records in a cloud-hosted MariaDB database.
 
