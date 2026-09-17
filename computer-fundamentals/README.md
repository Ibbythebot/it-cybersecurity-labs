# Computer Fundamentals & Windows Process Investigation

## Overview

This was my first hands-on introduction to computer fundamentals and basic Windows process investigation.

The goal of this lab was to understand how computer hardware, software, the operating system, applications, and processes interact, and then apply those concepts by investigating a running process using Windows Task Manager.

## Concepts Learned

### CPU

The CPU (Central Processing Unit) executes instructions and performs the calculations needed to run programs.

### RAM

RAM (Random Access Memory) is temporary working memory used by the computer while programs are running. It provides much faster access to actively used data than persistent storage.

### SSD/HDD

An SSD or HDD provides persistent storage. Files remain stored on the drive even after the computer is shut down.

### Operating System

The operating system acts as a layer between applications/users and the computer's hardware. It manages resources such as CPU time, memory, storage, processes, devices, users, permissions, and networking.

### Applications vs. Processes

An application is software designed to perform a particular task.

A process is a running instance of a program that the operating system is currently managing.

For example:

* Brave Browser installed on the computer = application
* `brave.exe` running in Task Manager = process

### Process ID (PID)

A Process ID (PID) is a unique identifier assigned by Windows to a running process.

It allows a specific process to be identified and investigated.

## Hands-On Investigation

I used Windows Task Manager to investigate a running Brave Browser process.

### Process Observations

| Attribute           | Observation                                                    |
| ------------------- | -------------------------------------------------------------- |
| Process             | `brave.exe`                                                    |
| PID                 | `8332`                                                         |
| CPU Usage           | ~0% at time of observation                                     |
| Memory Usage        | 86,784 K (~85 MB)                                              |
| Executable Location | `Program Files > Brave Software > Brave Browser > Application` |

I accessed the executable's location by right-clicking the process in Task Manager and selecting **Open file location**.

The executable was located within Brave Browser's expected installation directory.

## Security Takeaways

One important lesson from this investigation was that a process should not be classified as malicious based on a single observation.

For example, high CPU usage does not automatically indicate malware. A legitimate application performing a demanding task can also use a large amount of CPU.

Similarly, an unfamiliar process should not automatically be considered malicious.

A security investigation should gather additional evidence, such as:

* What process is running?
* What is its PID?
* What resources is it using?
* Where is its executable located?
* What process started it?
* What files or network connections is it accessing?
* Is its behavior expected?

The goal is to investigate the evidence before reaching a conclusion.

## Tools Used

* Windows Task Manager
* Windows File Explorer
* GitHub

## What I Learned

This lab gave me a basic understanding of how Windows manages applications and processes and introduced me to the idea of investigating system activity using observable evidence rather than making assumptions.
