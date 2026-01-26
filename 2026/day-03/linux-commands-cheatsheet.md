# Day 03 – Linux Commands Practice  


This cheat sheet covers commonly used Linux commands for **process management, file system, and networking troubleshooting**.

---

## 1. Process Management Commands

- `ps aux` – Show all running processes.
- `top` – Real-time process and resource monitor.
- `htop` – Enhanced interactive process viewer.
- `kill <PID>` – Send a signal to stop a process.
- `kill -9 <PID>` – Force kill a process.
- `nice -n 10 command` – Start a process with lower priority.
- `renice -n 5 -p <PID>` – Change priority of a running process.
- `uptime` – Show system running time and load average.
- `watch -n 1 ps aux` – Refresh process list every second.

---

## 2. File System Commands

- `ls -la` – List files with details and hidden files.
- `pwd` – Show current directory path.
- `cd /path` – Change directory.
- `touch file.txt` – Create an empty file.
- `mkdir test` – Create a directory.
- `rm file.txt` – Delete a file.
- `rm -r folder` – Delete a directory recursively.
- `cp file1 file2` – Copy a file.
- `mv old.txt new.txt` – Rename or move a file.
- `du -sh *` – Show size of files and folders.
- `df -h` – Show disk usage.
- `stat file.txt` – Show file details and timestamps.

---

## 3. Log & Text Inspection Commands

- `cat file.log` – View entire file content.
- `less file.log` – Scroll through large files.
- `tail -n 50 file.log` – View last 50 lines.
- `tail -f file.log` – Follow a growing log file.
- `grep "error" file.log` – Search for a word in a file.
- `wc -l file.log` – Count lines in a file.

---

## 4. Networking Troubleshooting Commands

- `ping google.com` – Check network connectivity.
- `ip addr` – Show IP addresses.
- `ss -tuln` – Show listening ports.
- `curl http://example.com` – Test HTTP response.
- `dig google.com` – DNS lookup.
- `netstat -tulnp` – Show ports and services.

---

## 5. System Information Commands

- `uname -a` – Show kernel and OS details.
- `free -h` – Show memory usage.
- `lsblk` – Show block devices.
- `whoami` – Show current user.
- `hostnamectl` – Show system hostname.

---

## Quick Notes

- Use `man <command>` to read detailed manuals.
- Combine commands using pipes: `ps aux | grep nginx`
- Use `sudo` when permission is denied.

---

## Why This Matters for DevOps

- Quickly inspect logs and services.
- Troubleshoot network issues.
- Monitor CPU, memory, and disk usage.
- Resolve incidents faster in production.

---
