# Dues Reminder — AI-Powered Bill Tracker

An n8n automation that monitors unpaid bills and sends
smart email reminders with AI-generated finance tips.

## What it does

**Daily (7:20 AM):**
- Reads all bills from Google Sheets
- Filters unpaid ones (Paid? = No)
- Sends a reminder email listing each unpaid bill
- Google Gemini AI adds a personalised finance tip

**Weekly (Every Friday 7:20 AM):**
- Calculates total spending across all bills
- Sends a weekly spending summary email

## Workflow preview
![Workflow preview](https://github.com/uzairio/n8n-dues-reminder/blob/main/Dues%20Reminder%20preview%20(n8n).png)

## Tools used
- n8n (automation platform)
- Google Sheets (bill data source)
- Gmail (email notifications)
- Google Gemini AI (finance tips via LangChain)

## Sheet structure required
| Column | Description |
|---|---|
| Bill Name | Name of the bill |
| Amount | Bill amount (number) |
| Due Date | When payment is due |
| Category | Bill category |
| Paid? | Yes or No |

## How to import
1. Download `DUES_REMINDER.json`
2. In n8n: New Workflow → Import from file
3. Connect Google Sheets and Gmail credentials
4. Set your Google Gemini API key
5. Update the spreadsheet ID to point to your sheet
6. Activate both schedule triggers

## Status
This project is a work in progress and is being improved step by step.
