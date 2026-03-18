# 🐖 Mama Flor's Lechon House — Inventory & Staff Management System

> *From the kitchen to the ledger — keeping every branch running like clockwork.*

---

## 🍖 Welcome to the Story Behind the System

Picture this: it's another busy morning at **Mama Flor's Lechon House**, one of Cebu's beloved go-to spots for golden, crispy lechon. Orders are rolling in, staff are hustling across multiple branches, and somewhere in the back office, someone is juggling handwritten attendance sheets, loose-leaf sales tallies, and a mental map of which product went where.

Sound familiar? For many small Filipino restaurant businesses, this is the daily reality — and it's exactly the kind of chaos that **Mama Flor's Inventory & Staff Management System** was built to fix.

This web-based system brings structure, visibility, and accountability to every corner of the operation — from tracking how many kilos of *liempo* were cooked to confirming that the morning shift clocked in on time across all branches.

---

## 🔥 What Is This System?

**Mama Flor's Lechon House Management System** is a full-featured, role-based web application designed specifically for managing the day-to-day operations of a multi-branch lechon restaurant business.

Built with **PHP**, **MySQL**, and plain good sense, the system serves two types of users:

- 👑 **Administrators** — who oversee all branches, manage staff and accounts, and review analytics
- 🧑‍🍳 **Staff Members** — who log in, get assigned to their branch, and submit daily sales reports

The system doesn't try to do everything — it does the *right* things well.

---

## 😤 The Problems It Solves

Running a restaurant isn't just about the food. Behind every perfectly roasted pig is a mountain of operational headaches. Here's what this system tackles head-on:

### 1. 📋 The Paper Trail Problem
Before this system, tracking which staff member worked which day at which branch meant digging through notebooks or spreadsheets — if they existed at all. **Attendance records are now tied directly to login sessions**, automatically logging time-in the moment a staff member authenticates.

### 2. ⏰ The "Who Was Late?" Problem
With manual attendance, tardiness is easy to overlook. This system automatically flags staff as **Present, Absent, or Late** based on their login time (cutoff: 8:00 AM Manila time), removing guesswork and reducing favoritism.

### 3. 🧾 The Sales Accountability Gap
How much was cooked? How much was reheated? How much was actually sold — and how much was left over? These numbers matter for both inventory control and cash reconciliation. The **daily sales report module** captures every quantity: cooked, reheated, displayed, sold, leftover, and pulled out — tied directly to the staff member who submitted it.

### 4. 🏪 The Multi-Branch Coordination Challenge
Operating two branches (Tipolo and Lapu-Lapu, Cebu) means double the complexity. Without a centralized system, assignments slip through the cracks and performance is nearly impossible to compare. This system provides **branch-level visibility** so management knows exactly what's happening at every location.

### 5. 💸 The Revenue Reconciliation Headache
How do you know if the cash remitted matches what was sold? By linking each sales report to a staff member and branch — and requiring **admin confirmation before a report is finalized** — the system creates an audit trail that makes discrepancies obvious.

### 6. 🗂️ The Scattered Staff Records Problem
Employee information — contact numbers, addresses, salary, SSN, TIN — is often scattered across HR folders or a manager's inbox. The **staff directory module** centralizes all employee data, making it accessible and editable from one place.

### 7. 📊 The "Flying Blind" Analytics Problem
Without data, decisions are gut-feeling guesses. The **admin dashboard** gives management a real-time view of sales performance — filterable by day, week, month, or year — powered by visual charts so trends are easy to spot.

### 8. 🔐 The "Anyone Can Touch Anything" Security Problem
Not every employee needs access to payroll data or branch settings. The **role-based access system** ensures that administrators and regular staff each see only what's relevant to their role — protecting sensitive business data.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | PHP 8.2 |
| Database | MySQL / MariaDB 10.4 |
| Frontend | HTML, CSS, JavaScript |
| Charts | CanvasJS |
| Typography | Google Fonts (Poppins, Jost) |
| Server | Apache (localhost) |
| Auth | bcrypt password hashing |

---

## 🗂️ Core Modules at a Glance

| Module | What It Does |
|---|---|
| **Login & Authentication** | Secure login with bcrypt; auto-records staff time-in on login |
| **Dashboard** | Visual sales analytics across branches and date ranges |
| **Staff Management** | Full employee directory with contact info, salary, and status |
| **Account Management** | User credentials and role assignments (Admin / Regular) |
| **Branch Management** | Multi-branch setup and contact details |
| **Product Management** | Menu item catalog with pricing |
| **Sales Reports** | Daily quantity and revenue tracking, pending/confirmed workflow |
| **Attendance & Assignment** | Daily staff-branch assignments with attendance status |

---

## 🚀 Getting Started

### Prerequisites

- PHP 8.2+
- MySQL / MariaDB 10.4+
- Apache web server (XAMPP, WAMP, or Laragon recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/wolfgang04/IM2.git
   cd IM2
   ```

2. **Set up the database**
   - Create a MySQL database named `mamaflors`
   - Import the schema:
     ```bash
     mysql -u root -p mamaflors < mamaflors.sql
     ```

3. **Configure your web server**
   - Point your web server's document root to the project folder
   - Or place the folder inside `htdocs/` (XAMPP) or `www/` (WAMP/Laragon)

4. **Open in browser**
   ```
   http://localhost/IM2/
   ```

5. **Log in**
   - Use the sample credentials from the database or create a new admin account

---

## 📁 Project Structure

```
IM2/
├── index.php                  # Login page
├── authentication.php         # Session & time-in handler
├── dashboard.php              # Admin analytics dashboard
├── staff.php                  # Staff directory
├── account.php                # Account management
├── branch.php                 # Branch management
├── product.php                # Product/menu management
├── salesreport.php            # Sales report viewer
├── addsalesreport.php         # Daily sales entry form
├── assignment.php             # Staff-branch assignment tracker
├── addattendance.php          # Attendance recorder
├── styles.css                 # Main stylesheet
├── mamaflors.sql              # Database schema & sample data
├── confirmationfolder/        # Confirmation dialog pages
├── errorfolder/               # Error message pages
└── imagesources/              # Brand assets (logo, icons)
```

---

## 👥 User Roles

### 🔑 Administrator
- Full access to all modules
- Confirms or rejects pending sales reports
- Views cross-branch analytics and dashboards
- Manages staff, accounts, products, and branches

### 🧑‍🍳 Regular Staff
- Logs in and is auto-assigned to their branch
- Submits and edits their own daily sales reports
- Views their own attendance and assignment history

---

## 📸 Feature Highlights

- **Auto Time-In**: Staff login automatically records their time-in, flagging them as Late if after 8:00 AM (Asia/Manila timezone)
- **Dynamic Sales Forms**: Sales report forms dynamically add product rows, making data entry fast and flexible
- **Pending → Confirmed Workflow**: Reports stay in "Pending" status until reviewed and confirmed by an admin
- **Revenue Estimation**: The system auto-calculates estimated revenue based on quantities sold and product prices
- **Date Range Filtering**: View sales data by a specific day, week, month, or year on the dashboard

---

## 🤝 Contributing

Have ideas for improvement? Found a bug? Pull requests are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to your branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Built with ❤️ for Mama Flor's Lechon House — because great food deserves great systems.*
