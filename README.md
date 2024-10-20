Task Management Application
Overview
The Task Management Application is a simple web-based tool built using JSP (JavaServer Pages) and MySQL to help users manage their notes or tasks efficiently. Users can create, edit, and delete tasks, making it a useful utility for organizing personal or professional activities.

Features
User Authentication: Secure user sessions for managing personal tasks.
CRUD Operations: Create, Read, Update, and Delete tasks.
Responsive UI: Built with Bootstrap for a clean and responsive design.
Modal Forms: Use of modals for editing tasks to enhance user experience.
Technologies Used
Frontend: HTML, CSS (Bootstrap)
Backend: JSP (JavaServer Pages)
Database: MySQL
Setup Instructions
Prerequisites
Java Development Kit (JDK)
Apache Tomcat or any other JSP server
MySQL Server
JDBC Driver for MySQL
Installation
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd <repository-directory>
Set Up Database:

Create a new database named enotedb.
Run the following SQL commands to create the necessary tables:
sql
Copy code
CREATE TABLE <user_table_name> (
    note_id INT AUTO_INCREMENT PRIMARY KEY,
    note_title VARCHAR(255) NOT NULL,
    note_description TEXT NOT NULL
);
Replace <user_table_name> with the sanitized email of the user (for example, if the email is user@example.com, the table name would be userexamplecomnotes).

Configure Database Connection:

Open the task.jsp file and update the following line with your database credentials:
java
Copy code
Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/enotedb", "root", "your password");
Deploy the Application:

Deploy the application on your Tomcat server. Place the JSP files in the appropriate web application directory.
Access the Application:

Open a web browser and navigate to http://localhost:8080/<your-application-name>/task.jsp.
Usage
Adding a Task:

Fill in the "Note Name" and "Note Description" fields and click the "Add Note" button to create a new task.
Editing a Task:

Click the "Edit" button next to a task. This will open a modal where you can update the task details. After editing, click the "Update Task" button to save changes.
Deleting a Task:

Click the "Delete" button next to a task to remove it from the list.
Task List:

All tasks will be displayed in a table format, showing the task name and description along with action buttons.
