# SmartSpend – Smart Daily Spending Tracker

**Project Better Tomorrow**

> “Track today. Spend smarter tomorrow.”

[![Deploy to GitHub Pages](https://github.com/YOUR-USERNAME/YOUR-REPOSITORY/actions/workflows/deploy.yml/badge.svg)](https://github.com/YOUR-USERNAME/YOUR-REPOSITORY/actions/workflows/deploy.yml)

### Live Demo
👉 **[https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/](https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/)**

---

## 1. Project Overview

**SmartSpend** is a complete, modern, responsive financial habit and expense-tracking static web application created specifically for the **Project Better Tomorrow** university assignment.

Engineered with a student-first philosophy, SmartSpend empowers young adults living independently to effortlessly record daily micro-expenses, maintain a disciplined monthly budget, visualize expenditure habits with interactive charts, and build sustainable savings goals—all completely client-side with 100% privacy preservation.

---

## 2. Problem Statement

University students and young professionals transitioning to independent hostel or apartment living frequently experience significant financial friction:
* **The "Month-End" Crisis**: Spending allowances rapidly in the first 10–15 days, resulting in borrowing or skipped meals.
* **Invisible Micro-Expenses**: Routine campus canteen snacks, tea, photocopying fees, and short auto-rickshaw rides slip by unmonitored yet consume 30%–50% of the monthly allowance.
* **Complex Financial Tools**: Existing banking apps and enterprise finance software demand sensitive bank credentials, SMS permissions, investment profiles, and complex setups inappropriate for student budgets.
* **Absence of Guardrails**: Students lack immediate, practical feedback answering: *"How much can I safely spend today?"*

---

## 3. Proposed Solution

SmartSpend directly solves student budgeting through an intuitive, lightweight, and completely private web platform:
* **Safe Daily Spend Engine**: Calculates remaining budget divided by the exact days left in the month to provide an immediate daily spending cap.
* **₹ (Indian Rupee) Native**: Standard Indian Rupee formatting (`₹`) with student-focused categories (Food, Transport, Shopping, Education, Entertainment, Bills, Health, Other) and Indian payment modes (UPI, Cash, Debit Card, Credit Card, Other).
* **Proactive Warning Tiers**: Dynamic visual progress meter alerting students at **80% (Warning)** and **100% (Budget Exceeded)** thresholds.
* **Rule-Based Smart Insights**: Automated pattern recognition identifying top categories, weekend spending spikes, and practical saving opportunities without offering speculative investment advice.
* **Zero-Setup Static Architecture**: Runs immediately in any browser with zero backend requirements, zero tracking, and complete offline persistence via browser `localStorage`.

---

## 4. Objectives

1. **Promote Financial Mindfulness**: Help students develop conscious spending habits through low-friction daily tracking.
2. **Prevent Debt & Overspending**: Provide real-time safe spending limits to eliminate month-end financial strain.
3. **Data Privacy by Design**: Eliminate account logins, passwords, cloud databases, and third-party trackers by keeping all records strictly on the student's device.
4. **Demonstration Excellence**: Supply a feature-complete, interactive experience with realistic demo data, automated Chart.js visualizations, and a responsive UI ready for academic assessment.

---

## 5. Features

### 5.1 Dashboard
* **Real-Time KPI Cards**: Today's Spending, This Week's Spending, This Month's Spending, Remaining Budget, and Total Transactions.
* **Safe-to-Spend Allowance**: Dynamic safe daily spending indicator.
* **Dynamic Budget Alert Banner**: Alerts user when spending reaches 80% or 100% of the monthly budget.
* **Recent Transactions List**: Quick preview of the 5 most recent transactions with one-click edit and delete actions.

### 5.2 Add Expense (Dedicated View & Modal)
* Inputs: Amount in **₹**, Category, Date, Payment Method, Description.
* **8 Categories**: Food, Transport, Shopping, Education, Entertainment, Bills, Health, Other.
* **5 Payment Methods**: Cash, UPI, Debit Card, Credit Card, Other.
* **Quick Preset Chips**: Quick addition buttons (+₹50, +₹100, +₹200, +₹500, +₹1,000) for rapid logging.
* Client-side validation preventing negative or zero inputs.

### 5.3 Transactions History & Filter Engine
* **Table View**: Date | Category | Description | Payment Method | Amount (₹) | Actions.
* **Live Search**: Instant multi-field searching across descriptions, categories, payment methods, and amounts.
* **Filters**: By Category, by Payment Method, and by Date Range (All, Today, This Week, This Month, Custom Date Range).
* **Sorting**: Date (newest/oldest) and Amount (highest/lowest).
* **CRUD Controls**: Full Create, Read, Update, and Delete capabilities with modal confirmation.
* **Data Portability**: One-click RFC-compliant CSV and JSON data export.

### 5.4 Budget Management
* Configurable monthly spending budget.
* Visual progress bar with dynamic color transitions:
  * 🟢 **Green** (`<70%`): Safe
  * 🟡 **Amber** (`70%–89%`): 80% Warning Limit
  * 🔴 **Red** (`≥90%`): Budget Exceeded Alert
* Comprehensive category distribution breakdown table.

### 5.5 Spending Analytics (Chart.js)
* **Spending by Category**: Doughnut Chart showing percentage and rupee share.
* **Daily Spending**: Bar Chart tracking daily expenditures over the past 14 days.
* **Weekly Spending**: Line Chart depicting spending pace across the month's weeks.
* **Monthly Spending**: Bar Chart tracking month-by-month spending progression.
* Auto-updates dynamically whenever any expense is added, edited, or deleted.

### 5.6 Smart Insights (Rule-Based Heuristics)
* Dynamic rule-based evaluations derived strictly from user records:
  * *"Food is your highest spending category this month."*
  * *"You have used 75% of your monthly budget."*
  * *"Your spending increased compared with last week."*
  * *"Shopping is becoming one of your highest spending categories."*
  * *"Consider setting a weekly spending limit."*
* Strictly rule-based; avoids financial or investment advice.

### 5.7 Savings Goals
* Create student savings goals: Goal Name, Target Amount (₹), Current Saved Amount (₹), Target Date.
* Visual animated progress bar, percentage completion, and days remaining countdown.
* Interactive **+ Add / - Withdraw Funds** drawer.
* Goal completion celebration badge upon hitting 100%.

### 5.8 SmartSpend Assistant
* Interactive student spending helper.
* Instant query pills (*"How is my budget pacing?"*, *"What is my highest category?"*, *"Can I spend ₹300 today?"*, *"Tips to save money"*).
* Natural-language query search bar delivering real-time heuristic advice based on recorded expenses.

### 5.9 UI & Themes
* Premium Dark/Light mode with instant persistence in `localStorage`.
* Fully responsive desktop sidebar, mobile top bar, and mobile bottom navigation.
* Clean Google typography (*Plus Jakarta Sans* & *Inter*), Font Awesome icons, and custom SVG wallet/rupee branding.

---

## 6. Technology Used

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Markup** | HTML5 | Semantic SPA structure, accessible ARIA dialogs |
| **Styling** | CSS3 | CSS Variables, Flexbox, Grid, Dark/Light theme tokens |
| **Logic** | Vanilla JavaScript (ES6+) | State management, CRUD, heuristics, router |
| **Charts** | Chart.js (v4.4 via CDN) | Hardware-accelerated Doughnut, Bar, and Line charts |
| **Storage** | Browser `localStorage` | Client-side persistence without a server |
| **Icons** | Font Awesome 6 (CDN) | Modern category and navigation icons |
| **Typography**| Google Fonts | Plus Jakarta Sans & Inter font families |
| **CI/CD** | GitHub Actions | Automated zero-touch deployment to GitHub Pages |

---

## 7. How It Works

```
┌─────────────────────────────────────────────────────────────┐
│                        User Browser                         │
│                                                             │
│   ┌───────────────┐   ┌────────────────┐   ┌────────────┐   │
│   │  index.html   │   │   style.css    │   │ script.js  │   │
│   │ Semantic SPA  │   │ Responsive UI  │   │ Logic/CRUD │   │
│   └───────┬───────┘   └───────┬────────┘   └─────┬──────┘   │
│           │                   │                  │          │
│           ▼                   ▼                  ▼          │
│   ┌─────────────────────────────────────────────────────┐   │
│   │                 Chart.js Rendering                  │   │
│   │       Doughnut • Bar • Line Visual Analytics        │   │
│   └───────────────────────────┬─────────────────────────┘   │
│                               │                             │
│                               ▼                             │
│   ┌─────────────────────────────────────────────────────┐   │
│   │                Browser localStorage                 │   │
│   │      Key: smartspend_data_v1 (Persistent)           │   │
│   └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

1. **Loading**: When `index.html` loads, `script.js` checks `localStorage.getItem('smartspend_data_v1')`. If empty, it loads pre-populated student demo transactions.
2. **Reactivity**: Adding, editing, or deleting an expense triggers an instant reactive cascade:
   * Saves updated state to `localStorage`.
   * Recalculates KPIs (Today, Week, Month, Budget Remaining, Safe Daily Spend).
   * Destroys and redraws Chart.js instances to reflect new balances.
   * Updates heuristic Smart Insights and Assistant suggestions.
3. **Routing**: A lightweight hash router (`#dashboard`, `#transactions`, `#budget`, `#analytics`, `#insights`, `#savings`, `#assistant`, `#settings`) provides seamless SPA navigation without page refreshes.

---

## 8. localStorage

All data is stored client-side under the key `smartspend_data_v1`:

```json
{
  "settings": {
    "currency": "₹",
    "theme": "dark",
    "monthlyBudget": 12000
  },
  "expenses": [
    {
      "id": "exp_1726378490000_1",
      "amount": 85,
      "category": "Food",
      "date": "2026-09-15",
      "paymentMethod": "UPI",
      "description": "Campus Canteen Masala Dosa & Tea"
    }
  ],
  "savingsGoals": [
    {
      "id": "goal_1",
      "name": "Coding Laptop Upgrade",
      "targetAmount": 45000,
      "currentAmount": 22500,
      "targetDate": "2026-12-15"
    }
  ]
}
```

* **Persistence**: Data survives page reloads, browser restarts, and device reboots.
* **Demo Data Button**: Located in Settings to reload realistic sample transactions during presentations.
* **Backup & Restore**: Export complete data as `.json` and restore anytime.

---

## 9. GitHub Pages Deployment

SmartSpend is 100% static, uses relative paths (`./`), contains a `.nojekyll` file, and includes an official **GitHub Actions** deployment workflow (`.github/workflows/deploy.yml`).

### Step-by-Step Publishing:

#### 1. Push Code to GitHub
Run in your project root:
```bash
git init
git add .
git commit -m "Initial commit - SmartSpend Daily Spending Tracker"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

#### 2. Enable GitHub Pages
1. Go to your GitHub repository: `https://github.com/YOUR-USERNAME/YOUR-REPOSITORY`
2. Click **Settings** → **Pages** (in the left sidebar under *Code and automation*).
3. Under **Build and deployment** → **Source**:
   * Choose **GitHub Actions** (the workflow `.github/workflows/deploy.yml` will automatically build and deploy the site on every push).
   * *Alternatively*, choose **Deploy from a branch** → select `main` and `/(root)` → click **Save**.
4. Within 60 seconds, your site will be live at:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/
   ```

---

## 10. Future Enhancements

* **Receipt OCR Scanner**: Capture photos of campus canteen receipts to extract amounts automatically.
* **PDF Monthly Report**: Download printable, parent-friendly financial summaries at month-end.
* **Hostel Bill Splitter**: Shared expense splitting calculator for roommates and group dinners.
* **Multi-Currency Toggle**: Expand beyond ₹ (INR) to support USD, EUR, and GBP for international students.

---

**Project Better Tomorrow** • *Track today. Spend smarter tomorrow.*
