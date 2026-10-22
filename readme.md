# StudentHub Portal - PHP + MySQL

This version keeps the original StudentHub visual design and adds a working PHP/MySQL backend.

## Folder structure

- `index.php` - project entry point
- `pages/` - StudentHub pages
- `backend/` - PHP authentication, forms, event registration and admin actions
- `database/studenthub.sql` - single SQL database file
- `css/style.css` - original frontend stylesheet
- `css/forms.css` - additional styles for forms/data cards

## Setup with XAMPP

1. Install/start **Apache** and **MySQL** in XAMPP.
2. Copy the `StudentHub-main` folder into `C:\xampp\htdocs\`.
3. Open phpMyAdmin: `http://localhost/phpmyadmin`
4. Import `database/studenthub.sql`.
5. Check `backend/config.php`. Default XAMPP settings are:
   - host: `localhost`
   - database: `studenthub`
   - username: `root`
   - password: empty
6. Open: `http://localhost/StudentHub-main/`
7. Create an administrator using `backend/setup_admin.php`.
8. After creating the admin, delete `backend/setup_admin.php` for safety.
9. Login using the admin account. Students can register from the Register page.

## Main features

- Student registration/login/logout
- Password hashing with PHP `password_hash`
- Session-based authentication
- Student dashboard
- Profile update
- Event listing/search
- Event registration with capacity checking
- Contact form saved to MySQL
- Feedback form saved to MySQL
- Admin dashboard
- Admin event add/hide/show/delete
- Admin student enable/disable
- Prepared SQL statements
- Basic input validation

## Important

The database is MySQL/MariaDB. The SQL file creates the `studenthub` database and all required tables.

For production hosting, change database credentials, enable HTTPS, add CSRF protection, and use a restricted database user.
