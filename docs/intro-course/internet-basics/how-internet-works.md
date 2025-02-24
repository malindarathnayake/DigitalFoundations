---
layout: default
title: How the Internet Works
nav_order: 2
parent: Internet & Computer Basics
grand_parent: Introduction to Technology
permalink: /intro-course/internet-basics/how-internet-works
---

# How the Internet Works
{: .no_toc }

A detailed look at internet protocols, data transmission, and network communication.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## The Internet: A Network of Networks

The internet is built on a hierarchical structure of networks:
- Local Networks (your home/office)
- Regional Networks (your ISP)
- National/International Networks (internet backbone)
- Tier 1 ISPs (Core Internet Infrastructure)

{% include callout.html type="note" title="Did You Know?" content="The internet was originally developed by DARPA (Defense Advanced Research Projects Agency) as a way to maintain communication in case of a nuclear attack." %}

## Core Internet Infrastructure

### ISP Tiers
1. **Tier 1 ISPs**
   - Form the backbone of the internet
   - Direct connections to other Tier 1 providers
   - Global network coverage
   
2. **Tier 2 ISPs**
   - Regional and national providers
   - Connect to Tier 1 networks
   - Serve smaller ISPs and businesses

3. **Tier 3 ISPs**
   - Local service providers
   - Connect end users to the internet
   - Purchase transit from larger ISPs

## How Data Packets Work

When you send or receive information over the internet, it's broken down into small pieces called packets:

1. **Breaking Down Data**
   - Large files are split into smaller packets
   - Each packet contains:
     - Source address
     - Destination address
     - Packet number
     - Actual data

2. **Packet Routing**
   - Packets may take different paths
   - They're reassembled at the destination
   - If a packet is lost, only that piece needs to be resent

{% include video.html path="assets/Intro_course/videos/Internet_view_1.mp4" caption="Detailed view of internet infrastructure" %}

## Internet Protocols

### TCP/IP (Transmission Control Protocol/Internet Protocol)
The fundamental protocol of the internet:
- TCP breaks data into packets and reassembles them
- IP handles addressing and routing
- Ensures reliable data delivery
- Manages network congestion

### HTTP/HTTPS (HyperText Transfer Protocol)
Used for web browsing:
- HTTP: Basic web communication
- HTTPS: Secured, encrypted version
- TLS encryption for data protection
- Certificate validation for security

### DHCP (Dynamic Host Configuration Protocol)
Automatic network configuration:
- IP address assignment
- Subnet mask configuration
- Default gateway setup
- DNS server information

### DNS (Domain Name System)
The internet's address book:
- Converts domain names to IP addresses
- Hierarchical naming system
- Distributed database
- Caching for performance

{% include callout.html type="important" title="Security Note" content="Always look for HTTPS when sharing sensitive information online. The 'S' means the connection is encrypted." %}

## Real-World Example: Loading a Webpage

When you visit a website, here's what happens:

1. **DNS Lookup**
   - Convert domain name to IP address
   - Find the server's location

2. **Connection Establishment**
   - Your device connects to the server
   - Handshake process occurs

3. **Data Transfer**
   - Request webpage content
   - Server sends back files
   - Browser renders the page

## Hands-On Demonstration

Try these commands to see the internet in action:

```bash
# See the path to a website
traceroute google.com

# View DNS information
nslookup google.com

# Check connection status
ping google.com
```
{: .code-example }

{% include callout.html type="tip" title="Practice Exercise" content="Try these commands with different websites and compare the results. What differences do you notice in response times and number of hops?" %}

## Network Troubleshooting

Common issues and how to diagnose them:

1. **Can't Connect to Internet**
   - Check physical connections
   - Verify IP address assignment
   - Test DNS resolution

2. **Slow Connection**
   - Check network usage
   - Test bandwidth
   - Monitor packet loss

3. **Website Not Loading**
   - Verify DNS resolution
   - Check server status
   - Clear browser cache
   
## Next Steps

Continue to the [Networking section](/intro-course/networking) to learn about DNS and DHCP - crucial systems that make the internet work smoothly.

## Additional Resources

- Network troubleshooting guide
- Common networking commands
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
