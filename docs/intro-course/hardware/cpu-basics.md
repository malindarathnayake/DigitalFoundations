---
layout: default
title: CPU Basics
nav_order: 1
parent: Computer Hardware
grand_parent: Introduction to Technology
permalink: /intro-course/hardware/cpu-basics
---

# CPU Basics
{: .no_toc }

Understanding the brain of your computer - the Central Processing Unit.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What is a CPU?

The Central Processing Unit (CPU) is the primary processor in a computer that:
- Executes program instructions
- Performs calculations and logical operations
- Coordinates data movement between components

{% include callout.html type="note" title="Key Concept" content="Think of the CPU as the brain of your computer - it makes decisions, performs calculations, and coordinates all activities." %}

## How CPUs Work

### The Fetch-Decode-Execute Cycle

Every CPU operation follows this basic cycle:

1. **Fetch**
   - Retrieve instruction from memory
   - Move to instruction register
   - Update program counter

2. **Decode**
   - Interpret instruction
   - Determine required operations
   - Identify data locations

3. **Execute**
   - Perform the operation
   - Store results
   - Prepare for next instruction

{% include callout.html type="important" title="Processing Speed" content="This cycle happens billions of times per second in modern CPUs!" %}

## CPU Components

### Core Parts
1. **Control Unit**
   - Manages instruction flow
   - Coordinates operations
   - Controls data movement

2. **Arithmetic Logic Unit (ALU)**
   - Performs calculations
   - Handles logical operations
   - Processes data

3. **Registers**
   - Small, fast memory
   - Temporary data storage
   - Quick access for CPU

### Modern Features
- Multiple cores
- Cache memory
- Branch prediction
- Hyperthreading

## Understanding CPU Specifications

### Clock Speed
```
Clock Speed = Cycles per second (measured in Hz)
3.5 GHz = 3.5 billion cycles per second
```
{: .code-example }

### Core Count
- Single-core
- Dual-core
- Quad-core
- Octa-core and beyond

{% include callout.html type="tip" title="More Cores ≠ Always Better" content="Not all applications can use multiple cores effectively. Some tasks benefit more from higher clock speeds." %}

## CPU Performance Monitoring

### Using Task Manager (Windows)

```bash
# Open Task Manager
taskmgr

# View detailed CPU info
wmic cpu get name, numberofcores, maxclockspeed
```
{: .code-example }

### Key Metrics to Monitor
1. **Usage Percentage**
   - Overall CPU usage
   - Per-core usage
   - Process-specific usage

2. **Temperature**
   - Normal operating range
   - Thermal throttling
   - Cooling effectiveness

3. **Clock Speed**
   - Base frequency
   - Turbo boost
   - Thermal limits

## Common CPU Issues

### 1. High CPU Usage
**Symptoms:**
- System slowdown
- Fan noise increase
- Application lag

**Solutions:**
- Close unnecessary programs
- Check for malware
- Update software
- Monitor background processes

### 2. Overheating
**Symptoms:**
- Random shutdowns
- Performance throttling
- System instability

**Solutions:**
- Clean dust from fans
- Improve ventilation
- Replace thermal paste
- Check cooling system

{% include callout.html type="warning" title="Temperature Warning" content="Sustained high temperatures can permanently damage your CPU. Monitor temperatures and ensure proper cooling." %}

## CPU Best Practices

### 1. Maintenance
- Keep system clean
- Ensure good airflow
- Update drivers
- Monitor temperatures

### 2. Usage
- Balance workloads
- Manage background tasks
- Use appropriate power plans
- Avoid excessive overclocking

### 3. Optimization
- Update Windows/OS
- Optimize startup programs
- Use appropriate power settings
- Monitor resource usage

## Hands-On Practice

Try these monitoring exercises:

1. **Usage Monitoring**
```bash
# Windows Performance Monitor
perfmon /res
```
{: .code-example }

2. **Process Analysis**
- Open Task Manager
- Sort by CPU usage
- Identify resource-intensive processes
- Monitor thread usage

## Performance Tips

### 1. Software Optimization
- Close unused programs
- Update applications
- Manage startup items
- Use appropriate power plans

### 2. System Maintenance
- Regular updates
- Driver maintenance
- Disk cleanup
- Malware scanning

### 3. Hardware Considerations
- Adequate cooling
- Proper ventilation
- Quality power supply
- Regular cleaning

## Next Steps

Continue to [RAM Basics](ram-basics) to understand how memory works with the CPU to run programs efficiently.

## Additional Resources

- CPU specifications guide
- Performance monitoring tools
- [Command Cheatsheet](assets/Intro_course/slides/command-cheatsheet.html)
- Troubleshooting guides
