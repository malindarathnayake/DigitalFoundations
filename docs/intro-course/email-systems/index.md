---
layout: default
title: Email Systems
nav_order: 3
parent: Introduction to Technology
has_children: true
permalink: /intro-course/email-systems
---

# How Email Works
{: .no_toc }

Understanding the complete journey of an email from sender to recipient.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction to Email Systems

Email is one of the most widely used communication tools in the world. Understanding how it works helps you:
- Troubleshoot email issues
- Protect against email threats
- Make informed decisions about email services

{% include figure.html path="assets/Intro_course/images/EmailFlow.svg" class="img-fluid" alt="Email System Overview" caption="Overview of how email systems work" %}

{% include callout.html type="important" title="Key Concept" content="Email relies on multiple protocols and servers working together to deliver messages securely across the internet." %}

## What Happens When You Send an Email?

When you click "Send" in your email client, a complex series of steps begins:

1. **Your Email Client** connects to an SMTP (Simple Mail Transfer Protocol) server
2. **SMTP Server** accepts your email and prepares to relay it
3. **DNS Lookup** is performed to find the recipient's mail server
4. **MX Records** are retrieved, indicating which mail servers handle email for the recipient's domain
5. **Email Delivery** to the recipient's mail server
6. **Recipient Retrieval** when they check their inbox

{% include callout.html type="note" title="SMTP Fundamentals" content="SMTP (Simple Mail Transfer Protocol) is the standard protocol for sending email across the internet. It defines how email messages are transmitted between servers." %}

## Key Components

### 1. Email Clients
- **Desktop applications**: Outlook, Thunderbird, Apple Mail
- **Web-based clients**: Gmail, Yahoo Mail, Outlook.com
- **Mobile apps**: iOS Mail, Gmail app, Outlook mobile

### 2. Email Servers
- **SMTP servers** for sending outgoing mail
- **POP3/IMAP servers** for retrieving incoming mail
- **Email storage systems** for maintaining your inbox

### 3. Protocols
- **SMTP** (Simple Mail Transfer Protocol): For sending email
- **POP3** (Post Office Protocol): For downloading email to a single device
- **IMAP** (Internet Message Access Protocol): For syncing email across multiple devices

{% include callout.html type="tip" title="Protocol Choice" content="IMAP is generally preferred over POP3 as it keeps emails synchronized across multiple devices, while POP3 typically downloads and removes emails from the server." %}

## Email Journey Diagram

{% include figure.html path="assets/Intro_course/images/EmailJourneyDetailed.svg" class="img-fluid" alt="Email Journey" caption="Detailed view of an email's journey from sender to recipient" %}

## MX Records and DNS

MX (Mail Exchange) records are a type of DNS record that specifies which mail servers are responsible for accepting email for a domain.

### How MX Records Work:
1. When an email is sent to user@example.com, the sending server performs a DNS lookup
2. It specifically requests the MX records for example.com
3. DNS returns a list of mail servers and their priorities
4. The sending server attempts delivery to the highest priority server first

## Email Authentication

{% include figure.html path="assets/Intro_course/images/Email-1.svg" class="img-fluid" alt="Email Security" caption="Email security and authentication flow" %}

### Authentication Methods
- **SPF** (Sender Policy Framework): Verifies that sending servers are authorized
- **DKIM** (DomainKeys Identified Mail): Adds a digital signature to verify the message hasn't been altered
- **DMARC** (Domain-based Message Authentication): Combines SPF and DKIM with reporting

### Common Email Threats
- Phishing attempts
- Spam and unwanted messages
- Malware attachments
- Email spoofing and impersonation

{% include callout.html type="warning" title="Security Alert" content="Always verify unexpected emails, especially those requesting sensitive information or containing attachments." %}

## Hands-On Demonstration: MX Record Lookup

Let's try a simple command to see the mail servers for a domain:

```bash
nslookup -type=MX gmail.com
```
{: .code-example }

This command shows:
- The mail servers that handle email for gmail.com
- Their priority values (lower numbers = higher priority)
- The fully qualified domain names of the mail servers

### Sample Output:

```
gmail.com	mail exchanger = 10 alt1.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 20 alt2.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 30 alt3.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 40 alt4.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 5 gmail-smtp-in.l.google.com.
```

{% include callout.html type="tip" title="Try It Yourself" content="Open your computer's terminal or command prompt and try looking up MX records for different email domains to see how they're configured." %}

## Optional: Email Authentication Check

You can also check a domain's SPF record:

```bash
nslookup -type=TXT gmail.com
```
{: .code-example }

This shows the TXT records for the domain, which include SPF information that helps validate email sources.

[Learn more about the Email Journey](email-journey){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

## Common Email Issues and Troubleshooting

Various issues can affect email service:
- **Sending problems**: SMTP server issues, authentication failures
- **Receiving problems**: Full mailbox, server downtime, filtering
- **Authentication failures**: Incorrect credentials, security blocks
- **Delivery delays**: Server congestion, greylisting, routing issues

[View Troubleshooting Guide](troubleshooting){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

## Mini Troubleshooting Activity

### Scenario: Your emails aren't being delivered

**Steps to diagnose:**
1. Check your internet connection
2. Verify your SMTP server settings
3. Look up the recipient domain's MX records
4. Check if your domain has proper SPF records
5. Test with a different recipient or email service

**Try this command to check if the recipient's mail servers are accessible:**
```bash
ping alt1.gmail-smtp-in.l.google.com
```
{: .code-example }

## Email Best Practices

### 1. Email Management
- Regular inbox cleanup and organization
- Create folders for important categories
- Archive rather than delete when possible
- Use filters and rules to automate sorting

### 2. Security Practices
- Use strong, unique passwords for email accounts
- Enable two-factor authentication
- Be cautious with attachments and links
- Regularly update email clients and security software

### 3. Professional Usage
- Write clear, concise subject lines
- Use professional formatting and signatures
- Respond in a timely manner
- Double-check recipients before sending sensitive information

## Next Steps

1. Explore the detailed [Email Journey](email-journey) to understand each step in depth
2. Learn about [Email Troubleshooting](troubleshooting) techniques
3. Practice the hands-on exercises with different domains
4. Try setting up email forwarding or filters in your own account

## Additional Resources

- [Email Security Best Practices](/intro-course/resources/email-security)
- [Common Email Commands](/intro-course/resources/commands#email)
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
- [Email Protocol Specifications](/intro-course/resources/email-protocols)
