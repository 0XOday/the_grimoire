A web application is likely to use SQL to read and write information from a database. SQL statements perform operations such as selecting data, inserting data and deleting data and updating data. In SQL injection attack the threat actor modifies one or more of these four basic functions by adding code to some input accepted by the app, causing it to execute the attackers own set of SQL queries or parameters. if succesful, this could allow the attack to extract or insert information into the database or execute arbitrary code on the remote system using the same privilege's as the database application.

For example, consider a web from that is supposed to take a name as input. if the user enters "Bob", the application runs the following query:

`SELECT * FROM tbl_user WHERE username = 'Bob'`

if a threat actor enters the string `' or 1=1--` and this input is not sanitized, the following malicious query will be executed:

`SELECT * FROM tbl_user WHERE username = '' or 1=1--#`

The logical statement 1=1 is always true, and --# string turns the rest of the statement into a comment, making it more likely that the web application will parse this modified version and dump a list of all users.