# Linux Process Management

A comprehensive, beginner‑friendly, **GitHub‑ready** guide to Linux Process Management with commands.

## What is a Process?

A **process** is a running instance of a program with its own memory, file descriptors, and execution context. Every process has a unique **PID** and a **parent** (PPID). The kernel scheduler decides which process runs on the CPU.

## Key Terms (PID, PPID, UID, GID)

* **PID**: Process ID (unique per process)
* **PPID**: Parent Process ID
* **UID/GID**: User/Group IDs that own the process
* **TTY**: Terminal controlling the process
* **CMD**: Command used to start the process

## Process States

Common `STAT`/state letters from `ps`/`top`:

* **R**: Running
* **S**: Interruptible sleep (waiting for event)
* **D**: Uninterruptible sleep (I/O wait)
* **T**: Stopped (job control)
* **Z**: Zombie (terminated, not reaped)
* **<**: High priority, **N**: Low priority (nice), **+**: foreground

## Must‑Know Commands

**List processes**

```bash
ps            # current shell’s processes
ps -ef        # full-format, all processes
ps aux        # BSD style, shows STAT and %CPU/%MEM
pgrep sshd    # find PIDs by name
pstree -p     # tree view with PIDs

## Signals (kill/killall/pkill)

* `SIGTERM (15)`: request to terminate (default)
* `SIGKILL (9)`: force kill, cannot be trapped
* `SIGINT (2)`: Ctrl+C in terminal
* `SIGSTOP/SIGCONT`: stop/continue a process

## Priorities (nice/renice)
Linux dynamic priority uses **nice** values from **-20 (highest priority)** to **19 (lowest)**.
