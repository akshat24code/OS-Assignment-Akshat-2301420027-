**Operating Systems Lab Assignment**  
**Submitted by: AKSHAT SHARMA, B.Tech CSE, Semester 5, Roll No: 2301420027**

# Experiment 1: Process Management in OS

## Summary of Tasks

---

### OS Assignment: Process Management in Linux

### This repository contains a comprehensive 5-task assignment on process management in Linux, completed by Akshat Sharma (Roll No. 2301420027) as part of the 5th-semester Operating Systems course.The tasks demonstrate important concepts of Linux process management through:Direct use of C system calls Interactions with the Linux kernel’s /proc filesystem, This work provides both practical coding exercises and conceptual understanding of how processes are created, managed, and monitored within Linux.

---

### **Task 1: Creating and Managing Processes**

This section focuses on the fundamental concepts of process creation. The goal is to:

- Create **three child processes** from a single parent process.
- Use the **`fork()`** system call to duplicate the parent process.
- Display the **Process IDs (PIDs)** of all child processes to verify their creation.

### **Task 2: Executing External Commands**

This task explores how a process can execute a completely different program.

- A child process is created specifically to run an external command.
- The **`exec()`** family of system calls is used to replace the child process's image with the **`ls -l`** command.

### **Task 3: Demonstrating Special Process States**

This section dives into the lifecycle of processes, specifically focusing on states that can occur if not handled properly.

- **Zombie Process**: A terminated process whose parent has not yet collected its exit status.
- **Orphan Process**: A process whose parent has terminated, causing it to be adopted by the **`init`** (or **`systemd`**) process.

### **Task 4: Examining Process Information**

This task demonstrates how to programmatically access detailed information about a running process directly from the Linux kernel.

- Read details from the virtual **`/proc`** filesystem.
- Extract information such as the process **status**, the path to its **executable file**, and its open **file descriptors**.

### **Task 5: Managing Process Priority**

This final task illustrates how process scheduling can be influenced by adjusting a process's priority.

- The **`nice`** value is used to adjust a process's scheduling priority.
- A **lower nice value** (e.g., -20) gives the process a higher priority and more CPU time.
- A **higher nice value** (e.g., +19) gives it a lower priority.

---

## Process Flow (Visual)

```mermaid
flowchart TD
    A["1. Create Processes
Fork three child processes and display their PIDs"] --> B["2. Execute Commands
Run 'ls -l' within a child process using exec()"]
    B --> C["3. Handle Special Processes
Demonstrate zombie and orphan process states"]
    C --> D["4. Examine Process Information
Read details from the /proc filesystem (status, exe, fd)"]
    D --> E["5. Manage Process Priority
Adjust nice values and observe scheduling behavior"]

```

## Included Files

- `process_management.py`: The main Python script containing the implementation for all tasks.
- `output.txt`: A file containing sample output from the script execution.
- `OS_Lab_Assignment 1.docx`: The original assignment document.
- `report.pdf`: The detailed lab report for this experiment.
