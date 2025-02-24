---
layout: default
title: DNS Basics
nav_order: 1
parent: Networking
grand_parent: Introduction to Technology
permalink: /intro-course/networking/dns-basics
---

# DNS Basics
{: .no_toc }

Understanding the Domain Name System and how it powers internet navigation.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is DNS?

DNS (Domain Name System) acts like the internet's phone book, translating human-readable domain names (like www.google.com) into IP addresses (like 142.250.190.78) that computers use to identify each other.

{% include figure.html path="assets/Intro_course/images/DNS_Flow.svg" class="img-fluid" alt="DNS Resolution Process" caption="The step-by-step process of DNS resolution" %}

{% include callout.html type="note" title="Why DNS Matters" content="Without DNS, you'd need to remember IP addresses for every website you want to visit, making the internet much harder to use." %}

## How DNS Works

### 1. The DNS Query Process

When you type a website address in your browser:

1. **Local DNS Cache Check**
   - Your computer first checks its local DNS cache
   - Recently visited sites are stored here for quick access

2. **Recursive DNS Server**
   - If not in cache, query goes to your ISP's DNS server
   - This server starts the recursive lookup process

3. **Root DNS Servers**
   - Query first goes to root servers (.)
   - They direct to the correct top-level domain servers

4. **Top-Level Domain (TLD) Servers**
   - Handles domains like .com, .org, .net
   - Points to authoritative name servers

5. **Authoritative Name Servers**
   - Contains the actual DNS records
   - Returns the IP address for the domain

{% include callout.html type="important" title="DNS Caching" content="DNS servers cache results to speed up future requests and reduce network traffic." %}

## DNS Record Types

Common DNS record types include:

| Record Type | Purpose | Example |
|------------|---------|---------|
| A | Maps domain to IPv4 | example.com → 93.184.216.34 |
| AAAA | Maps domain to IPv6 | example.com → 2606:2800:220:1:248:1893:25c8:1946 |
| CNAME | Creates domain alias | www.example.com → example.com |
| MX | Specifies mail servers | Mail handled by mail.example.com |
| TXT | Text information | SPF, DKIM records |

## Hands-On DNS Tools

### Using nslookup

```bash
# Basic DNS lookup
nslookup google.com

# Check mail servers
nslookup -type=mx gmail.com

# Query specific DNS server
nslookup google.com 8.8.8.8
```
{: .code-example }

{% include callout.html type="tip" title="Practice Exercise" content="Try looking up different types of DNS records for your favorite websites using nslookup." %}

## Common DNS Issues

### 1. DNS Resolution Failures
- "DNS Server Not Responding"
- "This site can't be reached"
- Slow website loading

### 2. Troubleshooting Steps
```bash
# Clear DNS cache (Windows)
ipconfig /flushdns

# Check DNS servers
ipconfig /all

# Test DNS resolution
nslookup google.com
```
{: .code-example }

### 3. Solutions
- Clear DNS cache
- Check network connection
- Try alternative DNS servers (e.g., 8.8.8.8)
- Contact ISP if persistent

## DNS Security

{% include callout.html type="warning" title="Security Note" content="DNS poisoning and spoofing attacks can redirect users to malicious websites. Always ensure your DNS settings are from trusted sources." %}

### DNSSEC (DNS Security Extensions)
- Adds security to DNS lookups
- Verifies DNS data integrity
- Prevents DNS spoofing

## Best Practices

1. **Use Reliable DNS Servers**
   - Your ISP's servers
   - Public DNS (Google: 8.8.8.8, Cloudflare: 1.1.1.1)

2. **Regular Maintenance**
   - Clear DNS cache periodically
   - Update DNS settings when needed
   - Monitor DNS response times

3. **Security Considerations**
   - Use DNSSEC when available
   - Monitor for unusual DNS behavior
   - Keep DNS software updated

## Next Steps

Continue to [DHCP Basics](dhcp-basics) to learn how devices obtain their network configurations automatically.

## Additional Resources

- DNS troubleshooting guide
- Common DNS commands
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
