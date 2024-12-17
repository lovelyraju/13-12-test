### **Assignment Title: Build a Student Management System**

**Course Name**: Web Application Development  
**Points**: 100  
**Due Date**: 28-12-2024  
**Submission Type**: Online (GitHub repository link)  
**Available From**: 14-12-2024  


---

### **Objective**
This assignment will guide you in building a **Student Management System** web application to practice and apply your knowledge of **HTML**, **CSS**, **JavaScript**, **Java**, and **MySQL**. You will develop a system with a responsive frontend, functional backend APIs, and database integration.

By the end of this assignment, you will have a deeper understanding of how to structure, develop, and deploy a complete web application.

---

### **Deliverables**
- **Login Page**: Allows the admin/teacher to log in.
- **Dashboard**: Displays a list of students with options to add, edit, delete, and search student records.
- **Backend**: APIs for user authentication and CRUD operations for student records.
- **Database**: A MySQL database for storing user and student data.

---

### **Instructions**

#### **1. Project Setup (10 Points)**
1. Create a GitHub repository named `StudentManagementSystem`.
2. Set up the following folder structure:
   ```
   /StudentManagementSystem
   ├── frontend
   │   ├── index.html
   │   ├── dashboard.html
   │   └── styles.css
   ├── backend
   │   ├── src
   │   │   ├── LoginServlet.java
   │   │   ├── StudentServlet.java
   │   │   └── DatabaseUtil.java
   │   └── web.xml
   └── database
       └── schema.sql
   ```

---

#### **2. Database Design (15 Points)**
1. Create a MySQL database named `student_management`.
2. Add the following tables:
   - **users**: Stores admin/teacher login credentials.
     ```sql
     CREATE TABLE users (
         id INT AUTO_INCREMENT PRIMARY KEY,
         username VARCHAR(50) NOT NULL,
         password VARCHAR(255) NOT NULL
     );
     ```
   - **students**: Stores student details.
     ```sql
     CREATE TABLE students (
         id INT AUTO_INCREMENT PRIMARY KEY,
         name VARCHAR(100) NOT NULL,
         roll_number INT UNIQUE NOT NULL,
         class VARCHAR(20),
         email VARCHAR(100)
     );
     ```
3. Insert sample data into the `users` table for testing:
   ```sql
   INSERT INTO users (username, password) VALUES ('admin', 'password123');
   ```

---

#### **3. Frontend Development (25 Points)**
1. **Login Page (5 Points)**:
   - Create a simple `index.html` page with fields for username and password.
   - Add a "Login" button that connects to the backend.

2. **Dashboard (10 Points)**:
   - Create a `dashboard.html` page that displays student data in a table.
   - Include an "Add Student" button and a form for adding/editing students.

3. **Styling (10 Points)**:
   - Use **CSS** to style the application with responsive design and a clean layout.

---

#### **4. Backend Development (30 Points)**
1. **Login API**:
   - Implement a `LoginServlet` to validate user credentials.

2. **Student Management API**:
   - Implement a `StudentServlet` for CRUD operations:
     - **GET**: Fetch all student records.
     - **POST**: Add a new student.
     - **PUT**: Update an existing student.
     - **DELETE**: Remove a student.

3. **Database Utility**:
   - Create a `DatabaseUtil` class to handle database queries using JDBC.

---

#### **5. Integration (15 Points)**
1. Use **AJAX/Fetch API** to connect the frontend to the backend APIs.
2. Validate login and redirect to the dashboard on success.
3. Display and update student data dynamically on the dashboard.

---

#### **6. Testing & Deployment (5 Points)**
1. Test the application locally on your system.
2. Document the steps to run your project in a `README.md` file in your repository.

---

### **Grading Rubric**

| **Criteria**                | **Points** | **Description**                                                                                 |
|-----------------------------|------------|-------------------------------------------------------------------------------------------------|
| **Project Setup**           | 10         | Correct folder structure, GitHub repository, and initial configuration.                         |
| **Database Design**         | 15         | Correct table creation, sample data, and database schema implementation.                        |
| **Frontend Development**    | 25         | Functional login page, dashboard, and responsive styling.                                       |
| **Backend Development**     | 30         | Functional APIs for login and student management using Java and MySQL.                          |
| **Integration**             | 15         | Successful frontend-backend integration with real-time updates via AJAX/Fetch API.              |
| **Testing & Deployment**    | 5          | Successfully running the application locally and documenting steps in a `README.md` file.       |

---

### **Submission Guidelines**
1. Submit the GitHub repository link containing:
   - Frontend and backend code.
   - MySQL schema file (`schema.sql`).
   - `README.md` file with clear setup and execution instructions.
2. Ensure that all files are well-organized and commented.

---

### **Learning Outcomes**
By completing this assignment, you will:
1. Understand how to design and implement a complete web application.
2. Learn to integrate frontend and backend components.
3. Gain hands-on experience with database operations and API development.
4. Practice organizing and deploying a full-stack application.

---

**Good luck! If you have any questions, Ask in our discussion.**

