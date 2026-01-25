# Linux Architecture, Processes, and systemd

## 1. Core Components of Linux

- **Kernel**
  - The heart of the OS.
  - Manages CPU, memory, devices, filesystems, and networking.
  - Talks directly to hardware.

- **User Space**
  - Where user programs run (bash, nginx, docker, etc.).
  - Includes system libraries (glibc) and utilities.

- **Init / systemd**
  - First process started by the kernel (PID 1).
  - Starts and manages all other services.
  - Handles service restarts, logging, and boot order.

---

## 2. How Processes Are Created and Managed

- A process is a running program.
- New processes are created using:
  - `fork()` → creates a copy of the current process.
  - `exec()` → replaces process memory with a new program.

- Each process has:
  - PID (Process ID)
  - PPID (Parent PID)
  - State
  - Priority

---

## 3. Process States

- **R (Running)** – Currently using CPU or ready to run.
- **S (Sleeping)** – Waiting for an event (disk, network, input).
- **D (Uninterruptible Sleep)** – Waiting for I/O (cannot be killed easily).
- **T (Stopped)** – Paused by signal or debugger.
- **Z (Zombie)** – Finished execution but parent hasn’t collected exit status.

---

## 4. What systemd Does and Why It Matters

- Starts services at boot.
- Restarts crashed services automatically.
- Manages dependencies between services.
- Collects logs using `journald`.

- Common uses:
  - Start/stop services
  - Enable services at boot
  - Check service status

---

## 5. Daily Useful Commands

- `ps aux` → List all running processes.
- `top` / `htop` → Monitor CPU and memory usage.
- `systemctl status nginx` → Check service status.
- `journalctl -u nginx` → View service logs.
- `kill -9 <PID>` → Force stop a process.

---

## 6. Why This Matters for DevOps

- Helps debug crashed services.
- Understand high CPU or memory usage.
- Confidently manage services and logs.

---

## Quick Summary

- Kernel = core OS  
- User space = apps + tools  
- systemd = service manager  
- Processes = running programs  
- Logs + services = `journalctl` + `systemctl`  
