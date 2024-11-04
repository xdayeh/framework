# PHP MVC Framework

## Table of Contents
- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Object-Oriented Programming (OOP) Structure](#object-oriented-programming-oop-structure)
- [Contributing](#contributing)
- [License](#license)

---

## About

This is a custom PHP framework built on the **Model-View-Controller (MVC)** architecture. It provides a robust structure for building scalable web applications in PHP, and it leverages MySQL as the database.

This framework is designed to be minimalistic yet flexible, making it easy to understand, extend, and maintain. It's ideal for developers looking to build from scratch without relying on heavy, opinionated frameworks.

---

## Features

- **MVC Architecture**: Separates application logic, data handling, and UI.
- **Routing System**: A straightforward routing system to define and manage routes.
- **Error Handling**: Basic error-handling for a more user-friendly development experience.
- **Database Management**: MySQL database with PHP's PDO extension for secure and prepared statements.
- **Built for Ubuntu Linux**: Tested on Ubuntu latest version with Apache and MySQL.

---

## Prerequisites

To run this framework, you need:
- **Ubuntu** (latest version recommended)
- **Apache** (latest version)
- **PHP** (latest version)
- **MySQL** (latest version)

---

## Installation

1. **Update System Packages**
   ```bash
   sudo apt-get update
   ```

2. **Install Apache and MySQL**
   ```bash
   sudo apt-get install apache2 mysql-server -y && mysql_secure_installation
   ```

3. **Install PHP and Required Extensions**
   ```bash
   sudo apt-get install php libapache2-mod-php php-mysql -y
   ```

4. **Configure Apache Directory Index**
   - Open Apache configuration file:
     ```bash
     sudo nano /etc/apache2/mods-enabled/dir.conf
     ```
   - Move `index.php` to the first position to prioritize PHP files:
     ```apache
     <IfModule mod_dir.c>
         DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
     </IfModule>
     ```

5. **Clone the Repository**
   ```bash
   git clone https://github.com/xdayeh/framework.git
   cd framework
   ```

6. **Set Up the Database**
   - Create a MySQL database:
     ```sql
     CREATE DATABASE your_database_name;
     ```
   - Configure database settings in `/config/database.php` to connect to MySQL:
     ```php
     define('DB_HOST', 'localhost');
     define('DB_USER', 'your_username');
     define('DB_PASS', 'your_password');
     define('DB_NAME', 'your_database_name');
     ```

---

## Usage

- **Start Apache Server**
   ```bash
   sudo service apache2 start
   ```

- **Access the Framework**
   - Open a web browser and navigate to `http://localhost` to start using the framework.

### Directory Structure

- **app**: Contains the application code (models, views, controllers).
- **config**: Contains configuration files.
- **public**: Public-facing files (e.g., index.php).
- **vendor**: Dependencies managed via Composer (if needed).
- **.htaccess**: Configuration for routing all requests through `index.php`.

---

## Object-Oriented Programming (OOP) Structure

This framework is built with **Object-Oriented Programming (OOP)** principles to ensure modularity, reusability, and a clear structure.

- **Models**: Encapsulate data and interact with the database using PHP classes and objects.
- **Controllers**: Manage the flow between models and views, and utilize methods to handle user requests.
- **Views**: Present data to the user and maintain a clear separation from the business logic.

OOP allows the framework to be easily extensible by leveraging **inheritance, encapsulation, and polymorphism**. Each component can be customized or extended without affecting other parts of the application.

---

## Contributing

If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are welcome.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
