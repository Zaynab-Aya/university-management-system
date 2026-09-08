University Management System

A desktop-based University Management and Registration System developed using Java, JavaFX, FXML, CSS, and Microsoft SQL Server.

Project Overview

The University Management System is a desktop application designed to manage and simplify academic processes within a university environment.

The system provides different features and access levels for Students, Instructors, and Administrators, with a centralized database for managing academic and user information.

The project is currently developed and run locally as a JavaFX desktop application through VS Code and is not deployed as an online/public system.

User Roles

Student

Students can:

* View and manage their profile
* Register for courses
* View registered courses
* Check course prerequisites
* Track registered credits
* View grades and grade components
* View their transcript
* Follow their degree progress
* View their study plan
* Check course eligibility and status
* View their timetable
* Receive notifications
* View the academic calendar
* Use the AI Assistant

Instructor

Instructors can:

* View their courses
* View registered students
* Manage student grades
* Enter grade components
* Save grades as drafts
* Submit and lock grades
* View course-related information

Administrator

Administrators can:

* Manage users and university data
* Manage courses and academic information
* Manage academic semesters
* Manage the academic calendar
* Monitor registrations
* View administrative dashboards
* View program distribution statistics
* View course pass-rate statistics
* Manage system information

Main Features

Course Registration

The registration module allows students to register for courses while applying academic rules such as:

* Prerequisite validation
* Schedule conflict detection
* Course availability
* Credit limits
* Registration period rules
* Add/Drop restrictions

Study Plan

The Study Plan helps students track their academic progress by displaying:

* Program information
* Courses organized by semester
* Course credits
* Prerequisites
* Course status
* Passed courses
* Courses in progress
* Failed courses
* Eligible courses
* Locked courses
* Remaining academic requirements

The system also considers semester credit limits when planning courses.

Grades & Transcript

The system provides grade management for instructors and students.

It supports:

* Coursework marks
* Midterm marks
* Lab marks
* Final marks
* Total marks
* Letter grades
* Grade points
* Grade publication controls
* Draft and submission workflows
* Student transcript generation

Timetable

Students can view their registered course schedules in an organized timetable while the system checks for schedule conflicts during registration.

Notifications

The system provides notifications for relevant academic and registration-related events.

Academic Calendar

The Academic Calendar allows administrators to manage important academic dates, including:

* Semester dates
* Registration periods
* Add/Drop deadlines
* Withdrawal deadlines
* Examination periods
* Final grade periods
* Holidays

Students can view the relevant academic calendar information from the system.

AI Assistant

The system includes an integrated AI Assistant designed to help users interact with the university system.

The assistant can support:

* University-related questions
* Student academic information
* General questions
* Text-based interaction
* Voice input
* Image-based interaction
* Document-based interaction

For university-related questions, the assistant works through the application’s services and data-access layers to retrieve relevant information from the system database rather than executing arbitrary SQL queries.

General questions can be handled through the Google Gemini API.

Admin Dashboard

The administrator dashboard provides an overview of university data through visual statistics and charts.

Examples include:

* Program distribution
* Course pass-rate statistics
* Registration-related information
* Academic data summaries

System Architecture

The application follows a layered architecture:

JavaFX / FXML
       ↓
Controllers
       ↓
Services
       ↓
DAO
       ↓
SQL Server Database

The AI Assistant is integrated into the application through the service layer:

JavaFX AI Assistant
        ↓
AI Assistant Service
        ↓
Authentication / Role / Intent
        ↓
University Services / DAOs
        ↓
SQL Server Database

General questions can be routed to the Gemini API when they are not related to university system data.

Technologies Used

* Java 21
* JavaFX
* FXML
* CSS
* Maven
* Microsoft SQL Server
* JDBC
* HikariCP
* BCrypt
* Google Gemini API
* JUnit
* Git & GitHub

Project Structure

src/
├── main/
│   ├── java/
│   │   └── com/university/
│   │       ├── controller/
│   │       ├── service/
│   │       ├── dao/
│   │       ├── model/
│   │       └── database/
│   │
│   └── resources/
│       ├── fxml/
│       ├── css/
│       └── images/
│
└── test/

Running the Project

Requirements

* Java 21
* Maven
* Microsoft SQL Server
* VS Code or another Java development environment

Run the Application

After configuring the database and required environment variables, the application can be started locally using:

mvn javafx:run

Project Status

This project was developed as part of a software engineering training experience.

The system is currently a local JavaFX desktop application and is not deployed as an online service.

Authors

Zaynab Matar & Aya Aboyehya
