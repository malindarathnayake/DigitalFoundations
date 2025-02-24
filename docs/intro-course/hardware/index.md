---
layout: default
title: Computer Hardware
nav_order: 4
parent: Introduction to Technology
has_children: true
permalink: /intro-course/hardware
---

# Computer Hardware
{: .no_toc }

Understanding the fundamental components that power computers.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction to Computer Hardware

Modern computers are complex machines built from various components working together. Understanding the basic hardware components helps you:
- Diagnose performance issues
- Make informed upgrade decisions
- Maintain your computer effectively

## Core Components

### 1. CPU (Central Processing Unit)
The "brain" of the computer that:
- Executes instructions
- Performs calculations
- Coordinates other components

[Learn more about CPU](cpu-basics){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

### 2. RAM (Random Access Memory)
The computer's "short-term memory" that:
- Stores active programs
- Holds current data
- Enables quick access

[Learn more about RAM](ram-basics){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

## How Components Work Together

{% include callout.html type="note" title="System Integration" content="The CPU and RAM work together closely - the CPU processes instructions stored in RAM, which holds both the programs and their data." %}

### Processing Flow
1. Program loads into RAM
2. CPU fetches instructions
3. CPU executes instructions
4. Results stored in RAM
5. Process repeats

## Performance Monitoring

### Using Task Manager (Windows)

```bash
# Open Task Manager
taskmgr

# Alternative command-line tool
wmic cpu get loadpercentage
```
{: .code-example }

### Using Terminal (Linux/Mac)
```bash
# View system resources
top

# Memory information
free -h
```
{: .code-example }

{% include callout.html type="tip" title="Monitoring Tip" content="Regular monitoring helps you understand your computer's normal behavior and spot potential issues early." %}

## Common Hardware Issues

### 1. Performance Problems
- High CPU usage
- RAM bottlenecks
- Slow response times
- System freezes

### 2. Hardware Failures
- System crashes
- Boot failures
- Memory errors
- Overheating

## Best Practices

### 1. Maintenance
- Regular cleaning
- Good ventilation
- Monitor temperatures
- Update drivers

### 2. Usage
- Close unused programs
- Manage startup items
- Monitor resource usage
- Regular restarts

### 3. Upgrades
- Assess needs
- Check compatibility
- Plan capacity
- Consider future needs

## Hands-On Practice

Try these monitoring tasks:

1. **CPU Monitoring**
   - Open Task Manager
   - Watch CPU usage
   - Identify heavy processes
   - Note temperature

2. **RAM Analysis**
   - Check memory usage
   - Observe page file use
   - Monitor application memory
   - Identify memory leaks

{% include callout.html type="important" title="Safety First" content="Always shut down your computer properly and avoid opening it unless you're qualified to do so." %}

## Next Steps

1. Start with [CPU Basics](cpu-basics) to understand processing
2. Continue to [RAM Basics](ram-basics) for memory concepts
3. Practice monitoring system resources

## Additional Resources

- Hardware troubleshooting guides
- System monitoring tools
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
- Performance optimization tips
