# Tambayan-ng-Tinig
TAMBAYAN NG TINIG: A PUBLIC FREEDOM SENTIMENT KIOSK SYSTEM FOR BARANGAY MUZON SOUTH, CITY OF SAN JOSE DEL MONTE, BULACAN



🗣️ Tambayan ng Tinig (Voice Hangout)
Tambayan ng Tinig is a resident feedback and sentiment management system built with Visual Basic .NET. It features a public kiosk for resident submissions and a secure administrative dashboard for barangay officials to track, resolve, and audit community concerns.

🚀 Key Features
🖥️ Kiosk Interface (Resident Side)
Standardized Data Entry: Residents use standard hardware input for fast and reliable data submission.

Validation: Strict input masking for contact numbers (11 digits), numeric-only block/lot fields, and character limits (80 for subjects).

Dynamic Address Guides: Address formats automatically adjust based on the selected subdivision (e.g., Harmony Hills vs. Pabahay 2000).

Sentiment Categorization: Residents can classify inputs as Suggestion, Complaint, Feedback, or Others.

Auto-Reference Generation: Instantly provides a unique Reference Number (e.g., MZN-2025-HAR-C001) for tracking.

🛡️ Admin Dashboard (Official Side)
Role-Based Access Control (RBAC): Distinct access levels for Admin, Secretary, and Captain.

Audit Trails:

Account Logs: Tracks every login and logout time for security.

Sentiment Logs: Records exactly who changed a ticket status (e.g., from Submitted to Approved or Denied) and when.

Complaint Analytics: Automatically tracks and counts complaints against specific individuals in the complained_person_tbl.

System Configuration: Admins can manage global parameters, including a Daily Submission Limit of 10.

🛠️ Technologies Used
Language: Visual Basic .NET (VB.NET)

Database: MySQL (tnt_db)

Framework: Windows Forms (WinForms)

Tools: Visual Studio, phpMyAdmin

⚙️ Installation & Setup
Clone the repository:

Bash
git clone https://github.com/yourusername/tambayan-ng-tinig.git
Database Setup:

Create a MySQL database named tnt_db.

Import the provided tnt_db.sql file located in the /database folder.

Configure Connection:

Update the MySQL connection string in your VB code to match your local server (e.g., server=localhost; user=root; database=tnt_db).

🗄️ Core Database Tables
sentiment_tbl: Stores all resident submissions and their current statuses (Submitted, Approved, Denied, Redirected).

accounts_tbl: Manages authentication and security for officials.

sentiment_logs_tbl: An audit trail that tracks all status transitions and field modifications.

system_config_tbl: Stores system-wide settings like the daily submission limit.
