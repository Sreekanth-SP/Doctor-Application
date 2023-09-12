
# Doctor-Application
>The Doctor-Patient project is a web application built using Spring Boot that facilitates the interaction between doctors and patients. The main goal of the project is to provide a platform where patients can schedule appointments with doctors, and doctors can manage their appointments efficiently. The application also includes a secure authentication system to ensure data privacy and security.
---
## Frameworks and Languages
This project is developed using the following frameworks and languages:

* **Spring Boot:** A Java-based framework for building web applications.
* **Spring MVC:** A module of the Spring Framework that supports building web applications.
* **Java:** The programming language used for backend development.
* **Hibernate:** An Object-Relational Mapping (ORM) framework used for database interactions.
* **MySQL:** The chosen database management system.
---
## Project Structure
The project is structured into the following components:

* **Controller:** Handles incoming HTTP requests, manages the data flow, and sends responses back to the client.
* **Service:** Implements business logic and interacts with the repositories.
* **Repository:** Handles database operations and provides an interface for data access.
* **Model:** Represents the database entities, such as Doctor, Patient, Appointment and AuthenticationToken.
* **DTO:** Data Transfer Objects used for transferring data between layers.
---
## Data Flow

* **Patient Registration (Sign-Up):** Patients can register on the platform by providing necessary details such as email and password. The system will issue a unique authentication token (OTP) to the valid email.
* **Patient Authentication (Sign-In):** Registered patients can log in to the system using their credentials. The system will validate the information and issue a unique authentication token upon successful login.
* **Patient Deletion (Sign-Out):** Registered patients can log out to the system using their credentials. The system will remove the information from the database.
* **Appointment Scheduling:** Patients can browse through available doctors and schedule appointments based on their preferred time slots and the doctor's availability.
* **Appointment Cancelation:** Patients can cancel their appointments.
* **Data Storage:** Patient data, appointment details, and other relevant information will be stored in the MySQL database.
---
## Database Design
The application's database design will consist of the following key entities:

* **Patient Table:** Stores user information such as username, email, encrypted password, age, address, gender."OneToOne" relation with appointment table.
* **Doctors Table:** Contains details about doctors, including their names, specialization, consultant fees and contact information. "OneToMany" relation to the appointment table.
* **Appointments Table:** Stores appointment information, including the doctor's and patient's IDs, appointment date and time, status, and any associated notes.
* **AuthenticationToken Table:** tores active authentication tokens and their associated user ID and expiration time. "OneToOne" relation with the patient.
---
## Conclusion
> The Doctor-Patient project aims to streamline the appointment scheduling process between doctors and patients. The use of Spring Boot ensures a robust and scalable application. By leveraging MySQL as the database management system, the application can efficiently store and retrieve user and appointment information. With the Sign-Up, Sign-In, and Sign-Out functionalities, users can securely access the system, interact with doctors, and manage their appointments effectively. This project serves as a foundation for building a comprehensive doctor-patient interaction platform.
