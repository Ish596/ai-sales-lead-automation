#  Sales Lead Automation

An n8n-based sales lead qualification and enrichment automation workflow designed to automate lead verification, customer classification, scoring, and reporting.

## Overview

This project automates the sales lead management process using n8n and multiple third-party integrations. It collects lead information, verifies email addresses, enriches company and person details, calculates lead scores, and categorizes leads based on predefined conditions.

## Features

- **Form Submission:** Collects customer and company information through an n8n form.
- **Email Validation:** Checks email format and verifies email deliverability using Hunter.io.
- **Lead Enrichment:** Retrieves available company and person information.
- **Customer Identification:** Identifies new and existing customers using Airtable.
- **Automated Lead Scoring:** Calculates scores based on customer type, country, and software industry.
- **Lead Classification:** Categorizes leads into Premium, Good, and Low Priority.
- **Google Sheets Integration:** Stores lead information and qualification results.
- **PDF Generation:** Creates personalized customer reports using Google Docs and Google Drive.
- **Email Automation:** Sends confirmation emails and approval requests through Gmail.
- **Slack Notifications:** Notifies relevant team members about qualified leads.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Hunter.io API | Email verification and enrichment |
| Airtable | Customer identification |
| Google Sheets | Lead data management |
| Google Docs | Customer report generation |
| Google Drive | PDF storage |
| Gmail | Email notifications and approvals |
| Slack | Team notifications |

## Lead Scoring Logic

The workflow calculates lead scores using three conditions:

| Condition | Score |
|---|---:|
| Existing customer | +1 |
| Target country (US, India, UK) | +1 |
| Software-based company | +1 |

### Lead Categories

- **Premium:** Score = 3
- **Good:** Score = 1 or 2
- **Low Priority:** Score = 0

New customers do not receive an automatic bonus.

## Workflow Process

1. Collect lead information through a form.
2. Validate the submitted email address.
3. Verify the email using Hunter.io.
4. Enrich available customer and company information.
5. Identify whether the customer is new or existing.
6. Calculate the lead score.
7. Categorize the lead based on its score.
8. Store relevant information in Google Sheets.
9. Generate customer reports and PDF documents.
10. Send notifications through Gmail and Slack.

## Project Structure

```text
ai-sales-lead-automation/
│
├── README.md
└── sales-lead-automation-workflow-sanitized.json
```

## Setup

1. Install or access n8n.
2. Import the workflow JSON file.
3. Configure the required credentials:
   - Hunter.io API
   - Google Sheets
   - Google Docs
   - Google Drive
   - Gmail
   - Airtable
   - Slack
4. Configure the required spreadsheet, document templates, and Airtable base.
5. Test the workflow with sample customer information.

## Project Status

Built as a personal automation project to explore workflow automation, API integrations, lead qualification, and business process automation.

**Note:** This repository contains a workflow export for demonstration and learning purposes. External service credentials and account configurations must be supplied separately.

## Author

**Ish Garg**

B.Tech Computer Science Engineering

Interested in AI, Generative AI, LLMs, and Workflow Automation.
