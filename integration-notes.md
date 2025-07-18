# Inbox AI Agent Integration Notes

## 1. Gmail → Airtable
- Use [Zapier](https://zapier.com/) or [Make.com](https://make.com/) to set up:
    - **Trigger:** New Gmail matching keywords (see `/triggers/trigger-keywords.txt`)
    - **Action:** Create a record in Airtable [Inbox AI Tasks](https://airtable.com/appPDEooFIkfpN08M/shr21qPF6nAqO5nsh)
        - Map: Name, Email, Subject, Deadline, Priority, Email Link, Status

## 2. Airtable → Slack
- Add another Zapier/Make.com step:
    - **Trigger:** New record in Airtable (priority = High or keyword match)
    - **Action:** Send Slack notification to your DM or channel #notifications
        - Example: “New High-Priority Lead: Jane Doe (Proposal signed)”

## 3. Draft Gmail Replies (Optional)
- In Zapier/Make, use the “Send Draft” or “Reply” step
- Pull reply text from `/templates/reply-thank-you.txt` or `/reply-generic-followup.txt`
- Personalize with merge fields (e.g., [Name], [Date])

## 4. Daily Summary (Optional)
- Use “Digest” or “Summary” in Zapier/Make.com
- At 5pm daily, send summary of tasks created to Slack (see `/examples/sample-daily-summary.txt`)

## 5. Customize
- Add or edit keywords in `/triggers/trigger-keywords.txt`
- Add new reply templates to `/templates`
- Update Airtable fields as your workflow grows

## 6. Security
- Use OAuth where possible, or set up app-specific passwords
- Share access only with trusted VAs/team
