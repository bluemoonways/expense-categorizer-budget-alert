# 💰 Expense Categorizer & Budget Alert

An AI-powered personal finance automation built with **n8n** that automatically categorizes expenses, determines whether spending is a **Need or Want**, stores the data in Google Sheets, calculates monthly spending, and sends an email alert when a category exceeds its budget.

## 🚀 Project Overview

Managing expenses manually can be time-consuming, and people often realize they have overspent only after the month is over.

This automation provides an early warning system by combining **AI classification, data storage, JavaScript calculations, conditional logic, and email notifications**.

## 📋 Problem Statement

For a detailed explanation of the business problem, pain points, project goal, and proposed automation:

👉 [View Problem Statement](https://bluemoonways.github.io/expense-categorizer-budget-alert/)

## 🔄 Workflow Chart

![Expense Categorizer & Budget Alert Workflow](screenshots/Workflow%20Chart.png)

## ✨ Key Features

* 📝 Collect expenses through an n8n form
* 🤖 Automatically categorize expenses using Google Gemini AI
* 🏷️ Classify spending as **Need** or **Want**
* 📊 Store categorized expenses in Google Sheets
* 🧮 Calculate total monthly spending by category
* 💰 Compare spending against predefined monthly budgets
* 🚨 Detect when a category exceeds its budget
* 📧 Send a professional Gmail budget alert automatically

The workflow's form collects expense details including description, amount, currency, date and email.

## 🧠 AI Classification

The AI agent categorizes each expense using predefined categories and determines whether the expense is a **Need** or **Want**.

The workflow uses structured output containing:

```json
{
  "category": "Food & Dining",
  "essential": "Want",
  "note": "Restaurant meal classified as discretionary spending."
}
```

This structured output is then stored in Google Sheets along with the original expense information.

## 💵 Default Monthly Budgets

| Category          |     Budget |
| ----------------- | ---------: |
| Food & Dining     | PKR 30,000 |
| Transport         | PKR 15,000 |
| Utilities & Bills | PKR 25,000 |
| Shopping          | PKR 20,000 |
| Entertainment     | PKR 10,000 |
| Health            | PKR 15,000 |
| Other             | PKR 10,000 |

These budget values can be modified directly in the JavaScript Code node.

## 🛠️ Technologies Used

* **n8n**
* **Google Gemini AI**
* **Google Sheets**
* **JavaScript**
* **Gmail**
* **HTML Email**
* **Conditional / IF Logic**
* **Structured AI Output**

## 📊 Budget Detection

After the expense is added to Google Sheets, the workflow reads the stored expenses and calculates the current month's spending for the relevant category.

JavaScript then determines:

* Total amount spent
* Monthly budget
* Remaining budget
* Whether the budget has been exceeded

If the category is over budget, the IF node triggers the Gmail notification.

## 🚨 Email Alert

When a budget is exceeded, the workflow automatically sends a professionally formatted Gmail alert showing:

* Expense category
* Monthly budget
* Total spent
* Remaining budget
* Spending recommendation

## 🎯 Business Value

This automation helps users:

* Understand where their money is going
* Reduce manual expense categorization
* Identify unnecessary spending
* Receive early budget warnings
* Make better financial decisions

The core idea is **AI + real data + calculations + business logic + automated notification** rather than simply using AI for text generation.

## 🔮 Possible Improvements

Future versions could include:

* 📅 Monthly spending summary using Schedule Trigger
* 📂 Bulk transaction import from bank CSV
* ⚠️ 80% budget warning before the limit is reached
* 📈 Expense dashboard
* 📊 Spending trends and analytics
* 🔔 Multiple notification channels

## 📁 Workflow File

You can view and download the complete n8n workflow here:

👉 [View n8n Workflow JSON](Expense_Categorizer_Budget.json)

## 👨‍💻 Author

**Faheem Abbas**

AI Automation & n8n Projects

---

### #n8n #AIAutomation #GoogleSheets #JavaScript #GeminiAI #Gmail #WorkflowAutomation
