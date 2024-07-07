Contact Book Project
This Python script sets up a basic contact book application that interacts with a MySQL database using the pymysql library. Here's a detailed explanation of each part of the code:

1.Imports and Database Connection:
1.pymysql: Imports the library to connect and interact with MySQL databases.
2.time: Used for adding delays in the script.

Database Connection (conn):
1.Establishes a connection to the MySQL database running on localhost with credentials (user, password, db).

Functions:
1.intro(): Displays a simple introductory message.
2.add_new_record(): Prompts the user to input contact details (name, address, mobile, email), then inserts these details into the book table using an SQL INSERT statement.
3.search_record(name): Searches for a contact record by name in the book table and prints the details if found.
4.display_all_records(): Fetches and displays all records from the book table.
5.delete_record(name): Deletes a contact record by name from the book table.
6.modify_record(name): Allows the user to modify specific details (name, address, mobile) of a contact record identified by name.

Main Function (main()):

1.Displays a main menu with options for adding, searching, displaying, deleting, modifying records, or exiting.
2.Depending on the user's input, it calls corresponding functions (add_new_record(), search_record(name), etc.).
3.Handles input validation and ensures proper interaction with the database through try-except-finally blocks to manage exceptions and ensure resource cleanup (cur.close()).

Error Handling:

1.Uses try-except blocks to catch and handle errors that may occur during database operations (pymysql.Error).

Database Cursor (cur):
1.A cursor object (cur) is created from the connection (conn) to execute SQL statements (cur.execute()).

Closing Resources:
1.Ensures that database resources (cursor and connection) are properly closed in finally blocks to release resources and prevent memory leaks.
