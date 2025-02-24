---
layout: default
title: RAM Basics
nav_order: 2
parent: Computer Hardware
grand_parent: Introduction to Technology
permalink: /intro-course/hardware/ram-basics
---

# RAM Basics
{: .no_toc }

Understanding computer memory and its role in system performance.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is RAM?

Random Access Memory (RAM) is your computer's short-term memory that:
- Stores currently running programs
- Holds active data for quick access
- Provides fast read/write operations
- Clears when power is turned off

{% include callout.html type="note" title="Key Concept" content="Think of RAM as your computer's workspace - it holds everything you're actively working on, but clears when you shut down." %}

## How RAM Works

### Memory Hierarchy

1. **CPU Registers**
   - Fastest memory
   - Very small capacity
   - Built into CPU

2. **Cache Memory**
   - L1, L2, L3 cache
   - Very fast access
   - Small capacity
   - Expensive

3. **RAM**
   - Main system memory
   - Fast access
   - Larger capacity
   - Volatile storage

4. **Storage (HDD/SSD)**
   - Permanent storage
   - Slower access
   - Large capacity
   - Non-volatile

{% include callout.html type="important" title="Speed vs. Capacity" content="As you move down the memory hierarchy, capacity increases but speed decreases." %}

## RAM Characteristics

### 1. Volatile Memory
- Requires power to maintain data
- Clears on shutdown
- Temporary storage only

### 2. Random Access
- Any memory location accessible
- Equal access time to all data
- No sequential reading needed

### 3. Speed
- Much faster than storage
- Slower than CPU cache
- Measured in MHz/GHz

## RAM and Performance

### Memory Usage Monitoring

```bash
# Windows Memory Info
wmic memorychip get capacity, speed

# View memory usage
taskmgr
```
{: .code-example }

### Common Performance Issues

1. **Low Memory**
   - Slow performance
   - System freezes
   - Excessive disk activity
   - Application crashes

2. **Memory Leaks**
   - Gradually increasing usage
   - Degrading performance
   - Application instability

{% include callout.html type="warning" title="Memory Warning" content="Running out of RAM forces your system to use much slower disk-based virtual memory, severely impacting performance." %}

## Virtual Memory

### What is Virtual Memory?
- Disk space used as RAM
- Managed by operating system
- Called "page file" or "swap"
- Much slower than RAM

### How It Works
1. System needs more memory
2. Data moved to page file
3. Retrieved when needed
4. Process called "paging"

```bash
# View page file usage (Windows)
wmic pagefile list /format:list
```
{: .code-example }

## Memory Management

### 1. Application Memory
- Program code
- Data structures
- Temporary variables
- Cached content

### 2. System Memory
- Operating system
- Device drivers
- System services
- File cache

### 3. Shared Memory
- Multiple programs
- System resources
- Common libraries
- Cached data

## Best Practices

### 1. Memory Usage
- Close unused programs
- Monitor usage patterns
- Manage browser tabs
- Limit background tasks

### 2. System Configuration
- Appropriate page file size
- Regular restarts
- Clean startup items
- Update drivers

{% include callout.html type="tip" title="Browser Memory" content="Web browsers can use significant RAM. Consider using browser extensions to manage tab memory usage." %}

## Hands-On Practice

Try these monitoring tasks:

1. **Memory Analysis**
```bash
# Open Resource Monitor (Windows)
resmon
```
{: .code-example }

2. **Usage Patterns**
- Monitor total usage
- Check per-application usage
- Observe page file activity
- Track memory trends

## Troubleshooting Memory Issues

### 1. Diagnosis
- Check Task Manager
- Monitor resource usage
- Review error messages
- Test memory health

### 2. Solutions
- Close unnecessary programs
- Increase page file size
- Add more RAM
- Check for memory leaks

### 3. Prevention
- Regular maintenance
- System updates
- Memory testing
- Usage monitoring

## Memory Optimization Tips

### 1. Software Management
- Uninstall unused programs
- Update applications
- Clear temporary files
- Manage startup items

### 2. Browser Optimization
- Limit open tabs
- Clear cache regularly
- Use memory-saving extensions
- Monitor browser processes

### 3. System Settings
- Adjust visual effects
- Optimize page file
- Configure startup programs
- Regular maintenance

## Next Steps

Review the [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html) for useful memory monitoring commands and tools.

## Additional Resources

- Memory testing tools
- Performance monitoring guides
- System optimization tips
- Troubleshooting documentation
