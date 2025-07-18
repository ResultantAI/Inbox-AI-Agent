# Inbox AI Agent

**Purpose:**  
Never miss a follow-up or critical client message. Inbox Agent monitors your email, flags high-priority messages, auto-creates follow-up tasks in Airtable, and sends a daily summary.

## Workflow Steps
1. Check Gmail inbox every 10 minutes for new messages
2. If subject or body matches trigger keywords (“proposal,” “signed,” “ready to start”), flag message
3. Create a new task in Airtable:  
   - Contact name  
   - Email  
   - Message subject  
   - Deadline (if present, or 48hr default)
   - Priority (high/medium/low)
   - Link to email
4. (Optional) Draft a thank-you or confirmation reply using templates
5. (Optional) Send daily Slack/Email summary at 5pm

## Required
- Gmail access (OAuth or app password)
- Airtable base with fields: Name, Email, Subject, Deadline, Priority, Email Link, Status
- List of trigger keywords
- Reply templates (in /templates)

## Example Output
**Airtable Task:**  
| Name      | Email             | Subject          | Deadline    | Priority | Link     |  
|-----------|-------------------|------------------|-------------|----------|----------|  
| Jane Doe  | jane@client.com   | Proposal signed  | 2025-07-18  | High     | [email]  |  
