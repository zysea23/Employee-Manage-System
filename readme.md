
# Employee Management System

This is a simple Employee Management System project built with a **React** frontend and a **Node.js + Express** backend, using **MySQL** for data storage. The project includes basic CRUD operations, allowing users to add, view, and manage employee information.

## Features

- Add new employee information (Name, Age, Country, Position, Wage)
- Display a list of all employees
- Clean and aesthetic UI with a macaron color theme

## Tech Stack

- **Frontend**: React, Axios
- **Backend**: Node.js, Express
- **Database**: MySQL
- **Styling**: CSS (with a macaron color scheme)

## Installation and Running the Project

### Prerequisites

- Node.js
- MySQL database

### Steps to Run Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/employee-management-system.git
   cd employee-management-system
   ```

2. **Setup MySQL Database**:
   - Open your MySQL client and create a new database:
     ```sql
     CREATE DATABASE employeeSystem;
     ```
   - Switch to the `employeeSystem` database and create the `employees` table:
     ```sql
     USE employeeSystem;

     CREATE TABLE employees (
         id INT AUTO_INCREMENT PRIMARY KEY,
         name VARCHAR(100),
         age INT,
         country VARCHAR(100),
         position VARCHAR(100),
         wage DECIMAL(10, 2)
     );
     ```

3. **Configure Backend**:
   - Navigate to the server folder and install the required packages:
     ```bash
     cd server
     npm install
     ```
   - Update the MySQL connection configuration in `server/index.js` with your MySQL username and password:
     ```javascript
     const db = mysql.createConnection({
         user: 'your_mysql_user',
         host: 'localhost',
         password: 'your_mysql_password',
         database: 'employeeSystem'
     });
     ```

4. **Run the Backend Server**:
   ```bash
   node server/index.js
   ```
   The server should start on port 3001.

5. **Setup and Run Frontend**:
   - Open a new terminal, navigate to the frontend folder, and install the necessary packages:
     ```bash
     cd ../client
     npm install
     ```
   - Start the React development server:
     ```bash
     npm start
     ```
   The frontend should open at `http://localhost:3000`.

## Usage

- **Add Employee**: Fill out the form and click "Add Employee" to add a new employee to the database.
- **Show Employees**: Click "Show Employees" to retrieve and display the list of all employees from the database.

## Screenshots

![Form and Employee List](./screenshots/form_and_list.png)

## License

This project is licensed under the MIT License.
