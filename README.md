# Doctor Appointment System

## Project Description

The **Doctor Appointment System** is a web-based application that allows patients to book, manage, and cancel appointments with doctors. This system aims to simplify the process of booking doctor appointments, reducing wait times, and ensuring efficient management of doctor schedules. It provides patients and doctors with a seamless platform for managing appointments.

## Screenshots

### Index Page

![Index page](https://drive.google.com/uc?export=view&id=10GdU-HmabbZ2pZvwXFyl6C8K9X5kFHT2)

### Doctor Login

![Doctor Login](https://drive.google.com/uc?export=view&id=1arzkd8pAfs7-LxJ98Da4VuV8cS81L2wT)

### Admin Login

![Image](https://drive.google.com/uc?export=view&id=1HWn8ArKoe_JGUobotviDzlbTXJ-koD35)

### Patient Login page

![Image](https://drive.google.com/uc?export=view&id=1FX7jCGan4KDvu1Ny4TwvczjfFjb4KrD-)




## Features

- **Patient Registration**: Allows patients to register with their details (name, contact, medical history, etc.).
- **Doctor Profiles**: Doctors can create profiles with their specialization, availability, and other relevant details.
- **Appointment Booking**: Patients can browse available doctors based on specialization and book an appointment at a preferred time.
- **Appointment Cancellation**: Patients can cancel their appointments as needed.
- **Doctor Availability**: Doctors can set and manage their available hours.
- **Appointment Notifications**: Patients and doctors receive notifications of upcoming appointments via email/SMS.
- **Admin Panel**: Admin can manage patients, doctors, and appointments.

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript, React (or any preferred framework)
- **Backend**: Node.js, Express.js, Django, or any suitable framework
- **Database**: MySQL, PostgreSQL, or MongoDB
- **Email/SMS API**: SendGrid, Twilio, or any relevant service for notifications
- **Authentication**: JWT, OAuth, or traditional session-based authentication
- **Hosting**: AWS, Heroku, or any suitable platform

## Setup Instructions

### 1. Download and Install XAMPP

XAMPP is an easy-to-install Apache distribution that includes MySQL, PHP, and Perl. To set up your development environment, follow these steps:

- Go to the [XAMPP Download Page](https://www.apachefriends.org/download.html).
- Download the installer for your operating system (Windows, macOS, or Linux).
- Run the installer and follow the setup wizard.
- Once installed, open the **XAMPP Control Panel**.

### 2. Start Apache and MySQL

1. Open the **XAMPP Control Panel**.
2. Start the **Apache** and **MySQL** services by clicking the **Start** buttons next to each one. Both should turn green, indicating they are running.

### 3. Access phpMyAdmin

phpMyAdmin is a web-based application that allows you to interact with MySQL databases. To access it:

1. Open your web browser and go to `http://localhost/phpmyadmin`.
2. You will be directed to the phpMyAdmin login page. Use the default credentials:
   - **Username**: `root`
   - **Password**: (Leave it blank)
3. After logging in, you will see the phpMyAdmin dashboard.

### 4. Import the Database

To import your existing database (e.g., `hms.sql`) into MySQL using phpMyAdmin:

1. In the phpMyAdmin dashboard, click on the **Databases** tab.
2. In the **Create database** field, enter the name of your database (e.g., `hms`) and click **Create**.
3. Once the database is created, click on the newly created database in the left-hand sidebar.
4. Next, click on the **Import** tab at the top of the page.
5. In the **File to import** section, click **Choose File** and select the `hms.sql` file from your local machine.
6. Make sure the **Format** is set to SQL, and then click the **Go** button to start the import process.

   - **Note**: If your database file is large, you may need to adjust the `upload_max_filesize` and `post_max_size` settings in `php.ini` (located in the `xampp/php` folder).

### 5. Configure the Database Connection

Once the database is successfully imported, you need to configure your application to connect to it:

1. Open the `config.php` file (or equivalent configuration file in your project).
2. Edit the database connection settings with your local environment details:
   ```php
   $servername = "localhost";
   $username = "root";
   $password = "";
   $dbname = "hms";  // Make sure this matches the database name you created


