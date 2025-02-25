---
layout: default
title: Computer Hardware
nav_order: 4
parent: Introduction to Technology
has_children: true
permalink: /intro-course/hardware
---

# CPU & RAM Basics
{: .no_toc }

Understanding the fundamental components that power computers and how they process information.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction to Computer Hardware

Modern computers are complex machines built from various components working together. Understanding the basic hardware components helps you:
- Diagnose performance issues
- Make informed upgrade decisions
- Understand how your devices process information
- Troubleshoot common problems

{% include callout.html type="important" title="Key Concept" content="While computers have many components, the CPU and RAM are the most critical for understanding how computers process and temporarily store information." %}

## Core Components

### 1. CPU (Central Processing Unit)
The "brain" of the computer that:
- Executes instructions using the fetch-decode-execute cycle
- Performs calculations and logical operations
- Coordinates other components
- Operates at a specific clock speed (measured in GHz)
- May have multiple cores for parallel processing

{% include figure.html path="assets/Intro_course/images/CPU_Diagram.svg" class="img-fluid" alt="CPU Diagram" caption="Basic structure of a CPU showing the fetch-decode-execute cycle" %}

[Learn more about CPU](cpu-basics){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

### 2. RAM (Random Access Memory)
The computer's "short-term memory" that:
- Stores active programs and current data
- Provides fast access compared to storage drives
- Is volatile (contents are lost when power is off)
- Has a specific capacity (measured in GB)
- Affects how many programs can run simultaneously

{% include figure.html path="assets/Intro_course/images/RAM_Diagram.svg" class="img-fluid" alt="RAM Diagram" caption="How RAM stores and retrieves data for active programs" %}

[Learn more about RAM](ram-basics){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

## How Components Work Together

{% include callout.html type="note" title="System Integration" content="The CPU and RAM work together closely - the CPU processes instructions stored in RAM, which holds both the programs and their data." %}

### The Fetch-Decode-Execute Cycle

The fundamental process that powers all computing:

1. **Fetch**: CPU retrieves an instruction from RAM
2. **Decode**: CPU determines what the instruction means
3. **Execute**: CPU performs the instruction
4. **Store**: Results are written back to RAM
5. **Repeat**: The cycle continues millions of times per second

{% include figure.html path="assets/Intro_course/images/FetchDecodeExecute.svg" class="img-fluid" alt="Fetch-Decode-Execute Cycle" caption="The continuous cycle that powers all computing operations" %}

## Hands-On Demonstration

### Using Task Manager (Windows)

```bash
# Open Task Manager
taskmgr
```
{: .code-example }

Task Manager shows:
- Current CPU usage percentage
- Memory (RAM) usage
- Running processes and their resource consumption
- Performance history graphs

### Using Terminal (Mac/Linux)
```bash
# View system resources
top

# Memory information
free -h
```
{: .code-example }

{% include callout.html type="tip" title="Try It Yourself" content="Open your computer's Task Manager (Windows) or Activity Monitor (Mac) and observe how CPU and RAM usage changes as you open and close programs." %}

## Real-World Impact

### When CPU is Overloaded:
- System becomes sluggish
- Programs respond slowly
- Operations take longer to complete
- Computer may feel hot as the processor works harder

### When RAM is Insufficient:
- System slows down dramatically
- Programs may crash
- Computer starts using disk space as virtual memory (much slower)
- You may see "out of memory" errors

## Mini Troubleshooting Activity

### Scenario: Your computer is running slowly

**Steps to diagnose:**
1. Open Task Manager/Activity Monitor
2. Check CPU usage - is it consistently near 100%?
3. Check RAM usage - is it nearly full?
4. Identify which processes are using the most resources
5. Determine if you need to close programs, add more RAM, or upgrade your CPU

{% include callout.html type="warning" title="Resource Hogs" content="Some common causes of high resource usage include web browsers with many tabs, video editing software, games, and malware." %}

## Best Practices for Optimal Performance

### 1. Software Management
- Close unused programs to free up RAM
- Limit startup programs that run automatically
- Keep your operating system and applications updated
- Restart your computer regularly to clear RAM

### 2. Hardware Maintenance
- Ensure proper ventilation for cooling
- Clean dust from air vents periodically
- Monitor temperatures during intensive tasks
- Consider upgrading RAM if consistently at capacity

### 3. When to Upgrade
- When multiple programs run slowly simultaneously
- When newer software requires more resources
- When Task Manager consistently shows high usage
- When your work or activities are being limited

## Understanding Computer Specifications

When buying or upgrading a computer, these are key specifications to understand:

### CPU Specifications
- **Clock Speed**: How many cycles per second (e.g., 3.2 GHz)
- **Cores**: Number of processing units (e.g., quad-core, octa-core)
- **Cache**: Small, very fast memory built into the CPU
- **Architecture**: Design and instruction set (e.g., x86, ARM)

### RAM Specifications
- **Capacity**: Total memory available (e.g., 8GB, 16GB)
- **Type**: Technology generation (e.g., DDR4, DDR5)
- **Speed**: How quickly data can be accessed (e.g., 3200 MHz)
- **Channels**: How memory communicates with the system

{% include callout.html type="important" title="Safety First" content="Always shut down your computer properly before making any hardware changes, and avoid opening your computer unless you're qualified to do so." %}

## Next Steps

1. Explore [CPU Basics](cpu-basics) for a deeper understanding of processors
2. Continue to [RAM Basics](ram-basics) for more on memory concepts
3. Practice monitoring your system resources using Task Manager
4. Try the troubleshooting activity with your own computer

## Additional Resources

- [Hardware Troubleshooting Guide](/intro-course/resources/hardware-troubleshooting)
- [System Monitoring Tools](/intro-course/resources/monitoring-tools)
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
- [Performance Optimization Tips](/intro-course/resources/performance-tips)
