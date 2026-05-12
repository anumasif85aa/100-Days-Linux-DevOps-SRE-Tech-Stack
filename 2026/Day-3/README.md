# Welcome to NIT Academy - Day 3

> Day-3: Monday 11th May, 2026

---

# Table of Contents

| Task | Title | Summary |
|------|------|------|
| 1 | [Open PowerShell as Administrator](#task-1---open-powershell-as-administrator) | Open elevated PowerShell |
| 2 | [Check if WSL is Installed](#task-2---check-if-wsl-is-already-installed) | Verify existing WSL installation |
| 3 | [Check Installed Linux Distros](#task-3---check-installed-linux-distros) | View installed Linux distributions |
| 4 | [Check Available Distros](#task-4---check-available-linux-distros) | View downloadable Linux distros |
| 5 | [Install WSL](#task-5---install-wsl-with-default-ubuntu) | Install WSL and Ubuntu |
| 6 | [Install Specific Distro](#task-6---install-a-specific-distro) | Install Ubuntu, Debian, etc. |
| 7 | [First Linux Setup](#task-7---first-linux-setup) | Create Linux username/password |
| 8 | [Start WSL Manually](#task-8---start-wsl-manually) | Launch Linux manually |
| 9 | [Verify Linux Is Working](#task-9---verify-linux-is-working) | Test Linux functionality |
| 10 | [Check WSL Version](#task-10---check-wsl-version) | Verify WSL 2 |
| 11 | [Convert Existing Distro to WSL2](#task-11---convert-an-existing-distro-to-wsl-2) | Upgrade distro version |
| 12 | [Set Default Distro](#task-12---set-default-distro) | Configure default Linux distro |
| 13 | [Shutdown and Restart WSL](#task-13---shutdown-and-restart-wsl) | Restart Linux environment |
| 14 | [Access Windows Files from Linux](#task-14---access-windows-files-from-wsl) | Access Windows drives |
| 15 | [Access Linux Files from Windows](#task-15---access-linux-files-from-windows) | Access Linux files from Explorer |
| 16 | [Common Commands](#task-16---common-commands-for-students) | Frequently used commands |
| 17 | [Common Problems and Fixes](#task-17---common-problems-and-fixes) | Beginner troubleshooting |
| 18 | [Final Verification Checklist](#task-18---final-student-verification-checklist) | Confirm installation success |

---

# What is WSL?

WSL (Windows Subsystem for Linux) is a feature in Windows that allows you to run a Linux environment directly inside Windows without requiring:

- Dual boot
- A separate virtual machine
- Additional hypervisors

This allows students to use Linux commands and development tools directly from Windows.

---

# Why Do We Need WSL?

Our goal is to provide Linux systems in an Open-Source environment without requiring students to purchase additional software or subscriptions.

WSL allows students to:

- Practice Linux commands
- Use Bash shell
- Run Linux tools
- Learn DevOps/Linux administration
- Access Linux directly from Windows

---

# Tasks Covered in This Guide

1. Install WSL
2. Install Ubuntu Linux
3. Check existing WSL installation
4. Verify Linux is working correctly
5. Fix common beginner issues

---

# Official Microsoft References

| Command | Purpose |
|------|------|
| `wsl --install` | Install WSL |
| `wsl --list --verbose` | List installed distros |
| `wsl --list --online` | List downloadable distros |

Source: Microsoft Learn

---

# Task 1 - Open PowerShell as Administrator

1. Open the **Start Menu**
2. Type:

```powershell
PowerShell
```

3. Right-click **Windows PowerShell**
4. Select:

```text
Run as administrator
```

---

# Task 2 - Check if WSL is Already Installed

Run:

```powershell
wsl --status
```

If WSL is installed, you may see:

- Default Distribution
- Default Version
- Kernel Version
- WSL Version

---

# Task 3 - Check Installed Linux Distros

Run:

```powershell
wsl --list --verbose
```

Short version:

```powershell
wsl -l -v
```

Example output:

```text
  NAME      STATE           VERSION
* Ubuntu    Stopped         2
```

## Explanation

| Column | Meaning |
|------|------|
| NAME | Installed Linux distro |
| STATE | Running or stopped |
| VERSION | WSL version |
| `*` | Default distro |

If Ubuntu appears, WSL is already installed.

---

# Task 4 - Check Available Linux Distros

Run:

```powershell
wsl --list --online
```

Short version:

```powershell
wsl -l -o
```

Example:

```text
NAME            FRIENDLY NAME
Ubuntu          Ubuntu
Debian          Debian GNU/Linux
kali-linux      Kali Linux Rolling
openSUSE        openSUSE Leap
```

---

# Task 5 - Install WSL with Default Ubuntu

Run:

```powershell
wsl --install
```

This installs:

- WSL
- Ubuntu
- WSL 2

Restart your computer if prompted.

---

# Task 6 - Install a Specific Distro

Install Ubuntu:

```powershell
wsl --install -d Ubuntu
```

Install Debian:

```powershell
wsl --install -d Debian
```

To view valid distro names:

```powershell
wsl --list --online
```

---

# Task 7 - First Linux Setup

After installation, Linux will ask for:

```text
Enter new UNIX username:
New password:
Retype new password:
```

Example username:

```text
student
```

## Important Notes

- Linux username does NOT need to match Windows username
- Password characters will NOT appear while typing
- Do NOT forget your password

---

# Task 8 - Start WSL Manually

Start default distro:

```powershell
wsl
```

Start Ubuntu directly:

```powershell
wsl -d Ubuntu
```

---

# Task 9 - Verify Linux is Working

Inside Linux, run:

```bash
whoami
pwd
uname -a
cat /etc/os-release
```

Expected output example:

```text
NAME="Ubuntu"
VERSION="24.04 LTS"
```

---

# Update Linux Packages

Run:

```bash
sudo apt update
```

Then:

```bash
sudo apt upgrade -y
```

---

# Task 10 - Check WSL Version

Run:

```powershell
wsl --version
```

Also verify distro version:

```powershell
wsl -l -v
```

Expected:

```text
VERSION
2
```

Example:

```text
  NAME      STATE           VERSION
* Ubuntu    Stopped         2
```

---

# Set WSL 2 as Default

Run:

```powershell
wsl --set-default-version 2
```

---

# Task 11 - Convert an Existing Distro to WSL 2

If your distro shows VERSION 1:

```powershell
wsl --set-version Ubuntu 2
```

Replace `Ubuntu` with your distro name.

Verify again:

```powershell
wsl -l -v
```

---

# Task 12 - Set Default Distro

If multiple distros are installed:

```powershell
wsl --set-default Ubuntu
```

Now running:

```powershell
wsl
```

will open Ubuntu automatically.

---

# Task 13 - Shutdown and Restart WSL

Shutdown WSL:

```powershell
wsl --shutdown
```

Restart Ubuntu:

```powershell
wsl -d Ubuntu
```

---

# Task 14 - Access Windows Files from WSL

Windows drives are mounted under:

```bash
/mnt
```

Example:

```bash
cd /mnt/c/Users
```

List files:

```bash
ls
```

---

# Task 15 - Access Linux Files from Windows

Open File Explorer and type:

```text
\\wsl$
```

Example:

```text
\\wsl$\Ubuntu
```

---

# Task 16 - Common Commands for Students

| Task | Command |
|------|------|
| Check WSL status | `wsl --status` |
| List installed distros | `wsl -l -v` |
| List online distros | `wsl -l -o` |
| Install WSL | `wsl --install` |
| Install Ubuntu | `wsl --install -d Ubuntu` |
| Start WSL | `wsl` |
| Start Ubuntu | `wsl -d Ubuntu` |
| Shutdown WSL | `wsl --shutdown` |
| Set WSL2 default | `wsl --set-default-version 2` |
| Set default distro | `wsl --set-default Ubuntu` |

---

# Task 17 - Common Problems and Fixes

## Problem 1 - `wsl` Command Not Recognized

Try:

1. Restart computer
2. Open PowerShell as Administrator
3. Run:

```powershell
wsl --install
```

---

## Problem 2 - No Linux Distro Installed

Check installed distros:

```powershell
wsl -l -v
```

View downloadable distros:

```powershell
wsl -l -o
```

Install Ubuntu:

```powershell
wsl --install -d Ubuntu
```

---

## Problem 3 - Ubuntu Opens Then Closes

Run:

```powershell
wsl -d Ubuntu
```

Copy any error message and send it to the instructor.

---

## Problem 4 - Forgot Linux Password

Open root shell:

```powershell
wsl -u root
```

Reset password:

```bash
passwd username
```

Example:

```bash
passwd student
```

Exit:

```bash
exit
```

---

## Problem 5 - Distro is WSL 1 Instead of WSL 2

Check:

```powershell
wsl -l -v
```

Convert:

```powershell
wsl --set-version Ubuntu 2
```

---

# Task 18 - Final Student Verification Checklist

Run:

```powershell
wsl --status
```

```powershell
wsl -l -v
```

Start Ubuntu:

```powershell
wsl -d Ubuntu
```

Inside Linux:

```bash
whoami
pwd
cat /etc/os-release
sudo apt update
```

If all commands work successfully, WSL is installed correctly.

---

# Final Summary

Recommended installation:

```powershell
wsl --install -d Ubuntu
```

Recommended updates:

```bash
sudo apt update
sudo apt upgrade -y
```

Recommended verification:

```powershell
wsl -l -v
```

Expected result:

```text
Ubuntu    Running or Stopped    2
```

This confirms Ubuntu is installed successfully using WSL 2.