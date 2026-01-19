# Tambayan-ng-Tinig
TAMBAYAN NG TINIG: A PUBLIC FREEDOM SENTIMENT KIOSK SYSTEM FOR BARANGAY MUZON SOUTH, CITY OF SAN JOSE DEL MONTE, BULACAN



That’s a very important technical detail. Using ODBC (Open Database Connectivity) is the bridge that allows your Visual Basic 2008 application to talk to your MySQL database.

I've updated the Installation & Setup and Technologies sections to specifically mention the MySQL ODBC Driver, which is the piece of software someone else would need to install to make your project work.

🗣️ Tambayan ng Tinig (Voice Hangout)
Tambayan ng Tinig is a resident feedback and sentiment management system developed using Visual Basic 2008. This application serves as a bridge between the community and local leadership, providing a public kiosk for resident submissions and a secure administrative dashboard for tracking, resolving, and auditing concerns.

🚀 Key Features
🖥️ Kiosk Interface (Resident Side)
Standardized Data Entry: Optimized for fast and reliable data submission using standard input hardware.

Validation & Constraints: * Strict input masking for contact numbers (11 digits).

Numeric-only restrictions for Block and Lot fields.

Character limit of 80 for subject lines to ensure conciseness.

Adaptive Address Formatting: The interface dynamically adjusts address guides based on the selected area—such as Harmony Hills or Pabahay 2000—to ensure the data matches the specific layout of the neighborhood.

Sentiment Categorization: Residents can classify their input as a Suggestion, Complaint, Feedback, or Others.

Auto-Reference Generation: The system instantly generates a unique Reference Number (e.g., MZN-2025-HAR-C001) for every submission.

🛡️ Admin Dashboard (Official Side)
Role-Based Access Control (RBAC): Secure login with distinct permissions for Admin, Secretary, and Captain accounts.

Comprehensive Audit Trails: * Account Logs: Monitors login and logout times for security auditing.

Sentiment Logs: Tracks every status change including who made the change and when.

Complaint Analytics: Automatically tracks and tallies complaints directed toward specific individuals.

System Configuration: Global settings management, including a Daily Submission Limit of 10 entries.

🛠️ Technologies Used
Language: Visual Basic .NET

IDE: Microsoft Visual Basic 2008

Database: MySQL (tnt_db)

Connectivity: ODBC (Open Database Connectivity)

Driver: MySQL ODBC 3.51 or 5.1 Driver (depending on your specific version. Dev used 9.3.0 https://downloads.mysql.com/archives/c-odbc/)

Tools: XAMPP / phpMyAdmin

⚙️ Installation & Setup
Clone the repository:

Bash
git clone https://github.com/yourusername/tambayan-ng-tinig.git
Database Setup:

Ensure XAMPP or a MySQL server is running.

Create a new database named tnt_db and import the tnt_db.sql file.

Install ODBC Driver:

You must install the MySQL ODBC Connector on your Windows machine.

Go to Control Panel > Administrative Tools > Data Sources (ODBC).

Create a System DSN or ensure your connection string matches the driver version installed (e.g., Driver={MySQL ODBC 5.1 Driver}).

Configure Connection:

Open the project in Visual Basic 2008.

Update the OdbcConnection string in your code to match your local credentials.

🗄️ Core Database Schema
The system relies on several relational tables within tnt_db:

sentiment_tbl: The core table storing all resident reports and current status.

accounts_tbl: Stores user credentials and access levels.

sentiment_logs_tbl: Audit trail for tracking all modifications.

system_config_tbl: Stores application-wide parameters like the daily submission limit (10).


## 🛠 How to Setup (For Testing)

### 1. Database Setup
* Open XAMPP and start **Apache** and **MySQL**.
* Go to `localhost/phpmyadmin`.
* Create a database named `tnt_db`.
* Click **Import** and select the `tnt_db.sql` file from this repository.

### 2. ODBC Driver (Required)
Since this app uses ODBC to connect to MySQL:
* Download and install the **MySQL ODBC Connector (3.51 or 5.1)**.
* Open **ODBC Data Source Administrator** on your Windows PC.
* Add a new **System DSN** named `tnt_db` (or whatever name you used in your code).
* Link it to your MySQL server (usually `localhost`, user `root`, no password).

### 3. Run the App
* Open the installed application and start submitting feedback!
