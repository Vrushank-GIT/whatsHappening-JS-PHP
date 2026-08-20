# whatsHappening — Community Events CMS

A full-stack Content Management System (CMS) that allows community groups to post and manage local events, with secure user authentication and a dynamic, date-aware event feed.

> **Tech Stack:** `PHP` · `JavaScript` · `HTML` · `CSS` · `MySQL` · `Bootstrap`

---

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [User Roles](#user-roles)
- [Project Background](#project-background)
- [Acknowledgements](#acknowledgements)

---

## Features

- **Secure Authentication:** User registration and login with password hashing (bcrypt) and regex-enforced strength rules covering length, character types, and special characters.
- **SQL Injection Prevention:** All database queries use PHP prepared statements throughout the application.
- **Dynamic Event Feed:** Only future events are displayed — filtered in real time based on the current date and time — across the homepage, events directory, and single-event pages.
- **Role-Based Access:** Community groups can log in and post events; general users browse without an account; administrators manage content and security.
- **Responsive UI:** Built on a Bootstrap theme across 6 pages, adapting cleanly to mobile and desktop viewports.

---

## Screenshots

**Homepage / Landing Page**

<img width="1779" height="980" alt="Homepage" src="https://github.com/user-attachments/assets/25c984cc-6e15-4908-b86b-867ff3183038" />
<img width="1795" height="980" alt="Homepage scrolled" src="https://github.com/user-attachments/assets/a9f09ce9-26dd-4132-a3f0-312ad08dc845" />

**Events Directory**

<img width="1794" height="983" alt="Events Directory" src="https://github.com/user-attachments/assets/d754d8d7-e739-4714-bf79-17e1a330c8c4" />

**Secure Login & Registration**

<img width="890" height="972" alt="Login page" src="https://github.com/user-attachments/assets/89217a4c-4da8-45cf-8f98-d29c56230df2" />

**Single Event View**

<img width="1794" height="983" alt="Single event view" src="https://github.com/user-attachments/assets/37ad4f93-9c03-4a58-ae74-2bdc7700edff" />

---

## Project Structure

```
whatsHappening-JS-PHP/
├── assets/             # CSS, images, and JS assets
├── forms/              # Form handling logic
├── files/              # Supporting files (CSV imports, etc.)
├── index.php           # Homepage / landing page
├── about.php           # About page
├── groups.php          # Community groups directory
├── events.php          # Events listing by theme and date
├── single-post.php     # Individual event view
├── login.php           # Login page
├── post.php            # Add/manage events (authenticated)
├── logout.php          # Session teardown
├── functions.php       # Shared utility functions
├── serverLogin.php     # DB connection & session config
└── whats_happening.sql # Database schema + seed data
```

---

## Getting Started

To run this project locally you will need **MAMP** (Mac) or **XAMPP** (Windows) — these are local server environments that bundle Apache and MySQL together.

**1. Install a local server environment**

- MAMP (Mac): https://www.mamp.info/
- XAMPP (Windows): https://www.apachefriends.org/

**2. Clone the repo and place it in your server root**

```bash
git clone https://github.com/Vrushank-GIT/whatsHappening-JS-PHP.git
```

- MAMP: move the folder to `/Applications/MAMP/htdocs/`
- XAMPP: move the folder to `C:\xampp\htdocs\`

**3. Set up the database**

- Open phpMyAdmin at `http://localhost/phpmyadmin`
- Create a new database named `whats_happening`
- Import `whats_happening.sql` — this creates the `Groups`, `Events`, `EventTypes`, and `Login` tables with sample data

**4. Configure your database connection**

Open `serverLogin.php` and update the credentials:

```php
$host = 'localhost';
$user = 'root';       // default for MAMP/XAMPP
$password = 'root';   // default for MAMP; blank '' for XAMPP
$database = 'whats_happening';
```

**5. Start the server and open the app**

- Launch MAMP or XAMPP and start Apache + MySQL
- Visit: `http://localhost/whatsHappening-JS-PHP/`

---

## User Roles

| Role | Capabilities |
|---|---|
| General User | Browse and view upcoming events |
| Community Group | Log in, post events, manage their listings |
| Administrator | Full content management, security oversight |

---

## Project Background

This project was built as a term-long CMS for CSCI at Dalhousie University, evolving from static Bootstrap templates → CSV file-based data → a fully relational MySQL database with PHP session management and secure authentication.

Key engineering decisions made along the way:
- Chose prepared statements over raw queries from the start to enforce secure DB access patterns
- Implemented password hashing at the model layer so no plain-text credentials ever touch the database
- Used date-based SQL filtering rather than client-side JS to prevent expired events from leaking into the DOM

---

## Acknowledgements

- [Bootstrap](https://getbootstrap.com/) — responsive front-end framework
- [PHP](https://www.php.net/) — server-side scripting
- [MySQL](https://www.mysql.com/) — relational database
- [MAMP](https://www.mamp.info/) / [XAMPP](https://www.apachefriends.org/) — local development environments
