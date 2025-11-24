# APTASK1
Here’s a simple, beginner-friendly guide to set up a local PHP + MySQL development environment on your computer.

✅ Option 1: Use XAMPP (Easiest & Most Popular)

Works on Windows, macOS, and Linux.

Step 1: Download XAMPP

Go to the official Apache Friends site:
https://www.apachefriends.org

Download the version for your OS (prefer PHP 8+).

Step 2: Install XAMPP

Just follow the setup wizard and install it in the default location.

Step 3: Start Apache and MySQL

Open XAMPP Control Panel

Click Start for:

Apache (for PHP)

MySQL (for database)

If both turn green, it's working.

Step 4: Test PHP

Go to the XAMPP installation → htdocs folder
Example (Windows):

C:\xampp\htdocs


Create a file named:
test.php

Add:

<?php
phpinfo();
?>


Open browser and visit:

http://localhost/test.php


If you see the PHP info page → PHP is working ✔️

Step 5: Open phpMyAdmin for MySQL

In your browser, open:

http://localhost/phpmyadmin


Here you can:

create databases

create tables

import/export SQL

run queries

Step 6: Connect PHP to MySQL

Create a file, e.g., db.php:

<?php
$server = "localhost";
$user = "root";
$pass = "";
$db = "testdb";

$conn = new mysqli($server, $user, $pass, $db);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
echo "Connected successfully!";
?>


Run:

http://localhost/db.php


You should see:
Connected successfully!

✅ Option 2: Use WAMP (Windows only)

Download: https://www.wampserver.com

Install it

Start services from the WAMP panel

Root folder: www

phpMyAdmin link: http://localhost/phpmyadmin

✅ Option 3: Use MAMP (macOS & Windows)

Download: https://www.mamp.info

Install

Start servers

Root folder: htdocs

phpMyAdmin link: http://localhost/phpmyadmin

⭐ Recommended for Beginners: XAMPP

Easiest, quick setup, stable, widely used.

If you want, I can also provide:

✅ Sample PHP + MySQL CRUD project
✅ Folder structure for PHP project
✅ php.ini configuration tips
✅ How to install Composer for modern PHP
Just tell me!
