# Elibrary-Management-System
A web-based E-Library Management System that allows users to browse, search, and manage digital books and resources. Features include user registration, book catalog management, borrowing system, and an admin panel to manage library operations efficiently.

# Superior University E-Library System
### Complete PHP/MySQL Library Management System

---

## 📋 REQUIREMENTS
- XAMPP (Apache + MySQL + PHP 7.4+)
- Browser (Chrome, Firefox, Edge)

---

## 🚀 INSTALLATION STEPS

### Step 1 — Copy Project Files
Copy the entire `elibrary` folder to:
```
C:\xampp\htdocs\elibrary
```

### Step 2 — Import Database
1. Start **XAMPP** — start Apache and MySQL
2. Open your browser and go to: `http://localhost/phpmyadmin`
3. Click **"New"** on the left sidebar
4. Create a database named: `elibrary`
5. Select the `elibrary` database
6. Click **"Import"** tab at the top
7. Click **"Choose File"** and select `database.sql` from the project folder
8. Click **"Go"** to import

### Step 3 — Configure Database (if needed)
If your MySQL has a different username/password, edit:
```
elibrary/admin/includes/config.php
```
Change these lines:
```php
define('DB_USER', 'root');   // your MySQL username
define('DB_PASS', '');       // your MySQL password (blank for default XAMPP)
```

### Step 4 — Create Upload Folders
Make sure these folders exist and are writable:
```
elibrary/admin/bookimg/       ← book cover images
elibrary/assets/ebooks/       ← PDF e-books
```
These are created automatically when you add books.

### Step 5 — Add Logo
Place your university logo file as:
```
elibrary/assets/img/logo.png
```

---

## 🔑 DEFAULT LOGIN CREDENTIALS

### Admin Login
- **URL:** `http://localhost/elibrary/admin/login.php`
- **Email:** `admin@elibrary.edu`
- **Password:** `password`

> ⚠️ Change these credentials after first login via Settings page!

### Student Login
- Students register themselves at: `http://localhost/elibrary/student/register.php`

---

## 📁 PROJECT STRUCTURE

```
elibrary/
├── index.php                    ← Landing page (role selection)
├── database.sql                 ← Database import file
├── README.md
│
├── assets/
│   ├── css/
│   │   └── style.css            ← Global stylesheet (purple & white theme)
│   ├── img/
│   │   └── logo.png             ← University logo
│   └── ebooks/                  ← Uploaded PDF e-books
│
├── admin/
│   ├── login.php                ← Admin login
│   ├── register.php             ← Admin registration
│   ├── logout.php
│   ├── dashboard.php            ← Admin overview
│   ├── manage-books.php         ← View/search/delete books
│   ├── add-book.php             ← Add new book + cover + PDF
│   ├── edit-book.php            ← Edit book details
│   ├── manage-categories.php    ← Add/edit/delete categories
│   ├── manage-authors.php       ← Add/edit/delete authors
│   ├── issue-book.php           ← Issue physical book to student
│   ├── return-book.php          ← Process returns + auto fine calc
│   ├── issued-books.php         ← Full issue history with filters
│   ├── manage-fines.php         ← View/pay/waive fines
│   ├── manage-students.php      ← View all students
│   ├── view-student.php         ← Student detail + issue history
│   ├── student-activity.php     ← E-book read/download log
│   ├── settings.php             ← Fine rate, loan days, password
│   ├── bookimg/                 ← Uploaded book cover images
│   └── includes/
│       ├── config.php           ← DB connection
│       ├── header.php           ← Admin layout header + sidebar
│       └── footer.php           ← Admin layout footer
│
└── student/
    ├── login.php                ← Student login
    ├── register.php             ← Student self-registration
    ├── logout.php
    ├── dashboard.php            ← Student overview
    ├── browse-books.php         ← Browse + search + filter + read/download
    ├── read-book.php            ← Inline PDF reader
    ├── my-issues.php            ← Student's borrowed books
    ├── my-fines.php             ← Student's fines
    ├── my-profile.php           ← Edit profile + change password
    └── includes/
        ├── config.php
        ├── header.php
        └── footer.php
```

---

## ✨ FEATURES

### Admin Panel
- 📊 Dashboard with live statistics (books, students, issued, overdue, fines)
- 📚 Full book management — add, edit, delete with cover image & PDF upload
- 🏷️ Category & Author management
- 📤 Issue books to students with automatic due date
- 📥 Return books with automatic fine calculation (live preview)
- 💰 Fine management — mark paid or waive
- 👥 Student management — view, activate/deactivate, delete
- 👁️ Per-student detail view (issue history + e-book activity)
- 📈 E-book activity log (reads & downloads)
- ⚙️ Settings — loan period, fine rate, library name, admin password

### Student Portal
- 🏠 Personal dashboard with current loans & overdue alerts
- 📚 Browse entire catalogue with search + category filter
- 📖 Read e-books inline (PDF viewer in browser)
- 📥 Download e-books as PDF
- 📋 Full issue history with status tracking
- 💰 Fine status with running calculation
- 👤 Edit profile & change password

---

## ⚙️ CONFIGURABLE SETTINGS (via Admin → Settings)
| Setting | Default | Description |
|---------|---------|-------------|
| Loan Days | 14 | Days before a book is overdue |
| Fine Per Day | ₨10 | Daily fine for overdue books |
| Library Name | Superior University E-Library | Displayed in header |

---

## 🎨 THEME
- **Primary color:** Purple `#4b2c5e`
- **Background:** Soft lavender `#f5f0fa`
- **Fonts:** Playfair Display (headings) + DM Sans (body)
- **Design:** Professional card-based layout with sticky header and sidebar

---

*Built for Superior University — XAMPP/PHP/MySQL*
