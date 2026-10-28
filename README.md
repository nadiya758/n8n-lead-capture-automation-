# AI-Powered Lead Capture Automation

An n8n automation project that captures leads from a form, validates email addresses, stores lead information in Airtable, generates personalized welcome emails with OpenAI, and sends notifications through Gmail and Slack.

## Business Problem

Businesses often manage incoming leads manually, which can lead to repetitive work, delayed follow-ups, and invalid email records.

## Solution

This workflow automates the lead-handling process from form submission to storage and notification.

## Workflow Architecture

```text
Lead Form Submission
        |
        v
   n8n Webhook
        |
        v
  Input Validation
        |
        v
   Email Validation
      /       \
   Valid      Invalid
     |           |
     v           v
  Airtable    Invalid Lead
     |         Handling
     v
 OpenAI Welcome Email
     |
     v
  Gmail Notification
     |
     v
  Slack Notification
```

*Update this diagram to match the actual node connections in your exported workflow.*

## Features

- Receives lead information through a form or webhook.
- Validates incoming data and handles invalid email addresses.
- Stores valid lead information in Airtable.
- Generates personalized welcome email content using OpenAI.
- Sends email notifications through Gmail.
- Sends lead notifications through Slack.
- Separates valid and invalid lead processing.

## Technology Stack

- **Automation:** n8n
- **AI:** OpenAI API
- **Database/CRM:** Airtable
- **Email:** Gmail
- **Team Notifications:** Slack
- **Input:** Form/Webhook

## Example Input

```json
{
  "name": "Demo User",
  "email": "demo@example.com",
  "interest": "AI Automation"
}
```

This is sample data for demonstration only.

## Expected Output

For a valid lead:

- The lead is processed by the workflow.
- Lead details are stored in Airtable.
- A personalized welcome email is generated.
- Configured email and Slack notifications are sent.

For an invalid email:

- The lead follows the invalid-data branch.
- The workflow handles the record according to the configured validation logic.

*Expected outputs must be verified against actual workflow executions.*


## Screenshots

### Workflow Overview
![Workflow Overview](./valid%20automation%20.png)

### Valid Email Automation
![Valid Email Automation](./Email.jpg)

### Email Output
![Email Output](./Email2.jpg)

### Invalid Email Handling
![Invalid Email Handling](./Invalid.png)


## Installation and Setup

1. Install or access an n8n instance.
2. Download the exported workflow JSON from this repository.
3. Import the JSON into n8n.
4. Configure the required credentials for OpenAI, Airtable, Gmail, and Slack.
5. Configure the webhook or form input.
6. Check the Airtable table and field mappings.
7. Run the workflow with test data.
8. Verify successful and invalid-input executions before using real leads.

## Testing Checklist

- [ ] Valid email is processed correctly.
- [ ] Invalid email follows the intended branch.
- [ ] Missing required fields are handled.
- [ ] Airtable receives the correct field values.
- [ ] AI generates suitable welcome email content.
- [ ] Gmail notification works.
- [ ] Slack notification works.
- [ ] API failures are handled safely.
- [ ] Duplicate submissions are tested.

## Demo Video

"▶ Watch n8n Lead Capture Automation Demo" https://drive.google.com/file/d/1neIXo03xCoL0qmKw2uBDhyCZkfy3jHT4/view?usp=drivesdk


The video should show the input submission, n8n execution, Airtable record, email output, and Slack notification.

## Security

- Never commit API keys, passwords, or access tokens.
- Configure credentials inside n8n.
- Use fictional data in public demonstrations.
- Protect production webhooks and restrict access where appropriate.

## Limitations

- Results depend on external API availability and configuration.
- AI-generated email content should be reviewed before production use.
- Email validation does not guarantee that an address exists or can receive messages.
- Error handling and duplicate prevention depend on the implemented workflow logic.

## Project Status

Status: Completed 

This repository is intended as a portfolio demonstration of workflow automation, API integration, AI-assisted communication, and lead management.

## Author

GitHub: [nadiya758](https://github.com/nadiya758)





