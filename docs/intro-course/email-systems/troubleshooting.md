---
layout: default
title: Email Troubleshooting
nav_order: 2
parent: Email Systems
grand_parent: Introduction to Technology
permalink: /intro-course/email-systems/troubleshooting
---

# Email Troubleshooting
{: .no_toc }

A practical guide to diagnosing and fixing common email issues.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Common Email Problems

{% include callout.html type="important" title="Before You Start" content="Always verify your internet connection is working before troubleshooting email-specific issues." %}

### 1. Cannot Send Emails

**Symptoms:**
- "Message failed to send" errors
- Emails stuck in outbox
- SMTP connection errors

**Diagnostic Steps:**
```bash
# Check SMTP server availability
ping smtp.gmail.com

# Verify DNS resolution
nslookup smtp.gmail.com

# Test email server ports
telnet smtp.gmail.com 587
```
{: .code-example }

**Common Solutions:**
- Verify SMTP server settings
- Check username/password
- Confirm port numbers (25, 587, 465)
- Update SSL/TLS settings

### 2. Cannot Receive Emails

**Symptoms:**
- Missing expected emails
- Delayed reception
- Incomplete synchronization

**Diagnostic Steps:**
```bash
# Check mail server records
nslookup -type=mx yourdomain.com

# Verify server response
telnet pop.gmail.com 995
```
{: .code-example }

**Common Solutions:**
- Check POP3/IMAP settings
- Verify storage space
- Clear local cache
- Update email client

## Authentication Issues

{% include figure.html path="assets/Intro_course/images/Email-1.svg" class="img-fluid" alt="Email Authentication" caption="Email authentication process and potential failure points" %}

### 1. SPF Failures

**Check SPF Records:**
```bash
# View SPF record
nslookup -type=txt domain.com
```
{: .code-example }

**Common Issues:**
- Missing SPF record
- Incorrect server IP in record
- Syntax errors in SPF
- Too many DNS lookups

### 2. DKIM Problems

**Verify DKIM:**
- Check DKIM signature in headers
- Validate key rotation
- Confirm DNS records

{% include callout.html type="tip" title="DKIM Tip" content="Most email clients can show you the DKIM signature status in the email headers." %}

### 3. DMARC Issues

**Check DMARC Policy:**
```bash
# View DMARC record
nslookup -type=txt _dmarc.domain.com
```
{: .code-example }

**Troubleshooting Steps:**
1. Verify DMARC record exists
2. Check policy syntax
3. Review alignment with SPF/DKIM
4. Monitor DMARC reports

## Delivery Problems

### 1. Bounced Emails

**Types of Bounces:**
- Hard bounces (permanent)
- Soft bounces (temporary)
- Delayed delivery notices

**Common Causes:**
1. Invalid recipient address
2. Server rejection
3. Full mailbox
4. Policy violation

### 2. Spam Filter Issues

**If Emails Go to Spam:**
1. Check sender reputation
2. Review content for triggers
3. Verify authentication
4. Check IP blacklists

{% include callout.html type="warning" title="Blacklists" content="Being on an email blacklist can severely impact delivery. Regularly check your IP against major blacklists." %}

## Performance Issues

### 1. Slow Email Client

**Optimization Steps:**
1. Clear cache
2. Compact mailbox
3. Remove large attachments
4. Update client software

### 2. Synchronization Problems

**IMAP Troubleshooting:**
1. Check folder settings
2. Verify quota usage
3. Test connection speed
4. Reset sync state

## Advanced Diagnostics

### Reading Email Headers

```text
Received: from mail-yw1-f41.google.com
    by mx.domain.com with ESMTPS
    id ABC123; Thu, 23 Feb 2024
Authentication-Results: spf=pass dkim=pass
```
{: .code-example }

**Key Header Fields:**
- Received lines (trace route)
- Authentication results
- Message ID
- Date stamps

### Network Diagnostics

```bash
# Test email server connectivity
telnet smtp.gmail.com 587

# Check DNS resolution
dig +short mx gmail.com

# Verify reverse DNS
nslookup IP_ADDRESS
```
{: .code-example }

## Best Practices

### 1. Preventive Measures
- Regular backup of emails
- Update client software
- Monitor storage usage
- Check authentication setup

### 2. Security Practices
- Enable 2FA
- Use strong passwords
- Keep software updated
- Monitor for unusual activity

### 3. Maintenance Tasks
- Clean inbox regularly
- Archive old emails
- Update contact lists
- Check spam folder

## When to Seek Help

Contact your email provider or IT support when:
- Persistent authentication failures
- Systematic delivery problems
- Security compromises
- Complex configuration issues

{% include callout.html type="note" title="Documentation" content="Always document troubleshooting steps and results for future reference." %}

## Additional Resources

- Email protocol documentation
- Server configuration guides
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
- Authentication setup tutorials
