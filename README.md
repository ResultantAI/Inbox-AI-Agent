# Inbox AI Agent

> **Never miss a follow-up. Inbox Agent monitors your Gmail, flags priority messages, auto-creates Airtable tasks, and pings you on Slack.**

## Features
- Monitors Gmail (chris@resultantai.com) for high-priority/lead messages
- Triggers on custom keywords: proposal, contract, urgent, demo, invoice, payment, signed
- Auto-creates follow-up tasks in Airtable: [Inbox AI Tasks](https://airtable.com/appPDEooFIkfpN08M/shr21qPF6nAqO5nsh)
- Sends Slack notification for each flagged/urgent email
- (Optional) Drafts replies using your templates
- Daily summary of new leads and priority tasks (Slack/email)

## How It Works
1. Checks Gmail inbox every 10 minutes for new messages.
2. Flags any email with subject or body matching trigger keywords.
3. For each flagged email:
    - Creates a task in Airtable (contact, subject, deadline, priority, link)
    - Sends a Slack notification with summary and direct email link
    - (Optional) Drafts a reply from your saved template
4. Sends a daily summary to Slack at 5pm.

## Integration
- Gmail: chris@resultantai.com (OAuth or Zapier/Make)
- Airtable: [Inbox AI Tasks](https://airtable.com/appPDEooFIkfpN08M/shr21qPF6nAqO5nsh)
- Slack: Direct message or channel #notifications
- Templates and trigger keywords in `/templates` and `/triggers`

## Quickstart (No Code)
1. Set up a Zapier/Make.com scenario:
    - Trigger: Gmail → Search for trigger keywords
    - Action: Create record in Airtable
    - Action: Send Slack notification
    - (Optional): Draft reply in Gmail from template
2. Add or update trigger keywords and templates as needed.

## See `/integration-notes.md` for detailed step-by-step setup.

---
