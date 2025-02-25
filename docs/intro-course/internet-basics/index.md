---
layout: default
title: Internet & Computer Basics
nav_order: 1
parent: Introduction to Technology
has_children: true
permalink: /intro-course/internet-basics
---

# Internet & Computer Basics
{: .no_toc }

Understanding how devices connect to the internet and how data travels across networks.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is the Internet?

{% include video.html path="assets/Intro_course/videos/Internet_view.mp4" caption="Overview of how the internet works" autoplay=false controls=true %}

The internet is essentially a network of networks - a vast system that connects computers and devices worldwide. When you type a website into your browser, your device sends a request through this network to retrieve the information you want.

{% include callout.html type="important" title="Key Concept" content="Everything on the internet happens through data 'packets' traveling across networks - whether you're browsing websites, sending emails, or streaming videos." %}

### The Internet vs. The Web

Many people use the terms "internet" and "web" interchangeably, but they're actually different:

- **The Internet**: The physical infrastructure of interconnected networks
- **The World Wide Web**: A service that runs on the internet, using HTTP protocol and web browsers

Other internet services include email, file transfers (FTP), messaging, and more.

## Basic Internet Diagram

{% include figure.html path="assets/Intro_course/images/InternetDiagram.svg" class="img-fluid" alt="Basic Internet Diagram" caption="Simplified view of how devices connect to the internet" %}

When you connect to the internet, your data follows this basic path:

1. **Your Device → Local Network**: Your computer connects to your home router
2. **Local Network → ISP**: Your router connects to your Internet Service Provider
3. **ISP → Internet Backbone**: Your ISP connects to larger networks
4. **Internet Backbone → Destination Server**: Data travels to the server hosting the website
5. **Server → Back to You**: The server sends the requested information back through the same path

## Basic Network Components

### Client Devices
- **Computers**: Desktops and laptops
- **Smartphones**: Mobile devices with internet capabilities
- **Tablets**: Portable touchscreen devices
- **Smart devices (IoT)**: Internet-connected appliances, sensors, etc.

### Network Infrastructure
- **Routers**: Direct traffic between networks
- **Switches**: Connect devices within a network
- **Modems**: Convert signals between your home and ISP
- **Cables and wireless signals**: Physical and wireless transmission media

### Servers
- **Web servers**: Host websites and web applications
- **Email servers**: Process and store email messages
- **File servers**: Store and serve files
- **Database servers**: Store and retrieve structured data

## Hands-On Demonstration

Let's try a simple command to see how data travels across the internet:

```bash
ping google.com
```
{: .code-example }

This command shows:
- If you can reach a website
- How long it takes (in milliseconds)
- If any data packets are lost

{% include callout.html type="tip" title="Try It Yourself" content="Open your computer's terminal or command prompt and try pinging different websites to see how response times vary." %}

### What's Happening Behind the Scenes

When you run the ping command:
1. Your computer looks up the IP address for google.com (using DNS)
2. It sends small data packets to that IP address
3. It waits for a response from the server
4. It measures how long the round trip takes
5. It reports the results to you

## Understanding Web Addresses

When you type a web address (URL) like `www.example.com`:
1. Your browser needs to find the server's actual address (IP address)
2. It uses DNS (Domain Name System) to look this up
3. Once found, it can request the webpage

{% include callout.html type="note" title="IP Addresses" content="IP addresses are like phone numbers for devices on the internet. IPv4 addresses look like 192.168.1.1, while newer IPv6 addresses are longer and include letters and numbers." %}

### Anatomy of a URL

A typical URL (Uniform Resource Locator) has several parts:
- **Protocol**: `https://` (secure web protocol)
- **Domain**: `www.example.com` (the website name)
- **Path**: `/products/item1` (specific location on the site)
- **Parameters**: `?color=blue&size=large` (additional information)

## Introduction to Computer Hardware

While we'll cover computer hardware in more detail later, it's important to understand the basic components that enable internet connectivity:

- **CPU (Central Processing Unit)**: The "brain" that processes instructions
- **RAM (Random Access Memory)**: Short-term memory for active processes
- **Network Interface Card**: Hardware that connects to networks
- **Storage**: Where your files and programs are kept

## Next Steps

Continue to [How the Internet Works](how-internet-works) for a deeper dive into internet protocols and communication methods.

## Additional Resources

- [Internet Basics Video](assets/Intro_course/videos/Internet_view_1.mp4)
- [Command Reference Guide](/intro-course/resources/commands)
- [Network Troubleshooting Tips](/intro-course/resources/troubleshooting)
