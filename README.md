# Employee Details Management System

## Overview
This project is a **web-based Employee Details Management System** that allows users to enter and manage employee information. It includes a **frontend (HTML form), backend (Maven-based Java application), and deployment pipeline (Jenkins for CI/CD).**

## Features
- Employee details form for data entry.
- Maven-based Java web application.
- Automated build and deployment using Jenkins.
- Deployment to Tomcat Server on AWS.

## Technologies Used
- **Frontend:** HTML, Forms
- **Backend:** Java, Maven
- **Build Tool:** Apache Maven
- **CI/CD:** Jenkins
- **Deployment:** Tomcat Server, AWS

## Project Structure
### 1. **Frontend (index.html)**
- A simple HTML form to collect employee details:
  - First Name, Last Name
  - Father's & Mother's Name
  - Gender
  - Employee ID, Designation
  - Phone Number, Address
  - Submit Button

### 2. **Backend (Maven-based Java Web Application)**
- The project is structured as a **Maven Web Application** (`pom.xml`).
- Uses **Maven War Plugin** to package the project as a `.war` file for deployment.
- Includes dependencies such as JUnit for testing.

### 3. **Jenkins Pipeline (Jenkinsfile)**
- **Automates build, test, and deployment process.**
- **Stages:**
  - Clone the GitHub repository.
  - Build the project using Maven.
  - Deploy the WAR file to a **Tomcat server** running on AWS.
- **Triggers:** Uses a cron job to execute the pipeline every 10 minutes.

## Installation & Deployment
### Prerequisites
- Git
- Maven
- Jenkins
- Tomcat Server

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Tejasrikrishnamraju/employee-details.git
   ```
2. Navigate to the project directory:
   ```bash
   cd employee-details
   ```
3. Build the Maven project:
   ```bash
   mvn clean install
   ```
4. Deploy the generated WAR file to Tomcat:
   ```bash
   cp target/web-application-war-file.war /path/to/tomcat/webapps/
   ```
5. Start Tomcat Server:
   ```bash
   ./catalina.sh run
   ```

## Future Enhancements
- Implement database integration for persistent storage.
- Add authentication and role-based access control.
- Improve UI/UX with modern frontend frameworks.
- Implement RESTful APIs for better scalability.
