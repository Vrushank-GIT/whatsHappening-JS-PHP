# whatsHappening-JS-PHP

The What's Happening Full Stack Website uses PHP, JavaScript, HTML, CSS, and MySQL to create a lightweight Content Management System (CMS) for community events. 

This project is a full-stack web application that allows users to manage and view upcoming events securely.

## Main Features

* **Secure User Registration and Login:** Users can create accounts with strong passwords that adhere to strict security rules, including length, character types, and special characters. Passwords are securely stored in the database as hashed values.
* **Password Validation:** Passwords are validated using regular expressions during account creation, ensuring they meet all criteria with appropriate error messages for any deficiencies.
* **Future Events Display:** Dynamically shows only future events on the homepage, events page, and single-post pages based on the current date and time.
* **Prepared Statements for Database Security:** All SQL queries use prepared statements to prevent SQL injection attacks.
* **Responsive Pages:** The site features a landing page, an about page, a community groups page, an events page, and a login page, all adapting a Bootstrap theme for a cohesive look and feel.

## Screenshots

**Homepage / Landing Page**

<img width="1779" height="980" alt="Screenshot 2026-04-05 at 8 21 36 PM" src="https://github.com/user-attachments/assets/25c984cc-6e15-4908-b86b-867ff3183038" />
<img width="1795" height="980" alt="Screenshot 2026-04-05 at 9 01 01 PM" src="https://github.com/user-attachments/assets/a9f09ce9-26dd-4132-a3f0-312ad08dc845" />

**Events Directory**
<img width="1794" height="983" alt="Screenshot 2026-04-05 at 9 21 38 PM" src="https://github.com/user-attachments/assets/d754d8d7-e739-4714-bf79-17e1a330c8c4" />

**Secure Login & Registration**
<img width="890" height="972" alt="Screenshot 2026-04-05 at 9 26 21 PM" src="https://github.com/user-attachments/assets/89217a4c-4da8-45cf-8f98-d29c56230df2" />

**Single Event View**
<img width="1794" height="983" alt="Screenshot 2026-04-05 at 9 21 38 PM" src="https://github.com/user-attachments/assets/37ad4f93-9c03-4a58-ae74-2bdc7700edff" />

## Purpose of Assignments Over the Term

Throughout the term, this project was built as a lightweight Content Management System (CMS) called What's Happening. This online site allows community members to upload their events and contact information, enabling users to view upcoming events and potentially contact event organizers to purchase tickets or contribute.

By the end of the course, the site features:
* Responsive pages with a landing page.
* Collections of events organized by themes and dates.
* The ability for community groups to upload events.
* A search functionality for users to find events.
* Administrative duties such as uploading event information, removing events after their dates, and ensuring site security.

## Users of the Site

* **Community Groups:** Can securely log in and add events.
* **General Users:** Can view upcoming events.
* **Administrators:** Ensure the site is secure and up to date.

## Assignment Description

The project was built in stages. For the first assignment, the goal was to become familiar with the code and structure of the Bootstrap theme by adapting it to meet the project requirements. Templates were created for the following pages:

* Homepage (landing page) - `index.php`
* About page - `about.php`
* Community groups page - `groups.php`
* Events by themes and dates - `events.php`
* Login page - `login.php`
* Add Events page - `post.php` 

As the project progressed, static data was replaced with file-based reading (CSVs), and eventually upgraded to a fully relational MySQL database utilizing PHP session management and secure authentication.

## Installation Steps

To run this project locally, you will need to set up either MAMP or XAMPP.

**1. Download and Install MAMP or XAMPP:**
* MAMP: https://www.mamp.info/
* XAMPP: https://www.apachefriends.org/index.html

**2. Set Up the Project:**
* Clone this repository or download the ZIP file.
* Place all project files in the `htdocs` directory of your MAMP or XAMPP installation.
  * For MAMP: `/Applications/MAMP/htdocs/whatsHappening-JS-PHP`
  * For XAMPP: `C:\xampp\htdocs\whatsHappening-JS-PHP`

**3. Database Setup:**
* Open phpMyAdmin (`http://localhost/phpmyadmin`).
* Create a new database named `whats_happening`.
* Import the provided SQL dump file (`whats_happening.sql`) to set up the necessary tables (Groups, Events, EventTypes, and Login). Ensure the Login table has a VARCHAR(255) field for storing hashed passwords.

**4. Configuration:**
* Update the database connection settings in your PHP connection file (e.g., `serverlogin.php`) with your local database credentials (usually `root` for both username and password).

**5. Start the Server:**
* Start MAMP or XAMPP and ensure the Apache and MySQL services are running.

**6. Access the Application:**
* Open your web browser and navigate to `http://localhost/whatsHappening-JS-PHP/` to access the application.

## Acknowledgements

* PHP for server-side scripting.
* MySQL for database management.
* Bootstrap for the responsive front-end framework.
* MAMP and XAMPP for local development environments.
* All images used in this project are stock images available from Microsoft PowerPoint.
* Dummy text generated using Lorem Ipsum.
