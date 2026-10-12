Advanced xv6-riscv Operating System Extensions: 
Project Information
Project Base: mit-pdos/xv6-riscv (a re-implementation of Unix Version 6 for RISC-V, written in C)

Student Name: [Musab Hasnain Shah]

Roll Number: [BCS-F24-M47]

Subject: Operating Systems 

Instructor: [Sir Raza]

Project Scope: Implementation of five advanced kernel and user-space features covering asynchronous timers, access control security, process visibility, resource limits, and file I/O.

Overview
This project extends the xv6-riscv teaching kernel (a re-implementation of Unix Version 6 for RISC-V, written in C) provided as the base by the instructor. The goal is to add five advanced features covering timer-based system calls, security and access control, process inspection, resource limiting, and low-level file operations.

Project Features: 

Feature 1: Alarm System Call (alarm)

Adds an alarm(int ticks, void (*handler)()) system call that triggers a user-defined function callback after a specific number of CPU timer ticks elapse, teaching timer interrupts and asynchronous event handling.

Feature 2: File Permissions & Access Control (chmod & UIDs)

Introduces user IDs (UIDs) to processes and permission bits (read/write/execute) to file inodes, enforcing basic security checks during sys_open() to prevent unauthorized file modifications.

Feature 3: Process Status Command (ps)

Builds a proper user-space command (ps) backed by a system call to cleanly list active processes, their PIDs, and their states by safely iterating through the kernel process table.

Feature 4: Process Resource Limits (ulimit)

Restricts processes from opening an excessive number of files by introducing resource tracking fields into struct proc and validation logic inside file-allocation system calls.

Feature 5: Disk Usage / File Copy Utility (cp)

Implements a standard Unix file copy utility (user/cp.c) using low-level file descriptors (open, read, write, close) to solidify how raw byte streams are handled within the xv6 file system.
