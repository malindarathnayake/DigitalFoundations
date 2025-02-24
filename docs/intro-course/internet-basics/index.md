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

## Introduction to the Internet

{% include video.html path="assets/Intro_course/videos/Internet_view.mp4" caption="Overview of how the internet works" %}

The internet is essentially a network of networks - a vast system that connects computers and devices worldwide. When you type a website into your browser, your device sends a request through this network to retrieve the information you want.

{% include callout.html type="important" title="Key Concept" content="Everything on the internet happens through data 'packets' traveling across networks - whether you're browsing websites, sending emails, or streaming videos." %}

## How Data Travels

{% include figure.html path="assets/Intro_course/images/network-animation.svg" class="img-fluid" alt="Network Data Flow" caption="How data packets travel through networks" %}

When you connect to the internet, your data follows this basic path:
1. Your Device → Local Network
2. Local Network → ISP (Internet Service Provider)
3. ISP → Internet Backbone
4. Internet Backbone → Destination Server
5. Server → Back to You

## Basic Network Components

### Client Devices
- Computers
- Smartphones
- Tablets
- Smart devices (IoT)

### Network Infrastructure
- Routers
- Switches
- Modems
- Cables and wireless signals

### Servers
- Web servers
- Email servers
- File servers
- Database servers

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

## Understanding Web Addresses

When you type a web address (URL) like `www.example.com`:
1. Your browser needs to find the server's actual address (IP address)
2. It uses DNS (Domain Name System) to look this up
3. Once found, it can request the webpage

Learn more about DNS in the [Networking section](/intro-course/networking).

## Next Steps

Continue to [How the Internet Works](how-internet-works) for a deeper dive into internet protocols and communication methods.

## Additional Resources

- [Internet Basics Video](assets/Intro_course/videos/Internet_view_1.mp4)
- Command reference guide
- Troubleshooting tips
