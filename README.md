# Spendly — Smart Expense Tracker

A modern, lightweight expense tracking web app that syncs all your transactions directly to Google Sheets in real time.

Built with pure HTML, CSS, JavaScript, and Google Apps Script — no backend server required.

## ✨ Features

### 📊 Live Expense Tracking
* Add both Credit and Debit transactions
* Track income and expenses instantly
* Beautiful modern UI optimized for mobile devices

### ☁ Google Sheets Sync
Every transaction is automatically stored inside your own Google Sheet.

**Stored details:**
* Date
* Time
* Transaction Type
* Amount
* Reason
* Month
* Year
* Week Number

### 📈 Automatic Reports
Spendly automatically creates:
* **Monthly Reports**
  * Monthly credit totals
  * Monthly debit totals
  * Net balance
  * Auto-generated bar charts
* **Yearly Reports**
  * Year-wise financial summary
  * Credit vs Debit charts
* **Weekly Tracking**
  * Week numbers automatically generated
  * Easy filtering inside Google Sheets

### 🔄 Live Monthly Summary
At the top of the app, Spendly shows:
* Current Month
* Total Credits
* Total Debits
* Net Balance

*This data is fetched directly from Google Sheets in real time.*

### 📱 Mobile Friendly UI
* Smooth animations
* Responsive layout
* Clean dark theme
* Fast and lightweight
* Works directly in browser

---

## ⚙ How It Works

### Frontend
The frontend is built using:
* HTML
* CSS
* Vanilla JavaScript

**The app:**
1. Takes transaction input
2. Saves local copy in browser
3. Sends data to Google Apps Script
4. Google Apps Script stores data in Sheets
5. App fetches monthly summary from Sheets

### Backend (Google Apps Script)
Google Apps Script acts as:
* API server
* Database connector
* Report generator

* **`doPost()`**
  * Handles: Saving transactions and creating reports automatically
* **`doGet()`**
  * Handles: Returning current month summary and live balance updates

---

## 📂 Google Sheets Structure

### Sheet 1 — Transactions
Stores all raw transaction data.


| Date | Time | Type | Amount | Reason | Month | Year | Week |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

### Sheet 2 — Monthly_YYYY
*Example: `Monthly_2026`*

**Contains:**
* Monthly totals
* Net balances
* Charts

### Sheet 3 — Yearly_Summary
**Contains:**
* Yearly totals
* Charts
* Financial overview

---

## 🚀 Setup Guide

### Step 1 — Create Google Sheet
Create a new Google Spreadsheet.

### Step 2 — Open Apps Script
Inside Google Sheets:
**Extensions** → **Apps Script**

* Delete existing code.
* Paste the provided Apps Script code.
* Save the project.

### Step 3 — Deploy Web App
Click:
**Deploy** → **New Deployment**

Select:
**Web App**

Then set:

| Setting | Value |
| :--- | :--- |
| **Execute As** | Me |
| **Access** | Anyone |

* Click **Deploy**.
* Authorize permissions.
* Copy the generated Web App URL.

### Step 4 — Connect App
Open Spendly.

Go to:
**Settings** → **Web App URL**

* Paste the Apps Script URL.
* Click **Save**.

Done ✅

---

## 🔄 Data Flow
* **Saving Transaction:** User → HTML App → Apps Script → Google Sheets
* **Loading Monthly Summary:** HTML App → Apps Script (GET API) → Google Sheets

---

## 🧠 Technologies Used
* **Frontend:** HTML5, CSS3, JavaScript
* **Backend:** Google Apps Script
* **Database:** Google Sheets

---

## 🔐 Privacy
All data remains inside:
* Your own Google Account
* Your own Google Sheets

*No third-party database is used.*

---

## 📌 Important Notes
* Internet connection required for Google Sheets sync
* Local transactions are also stored in browser storage
* Google Apps Script deployment must remain active
* If Apps Script URL changes, update it in app settings

---

## 🌟 Future Improvements
Possible future upgrades:
* Category support
* Export to PDF
* Pie charts
* Search transactions
* Multi-user sync
* Authentication
* Budget goals
* Notifications
* Cloud backup

---

## Developer Credits

### Designed & Developed By
**Tarun Mhanta**

*Built with passion for productivity, finance tracking, and elegant UI experiences.*

### ❤️ Spendly
*Track smarter. Spend wiser.*
