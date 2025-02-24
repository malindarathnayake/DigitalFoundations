---
layout: default
title: Commands Reference
nav_order: 1
parent: Resources
grand_parent: Introduction to Technology
permalink: /intro-course/resources/commands
---

# Commands Reference
{: .no_toc }

A comprehensive guide to useful commands for networking, system monitoring, and troubleshooting.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Network Commands

### Basic Connectivity

```bash
# Test network connectivity
ping google.com

# Trace route to destination
tracert google.com

# View network configuration
ipconfig /all
```
{: .code-example }

{% include callout.html type="tip" title="Ping Options" content="Use ping -t for continuous ping, Ctrl+C to stop. Add -n [number] to specify ping count." %}

### DNS Commands

```bash
# DNS lookup
nslookup google.com

# Check MX records
nslookup -type=mx gmail.com

# Check TXT records (SPF, DKIM)
nslookup -type=txt domain.com
```
{: .code-example }

### DHCP Commands

```bash
# Release DHCP lease
ipconfig /release

# Renew DHCP lease
ipconfig /renew

# Display DHCP information
ipconfig /displaydns
```
{: .code-example }

{% include callout.html type="warning" title="Network Disruption" content="Release and renew commands will temporarily disconnect you from the network." %}

## System Monitoring

### CPU & Memory

```bash
# Open Task Manager
taskmgr

# View CPU information
wmic cpu get name, numberofcores, maxclockspeed

# View memory information
wmic memorychip get capacity, speed

# Resource monitor
resmon
```
{: .code-example }

### Disk & Storage

```bash
# Check disk space
dir
chkdsk

# View disk information
wmic diskdrive get size, model

# System file check
sfc /scannow
```
{: .code-example }

### Process Management

```bash
# List running processes
tasklist

# Kill process by name
taskkill /IM "process.exe"

# Kill process by ID
taskkill /PID 1234
```
{: .code-example }

## Email Diagnostics

### Server Tests

```bash
# Test SMTP connection
telnet smtp.gmail.com 587

# Check mail server
nslookup -type=mx domain.com

# View email headers
Received: from mail-yw1-f41.google.com
```
{: .code-example }

### Authentication

```bash
# Check SPF record
nslookup -type=txt domain.com

# View DMARC policy
nslookup -type=txt _dmarc.domain.com
```
{: .code-example }

## Performance Analysis

### System Information

```bash
# Detailed system info
systeminfo

# List installed programs
wmic product get name

# View startup programs
wmic startup list brief
```
{: .code-example }

### Network Performance

```bash
# Network statistics
netstat -an

# Network interface statistics
netstat -e

# Protocol statistics
netstat -s
```
{: .code-example }

{% include callout.html type="note" title="Real-time Monitoring" content="Add -p to netstat commands for continuous monitoring." %}

## Troubleshooting Commands

### Network Reset

```bash
# Reset TCP/IP
netsh int ip reset

# Reset Winsock
netsh winsock reset

# Flush DNS cache
ipconfig /flushdns
```
{: .code-example }

### System Cleanup

```bash
# Disk cleanup
cleanmgr

# Check system files
sfc /scannow

# Clear temporary files
del /s /q %temp%\*
```
{: .code-example }

## Advanced Commands

### Power Management

```bash
# Power configuration
powercfg /energy

# Battery report
powercfg /batteryreport

# Sleep study
powercfg /sleepstudy
```
{: .code-example }

### System Recovery

```bash
# System restore
rstrui.exe

# Startup repair
shutdown /r /o

# Check disk
chkdsk /f
```
{: .code-example }

## Best Practices

### Command Usage
- Always run as administrator when required
- Document commands and results
- Use help flags for more information
- Be careful with destructive commands

### Safety Tips
- Back up data before major changes
- Verify commands before execution
- Keep system restore points
- Document configuration changes

{% include callout.html type="important" title="Administrative Rights" content="Many system commands require administrator privileges. Right-click Command Prompt and select 'Run as administrator'." %}

## Additional Resources

- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
- Microsoft Command Line Reference
- PowerShell Documentation
- System Administration Guides
