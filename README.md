# 💰 Expense Tracker

A simple and user-friendly **Expense Tracker web application** built using **Python Flask**, **SQLite**, **HTML/CSS**, **Jinja2 templates**, and **Chart.js**.

The application allows users to record their daily expenses, view expense records, filter expenses by different time periods, calculate total spending, and visualize category-wise spending through charts.

---

## 📌 Project Overview

The Expense Tracker is designed as a beginner-friendly web application for managing personal expenses.

Users can:

- Add a new expense
- Store expense description, category, amount, and date
- View all saved expenses
- Delete an expense
- Filter expenses by:
  - Today
  - Current Month
  - Current Quarter
  - Current Year
  - Custom Date Range
- View total expenses
- View category-wise spending using:
  - Pie Chart
  - Bar Chart

The application stores data locally in an SQLite database.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | Web application framework |
| SQLite | Database |
| HTML5 | Page structure |
| CSS3 | Styling and responsive layout |
| Jinja2 | Dynamic HTML templating |
| Chart.js | Expense data visualization |

---

## 📂 Project Structure

```text
Expense_tracker/
│
├── app.py
├── expenses.db
│
├── static/
│   └── style.css
│
├── templates/
│   └── index.html
│
└── README.md
```

### File Description

- **`app.py`**  
  Main Flask application. It contains the routes, database operations, expense filtering, and chart-data API.

- **`expenses.db`**  
  SQLite database containing the stored expense records.

- **`templates/index.html`**  
  Main user interface for adding, viewing, filtering, and deleting expenses.

- **`static/style.css`**  
  CSS file responsible for the application's visual design.

- **`README.md`**  
  Project documentation and setup instructions.

---

## ✨ Features

### 1. Add Expense

Users can enter:

- Description
- Category
- Amount
- Date

If no date is selected, the application automatically uses the current date.

### 2. View Expense Records

All saved expenses are displayed in a table containing:

- ID
- Description
- Category
- Amount
- Date
- Delete action

### 3. Delete Expense

Users can delete an existing expense directly from the expense table.

### 4. Expense Filters

The application provides predefined filters:

- **All** — displays all expenses
- **Today** — displays today's expenses
- **This Month** — displays expenses from the current month
- **This Quarter** — displays expenses from the current quarter
- **This Year** — displays expenses from the current year

It also supports a **custom date range** using From and To dates.

### 5. Total Expense Calculation

The application calculates the total amount of the currently displayed expense records.

### 6. Expense Visualization

The application provides two charts:

- **Pie Chart** — shows the distribution of expenses by category.
- **Bar Chart** — shows total spending for each category.

Chart data is supplied by the Flask `/chart-data` endpoint in JSON format.

---

## 🗄️ Database

The project uses **SQLite**.

### Database Table: `expenses`

| Column | Type | Description |
|---|---|---|
| `id` | INTEGER | Primary key |
| `description` | TEXT | Description of the expense |
| `category` | TEXT | Expense category |
| `amount` | REAL | Expense amount |
| `date` | TEXT | Expense date |

The table is automatically created when the Flask application starts.

---

## 🔗 Application Routes

| Route | Method | Purpose |
|---|---|---|
| `/` | GET | Display all expenses |
| `/add` | POST | Add a new expense |
| `/delete/<expense_id>` | GET | Delete an expense |
| `/filter` | GET/POST | Filter expenses |
| `/chart-data` | GET | Return category-wise chart data |

---

## ⚙️ Installation and Setup

### Step 1: Open the Project

Open PowerShell or Command Prompt and run:

```powershell
cd "C:\Users\lenovo\Desktop\Expense_tracker"
```

### Step 2: Create a Virtual Environment

```powershell
python -m venv venv
```

### Step 3: Activate the Virtual Environment

For PowerShell:

```powershell
venv\Scripts\Activate.ps1
```

If PowerShell blocks script execution, you can use Command Prompt:

```cmd
venv\Scripts\activate
```

### Step 4: Install Flask

```powershell
pip install flask
```

### Step 5: Run the Application

```powershell
python app.py
```

You should see Flask start the development server.

Open the browser at:

```text
http://127.0.0.1:5000/
```

---

## ▶️ How to Use

1. Start the Flask application.
2. Open `http://127.0.0.1:5000/` in a browser.
3. Enter an expense description.
4. Enter the category.
5. Enter the amount.
6. Select a date if required.
7. Click **+ Add Expense**.
8. The expense will appear in the expense table.
9. Use the filter buttons to view expenses for different periods.
10. Use the **Delete** button to remove an expense.
11. Check the Pie and Bar charts to understand category-wise spending.

---

## 📊 Example Categories

Some possible expense categories are:

- Food
- Travel
- Bus
- Bike
- Petrol
- Shopping
- Education
- Bills
- Entertainment
- Other

---

## 📈 Data Visualization

Chart.js is loaded through a CDN:

```text
https://cdn.jsdelivr.net/npm/chart.js
```

The frontend requests chart data from:

```text
/chart-data
```

The Flask backend returns JSON containing category labels and their total amounts.

Example response:

```json
{
  "labels": ["Food", "Travel", "Shopping"],
  "values": [1500, 2500, 1200]
}
```

---

## 🔒 Current Project Scope

This is a local expense-management application intended for learning and academic/project purposes.

The current version does **not** include:

- User registration/login
- Multiple user accounts
- Cloud database
- Password authentication
- Expense editing
- Budget alerts
- Expense export to PDF/Excel

These can be added as future enhancements.

---

## 🚀 Future Enhancements

Possible improvements include:

1. User registration and login
2. User-specific expense records
3. Edit/update expense functionality
4. Monthly budget management
5. Budget warning notifications
6. Export expenses to CSV/Excel
7. Generate PDF expense reports
8. More detailed dashboards
9. Monthly and yearly comparison charts
10. Responsive mobile-friendly improvements
11. Deployment to a cloud platform
12. REST API integration
13. Improved input validation and error handling

---

## 🎓 Academic Project Information

**Project Name:** Expense Tracker

**Project Type:** Web Application

**Backend:** Python Flask

**Database:** SQLite

**Frontend:** HTML, CSS, Jinja2, Chart.js

**Purpose:** Personal expense management and data visualization

---

## 👨‍💻 Author

**Sachin Dhage**

GitHub repository:

https://github.com/sachindhage93/Expense_tracker
---

## 📜 License

This project is intended for educational and learning purposes.
