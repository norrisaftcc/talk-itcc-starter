# IOC Notes: Reported Phishing Email

Purpose: a template to log indicators of compromise (IOCs) from one phishing report.

Do not click links or open attachments. Copy values from the headers or a report only.
Write domains in a safe form so they do not become live links: `example[.]com`.

- Ticket number: [ticket]
- Date reported: [date]
- Reported by: [role only, for example "staff user". No names.]

| Type          | Value                             | Where found        |
|---------------|-----------------------------------|--------------------|
| Sender        | alerts@login-verify[.]example[.]com | From header      |
| Reply-To      | help-desk@example[.]org           | Reply-To header    |
| Sending IP    | 192.0.2.45                        | Email headers      |
| Link domain   | portal.example[.]net              | Body link          |
| Linked IP     | 198.51.100.23                     | DNS lookup         |
| Attachment    | invoice.zip (not opened)          | Attachment name    |

- SPF / DKIM / DMARC: [pass / fail / none]
- Decision: [phishing / spam / legitimate / unsure]
- Sent to security team: [yes / no, date]
