# 💰 Expense Tracker

A comprehensive command-line interface (CLI) application for managing personal expenses with advanced reporting and analytics capabilities.

## 📋 Table of Contents

- [Features](#-features)
- [Data Management](#-data-management)
- [CLI Interaction](#-cli-interaction)
- [Technical Architecture](#-technical-architecture)
- [Development Roadmap](#-development-roadmap)
- [Getting Started](#-getting-started)

## ✨ Features

### 📊 Core Functionality
- **Add Expenses**: Record expenses with date, category, description, and amount
- **View & Filter**: Browse all expenses or filter by month/year/category
- **Edit & Delete**: Modify or remove existing expense entries
- **Data Persistence**: Secure local storage with automatic backups

### 📈 Reporting & Analytics
- **Period Summaries**: Total expenses for selected time periods
- **Category Analysis**: Breakdown by expense categories (e.g., Food: ₹5,000, Rent: ₹15,000)
- **Extremes Tracking**: Identify highest and lowest expenses per month
- **Trend Analysis**: Visual spending patterns over time

## 🗄️ Data Management

### Expense Operations
- ✅ Add an expense (date, category, description, amount)
- ✅ View all expenses
- ✅ View expenses for a given month/year
- ✅ View expenses by category
- ✅ Delete an expense
- ✅ Edit/update an expense

Show highest & lowest expenses in a given month

| Storage Type | Pros | Use Case |
|--------------|------|----------|
| **CSV** | Easy to read/write, human-readable | Simple projects, manual inspection |
| **JSON** | Structured data, easy parsing | Complex data relationships |
| **SQLite** | Database-like queries, ACID compliance | Advanced filtering and reporting |

## 🖥️ CLI Interaction

### Menu System
```
┌─────────────────────────────────┐
│        EXPENSE TRACKER          │
├─────────────────────────────────┤
│ 1. Add Expense                  │
│ 2. View Expenses                │
│ 3. View Summary                 │
│ 4. Delete Expense               │
│ 5. Edit Expense                 │
│ 6. Analytics & Reports          │
│ 7. Settings                     │
│ 8. Exit                         │
└─────────────────────────────────┘
```

### User Experience Features
- **Input Validation**: Robust error handling for all user inputs
- **Flexible Date Parsing**: Accept multiple formats (2025-08-10, 10/08/2025, etc.)
- **Clean Interface**: Clear console output with formatted displays
- **Interactive Prompts**: Guided user experience with helpful prompts

## 🏗️ Technical Architecture

### Code Organization
```
expense_tracker/
│
├── main.py             # Entry point
├── expense_manager.py  # Add, view, delete, edit logic
├── reports.py          # Summary & analytics
├── storage.py          # File handling (CSV/JSON/SQLite)
├── utils.py            # Helper functions (validation, formatting)
├── data/
│   └── expenses.csv
└── config.py           # Config settings (categories, file paths)

```

### Best Practices
- **Modular Design**: One function per action (`add_expense()`, `delete_expense()`, etc.)
- **Configuration Management**: Centralized config file for paths, categories, and settings
- **Error Handling**: Graceful handling of invalid inputs, missing files, and corrupted data
- **Data Safety**: Automatic backups before saving changes
- **Type Hints**: Full type annotation for better code maintainability

pgsql
Copy
Edit
1. Add Expense
2. View Expenses
3. View Summary
4. Delete Expense
5. Exit
User input validation (e.g., don’t allow text where numbers are required)

### 🚦 Basic Work Flow
'''
Welcome to Expense Tracker!
1. Add Expense
2. View All Expenses
3. View Summary
4. Delete Expense
5. Exit

Choice: 1
Date (YYYY-MM-DD): 2025-08-10
Category: Food
Description: Dinner at restaurant
Amount: 450
✅ Expense added successfully!

Choice: 3
Summary for August 2025:
Food: ₹3,450
Transport: ₹1,200
Rent: ₹15,000

'''


### Phase 1: Core Features ✅
- [x] Basic expense CRUD operations
- [x] CSV/JSON storage implementation
- [x] CLI menu system
- [x] Input validation

### Phase 2: Enhanced Analytics 📊
- [ ] Monthly budget setting & alerts
- [ ] Spending trends visualization (Matplotlib integration)
- [ ] Export reports (CSV/PDF)
- [ ] Advanced filtering and search

3️⃣ Good Coding Practices to Keep in Mind
Modular code

One function per action (add_expense(), delete_expense(), etc.)

main() function to control program flow

Config file

Keep file paths or categories in a separate config file

Error handling

Handle invalid input, missing files, corrupted data gracefully

Data backup

Create an auto-backup before saving new changes

4️⃣ Advanced / Optional Features
These can be added once you have the basics running.

Analytics
Monthly budget setting & alerts when crossing limit

# Run the application
python main.py
```

Export report as CSV or PDF

Integration Ideas
Azure Blob Storage: Store CSV in cloud instead of local

Pandas: Use for category summaries & filtering

PySpark (Future): Handle large expense datasets

APIs: Currency conversion if dealing with multiple currencies

Automation
Scheduled reminders to log expenses

**Built with ❤️ by [AnubhavBaranawal](https://github.com/AnubhavBaranawal)**
