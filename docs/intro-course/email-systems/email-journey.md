---
layout: default
title: Email Journey
nav_order: 1
parent: Email Systems
grand_parent: Introduction to Technology
permalink: /intro-course/email-systems/email-journey
---

# The Journey of an Email
{: .no_toc }

Following an email's path from sender to recipient.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Overview

When you click "Send" on an email, it triggers a complex journey involving multiple servers, protocols, and security checks before reaching its destination.

{% include figure.html path="assets/Intro_course/images/EmailFlow.svg" class="img-fluid" alt="Email Journey Flow" caption="The complete journey of an email from sender to recipient" %}

{% include callout.html type="note" title="Key Concept" content="Email delivery relies heavily on DNS, specifically MX records, to determine where to deliver messages." %}

## Step-by-Step Journey

### 1. Composition and Initial Send

When you compose and send an email:
- Your email client formats the message
- Attachments are encoded
- Headers are added (From, To, Subject, etc.)

{% include callout.html type="tip" title="Email Headers" content="Headers contain important routing information and metadata about the email's journey." %}

### 2. SMTP Server Connection

Your email client connects to its SMTP server:
```bash
# Example SMTP connection process
220 smtp.gmail.com ESMTP ready
HELO client.example.com
250 Hello client.example.com
MAIL FROM: <sender@example.com>
250 Sender OK
RCPT TO: <recipient@domain.com>
250 Recipient OK
DATA
354 Start mail input
```
{: .code-example }

### 3. DNS Lookup Process

The SMTP server performs several DNS lookups:

1. **MX Record Lookup**
```bash
# Check MX records
nslookup -type=mx recipient-domain.com
```
{: .code-example }

2. **Authentication Records**
```bash
# Check SPF and DKIM records
nslookup -type=txt recipient-domain.com
```
{: .code-example }

{% include callout.html type="important" title="MX Records" content="MX (Mail Exchange) records tell email servers which mail servers are responsible for accepting email for a domain." %}

### 4. Email Authentication

{% include figure.html path="assets/Intro_course/images/Email-1.svg" class="img-fluid" alt="Email Authentication" caption="Email authentication and security checks" %}

Multiple authentication methods work together:

1. **SPF (Sender Policy Framework)**
   - Verifies sending server is authorized
   - Prevents email spoofing
   - Uses DNS TXT records

2. **DKIM (DomainKeys Identified Mail)**
   - Adds digital signature
   - Ensures email hasn't been modified
   - Verifies sender domain

3. **DMARC (Domain-based Message Authentication)**
   - Combines SPF and DKIM
   - Sets handling policy for failures
   - Reports authentication results

### 5. Server-to-Server Transfer

Once authenticated:
- Sending server establishes connection
- Messages transferred via SMTP
- Multiple hops may occur
- Progress tracked in headers

### 6. Recipient Server Processing

The receiving mail server:
1. Accepts the incoming connection
2. Performs security checks
3. Scans for malware
4. Applies spam filtering
5. Stores message for retrieval

### 7. Final Delivery

Recipients can access their email through:
- **POP3**: Downloads and typically deletes from server
- **IMAP**: Syncs across devices, keeps on server
- **Web Interface**: Direct server access

## Examining Email Headers

Email headers reveal the journey:

```text
Received: from mail-yw1-f41.google.com
Received: from smtp.gmail.com
Authentication-Results: spf=pass dkim=pass
```
{: .code-example }

{% include callout.html type="tip" title="View Headers" content="Most email clients let you view complete headers through a 'Show Original' or similar option." %}

## Common Delivery Issues

### 1. Bounced Emails
- Invalid recipient address
- Server rejection
- Mailbox full
- Network issues

### 2. Delayed Delivery
- Server congestion
- Greylisting
- Rate limiting
- DNS issues

### 3. Authentication Failures
- SPF record mismatch
- DKIM signature failure
- Missing DMARC policy

## Best Practices for Reliable Delivery

1. **Sender Configuration**
   - Proper DNS records
   - Valid reverse DNS
   - Updated SSL/TLS certificates

2. **Content Guidelines**
   - Avoid spam triggers
   - Proper formatting
   - Reasonable attachment sizes

3. **Server Maintenance**
   - Regular updates
   - Monitor blacklists
   - Keep logs for troubleshooting

## Next Steps

Continue to [Email Troubleshooting](troubleshooting) to learn how to diagnose and fix common email issues.

## Additional Resources

- Email protocol specifications
- Authentication setup guides
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
