
# Registration Page

Registration_page allows users to register their details for vaccination. The interface includes fields for personal information, such as name, age, and contact details, as well as medical information like blood pressure and body temperature. It connects to a MySQL database to store the registration details.




## Features
- User Registration: Users can enter their personal and medical information to register for vaccination.
- Data Validation: Ensures all required fields are filled and valid before submission.
- Database Connectivity: Connects to a MySQL database to insert registration details.
- Image Display: Shows an image on the registration screen.
- Navigation: Includes a back button to navigate to the main menu.
## Prerequisites
- Java Development Kit (JDK): Ensure you have JDK installed on your system.
- MySQL Database: A MySQL database instance running with the vaccination_database_new database and a registration_data table.
- MySQL Connector for Java: Ensure you have the MySQL Connector - - JAR file added to your project.
## Setup and Installation
1. Clone the Repository :
```
git clone https://github.com/java-developer-payal/vaccine-management-system-gui.git
```
2. Configure Database :

- Create a MySQL database named vaccination_database_new.
- Create a registration_data table with the required columns.
```
CREATE DATABASE vaccination_database_new;
USE vaccination_database_new;
CREATE TABLE registration_data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    aadhar VARCHAR(50) NOT NULL,
    gender VARCHAR(10) NOT NULL,
    age INT NOT NULL,
    profession VARCHAR(50),
    temp FLOAT,
    address VARCHAR(255),
    vaccineName VARCHAR(50),
    bloodPressure FLOAT,
    contactNumber VARCHAR(15)
);
```
3. Update Database Credentials :

- Open the Registration_page.java file.
- Update the following line with your MySQL username and password:
```
Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/vaccination_database_new", "root", "your_password");
```
4. Run the Application :

- Compile and run the VaccineGui class.
```
javac VaccineGui.java
java VaccineGui
```
## Usage
1. Registration :

- Enter your personal and medical information in the provided fields.
- Click the "Submit" button to save your details to the database.
- A success message will be displayed upon successful data insertion.
2. Navigate Back :

- Click the "Back" button to return to the main menu.