<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Task Management Application README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        h1, h2, h3 {
            color: #333;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 5px;
            border-radius: 3px;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 3px;
            overflow-x: auto;
        }
    </style>
</head>
<body>

    <h1>Task Management Application</h1>

    <h2>Overview</h2>
    <p>The Task Management Application is a simple web-based tool built using JSP (JavaServer Pages) and MySQL to help users manage their notes or tasks efficiently. Users can create, edit, and delete tasks, making it a useful utility for organizing personal or professional activities.</p>

    <h2>Features</h2>
    <ul>
        <li><strong>User Authentication:</strong> Secure user sessions for managing personal tasks.</li>
        <li><strong>CRUD Operations:</strong> Create, Read, Update, and Delete tasks.</li>
        <li><strong>Responsive UI:</strong> Built with Bootstrap for a clean and responsive design.</li>
        <li><strong>Modal Forms:</strong> Use of modals for editing tasks to enhance user experience.</li>
    </ul>

    <h2>Technologies Used</h2>
    <ul>
        <li><strong>Frontend:</strong> HTML, CSS (Bootstrap)</li>
        <li><strong>Backend:</strong> JSP (JavaServer Pages)</li>
        <li><strong>Database:</strong> MySQL</li>
    </ul>

    <h2>Setup Instructions</h2>

    <h3>Prerequisites</h3>
    <ul>
        <li>Java Development Kit (JDK)</li>
        <li>Apache Tomcat or any other JSP server</li>
        <li>MySQL Server</li>
        <li>JDBC Driver for MySQL</li>
    </ul>

    <h3>Installation</h3>
    <ol>
        <li><strong>Clone the Repository:</strong>
            <pre><code>git clone &lt;repository-url&gt;
cd &lt;repository-directory&gt;</code></pre>
        </li>
        <li><strong>Set Up Database:</strong>
            <p>Create a new database named <code>enotedb</code>.</p>
            <p>Run the following SQL commands to create the necessary tables:</p>
            <pre><code>CREATE TABLE &lt;user_table_name&gt; (
    note_id INT AUTO_INCREMENT PRIMARY KEY,
    note_title VARCHAR(255) NOT NULL,
    note_description TEXT NOT NULL
);</code></pre>
            <p>Replace <code>&lt;user_table_name&gt;</code> with the sanitized email of the user (e.g., if the email is <code>user@example.com</code>, the table name would be <code>userexamplecomnotes</code>).</p>
        </li>
        <li><strong>Configure Database Connection:</strong>
            <p>Open the <code>task.jsp</code> file and update the following line with your database credentials:</p>
            <pre><code>Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/enotedb", "root", "your password");</code></pre>
        </li>
        <li><strong>Deploy the Application:</strong>
            <p>Deploy the application on your Tomcat server. Place the JSP files in the appropriate web application directory.</p>
        </li>
        <li><strong>Access the Application:</strong>
            <p>Open a web browser and navigate to <code>http://localhost:8080/&lt;your-application-name&gt;/task.jsp</code>.</p>
        </li>
    </ol>

    <h2>Usage</h2>
    <ol>
        <li><strong>Adding a Task:</strong> Fill in the "Note Name" and "Note Description" fields and click the "Add Note" button to create a new task.</li>
        <li><strong>Editing a Task:</strong> Click the "Edit" button next to a task. This will open a modal where you can update the task details. After editing, click the "Update Task" button to save changes.</li>
        <li><strong>Deleting a Task:</strong> Click the "Delete" button next to a task to remove it from the list.</li>
        <li><strong>Task List:</strong> All tasks will be displayed in a table format, showing the task name and description along with action buttons.</li>
    </ol>

    <h2>Contributing</h2>
    <p>Contributions to enhance the application are welcome! Please fork the repository and submit a pull request with your changes.</p>

    <h2>License</h2>
    <p>This project is licensed under the MIT License. See the <a href="LICENSE">LICENSE</a> file for details.</p>

</body>
</html>
