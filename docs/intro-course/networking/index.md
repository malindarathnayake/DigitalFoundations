---
layout: default
title: Networking
nav_order: 2
parent: Introduction to Technology
has_children: true
permalink: /intro-course/networking
---

# Networking: DNS & DHCP
{: .no_toc }

Understanding how devices obtain IP addresses and how domain names are resolved.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction to Network Services

Modern networks rely on two crucial services to function properly:
- **DNS (Domain Name System)**: Converts human-readable domain names to IP addresses
- **DHCP (Dynamic Host Configuration Protocol)**: Automatically assigns network configuration to devices

{% include callout.html type="important" title="Key Concept" content="Think of DNS as the internet's phone book and DHCP as the hotel front desk that assigns room numbers to guests." %}

## DNS Overview

{% include figure.html path="assets/Intro_course/images/DNS_Flow.svg" class="img-fluid" alt="DNS Flow Diagram" caption="How DNS resolves domain names to IP addresses" %}

DNS is responsible for:
- Converting domain names (like google.com) to IP addresses
- Storing and distributing website location information
- Enabling global access to websites using memorable names

[Learn more about DNS](dns-basics){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

## DHCP Overview

{% include figure.html path="assets/Intro_course/images/DHCP_flow.svg" class="img-fluid" alt="DHCP Flow Diagram" caption="The DHCP process for obtaining network configuration" %}

DHCP handles:
- Automatic IP address assignment
- Network configuration distribution
- IP address management and lease time
- Conflict prevention in network addressing

[Learn more about DHCP](dhcp-basics){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

## Why These Services Matter

### Without DNS
- You'd need to remember IP addresses for every website
- No easy way to change server locations
- Difficult to manage web services

### Without DHCP
- Manual network configuration required
- Higher chance of address conflicts
- More complex network management
- Difficult to move between networks

## Hands-On Practice

Try these commands to see DNS and DHCP in action:

```bash
# View your DHCP-assigned IP configuration
ipconfig /all

# Look up DNS information for a domain
nslookup google.com
```
{: .code-example }

{% include callout.html type="tip" title="Practice Tip" content="Try these commands on your computer to see your actual network configuration and DNS resolution in action." %}

## Common Issues and Solutions

### DNS Issues
- Cannot resolve website names
- Slow website loading
- "DNS Server Not Responding" errors

### DHCP Issues
- "No Valid IP Configuration"
- Limited or no network access
- IP address conflicts

## Next Steps

1. Start with [DNS Basics](dns-basics) to understand how domain names work
2. Continue to [DHCP Basics](dhcp-basics) to learn about network configuration
3. Try the hands-on exercises in each section

## Additional Resources

- Network troubleshooting guide
- Common networking commands
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
