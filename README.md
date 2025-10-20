# IanHelt.github.io

**CS-499 Computer Science Capstone**

**Professional Self-Assessment**

Throughout my Computer Science program, I have developed the technical skills and professional discipline needed to design secure, efficient, and user-focused software. Building my ePortfolio allowed me to bring together what I’ve learned in programming, database design, and system security to showcase projects that reflect my growth and expertise. My capstone project, the Inventory Tracker App, as simple as it is, demonstrates these abilities through its clean interface, database integration, and secure user authentication features.

Developing the Inventory Tracker strengthened my understanding of data structures and algorithms, software engineering principles, and database management. Migrating from SQLite to MySQL taught me to create scalable, centralized systems while maintaining data integrity and security. Redeveloping the UI to take advantage of sorting algorithms and parse different users shows my experience in engineering and algorithms.

Security has become one of my strongest professional priorities. My coursework in secure coding and DevSecOps reinforced best practices such as validating input, protecting data in storage and in transit, and managing system privileges responsibly. I strive to follow these principles in all my current and future projects.

Together, the artifacts in my ePortfolio demonstrate a cohesive set of skills in programming, system design, database development, and security. They reflect my ability to create software that is not only functional but also dependable and secure. This work represents my readiness to contribute to the computer science field with a focus on quality, integrity, and professional excellence.

**Artifact:**

Inventory Tracker

Android app with user login for managing inventory with add/edit/delete functionality, recently migrated to MySQL.

Tech: Java, MySQL

**Enhancement Plan and Code Review**

[Initial Code Review](https://youtu.be/TPt_CZDBrgQ)

For the capstone of my Computer Science Degree, I chose to focus on enhancing this Inventory Tracker application. Originally, the app used SQLite databases to track items entered by users. There was registration and login functionality, but it didn't do much, as every user was able to view the entirety of the item database. The databases being SQLite also meant that they were tied to the device running the app.

**Enhancement One: Software Engineering**

For this enhancement, I chose to change my inventory app so that each user saw only their own unique inventories. I was able to accomplish this by first writing a backend API for the application then refactoring the application to utilize MySQL. After doing so, I was able to associate each item with its user, and change the user interface to display only items associated with the actively logged in user. The screenshots below display inventories for two seperate users.

**Enhancement Two: Algorithms and Data Structures**

For this enhancement, I chose to add a sorting algorithm to my app in order to allow users to organize their homepage in a way that best suits them. Originally, the app displayed items in the order in which they had been added to the database. Now, the application sorts items alphabetically by default, and allows users to select sorting by type or quantity from the spinner drop down below the “Add Item” button. The item cards are changed immediately upon the option being selected. The sorting method is also saved during the current session, so jumping between screens will not reset the desired sorting method.

**Enahncement Three: Databases**

For this enhancement, I chose to migrate my inventory application from a device-based SQLite database to a server-based MySQL database. Doing so allows data to be stored, managed, and accessed independently from the device running the application. I started by creating a MySQL database in docker and populating it with a “users” and “items” table. I made sure to link each item to their respective user using a foreign key, which was essential to the functionalities of enhancements one and two. Next, I tried to figure out a way for the app to communicate with the database without building an entire backend API, but eventually I realized it made much more sense to just build the API. Once I got the API connected to the database, I learned how to use the retrofit library to connect my app’s codebase to the backend API, then refactored my code to get rid of all references to the original SQLite databases and reroute them to the backend API. The application now requires both the backend API and the MySQL server to be running to function properly, but the migration was overall successful.

**Overall, these enhancements transformed the app into a more secure, flexible, and professional inventory management tool that demonstrates strong software engineering and database integration principles.**
