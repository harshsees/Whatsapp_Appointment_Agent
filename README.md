# WhatsApp Appointment Booking AI Agent using n8n

An automated appointment booking workflow built with n8n, WhatsApp Business API, OpenAI, Google Sheets, and Gmail. The workflow acts as a WhatsApp-based AI assistant that talks to customers, checks lead details, books appointments, stores records, and sends confirmation messages.

## Project Overview

This project automates the appointment booking process through WhatsApp. When a customer sends a message, the workflow triggers an AI agent that can understand the request, collect appointment details, check or update lead data, and confirm the booking through WhatsApp and email.

The workflow is designed for businesses that want to reduce manual follow-ups, manage leads more efficiently, and provide faster appointment scheduling support.

## Key Features

- WhatsApp message trigger using WhatsApp Business API
- AI-powered appointment booking assistant using OpenAI GPT-4o
- Conversation memory for handling follow-up messages in context
- Lead lookup and appointment storage using Google Sheets
- Knowledge base search for service details, pricing, availability, FAQs, and business information
- Automated WhatsApp replies after customer interaction
- Gmail confirmation email after successful appointment booking
- JSON-based data handling for phone number, name, email, appointment date, and service type

## Workflow Integrations

The n8n workflow uses the following services:

- n8n
- WhatsApp Business API
- OpenAI API
- Google Sheets API
- Gmail API
- LangChain AI Agent node in n8n
- Window Buffer Memory node in n8n

## How The Workflow Works

1. A customer sends a WhatsApp message.
2. The WhatsApp Trigger node receives the message.
3. The AI Agent processes the message using OpenAI GPT-4o.
4. The agent checks whether the customer is a new or existing lead.
5. The agent searches the knowledge base for company information and available appointment details.
6. The workflow saves or updates lead and appointment information in Google Sheets.
7. The workflow sends a WhatsApp reply confirming the next step or appointment details.
8. If the customer provides an email address, Gmail sends a confirmation email.

## Requirements

Before importing and running this workflow, make sure you have:

- An active n8n account or self-hosted n8n instance
- WhatsApp Business API access
- OpenAI API key
- Google account with access to Google Sheets and Gmail
- Google Sheets OAuth2 credentials configured in n8n
- Gmail OAuth2 credentials configured in n8n
- A Google Sheet with columns similar to:
  - Phone
  - Name
  - Email
  - AppointmentDate
  - ServiceType
  - Status
  - LastUpdated
- A knowledge base workflow or connected data source for service details, pricing, business hours, FAQs, and appointment slots

## Suggested Google Sheet Format

| Phone | Name | Email | AppointmentDate | ServiceType | Status | LastUpdated |
| --- | --- | --- | --- | --- | --- | --- |
| Customer WhatsApp number | Customer name | Customer email | Appointment date and time | Requested service | Booked/Pending | ISO timestamp |

## Import Instructions

1. Open your n8n dashboard.
2. Create a new workflow.
3. Import the workflow JSON file:
   - `whatsapp_app_setter.json`
4. Replace placeholder credential IDs with your own n8n credentials.
5. Replace `YOUR_GOOGLE_SHEET_ID_HERE` with your actual Google Sheet ID.
6. Configure the WhatsApp webhook in your WhatsApp Business API settings.
7. Test the workflow by sending a WhatsApp message to the connected business number.
8. Confirm that lead data is saved in Google Sheets and appointment emails are sent through Gmail.


## Author

Harsh Shah

- GitHub: https://github.com/harshsees
- LinkedIn: http://www.linkedin.com/in/harsh-shah-aa9228244
