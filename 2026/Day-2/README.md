# Welcome to NIT Academy - Day 2

> Day-2: Sunday 10th May, 2026

## Table of Contents

| Task | Title | Summary |
|------|------|------|
| 1 | [Access your Virtual Machine](#task-1---access-your-virtual-machine) | Introduction to Unix/Linux |
| 2 | [What is Linux Shell?](#task-2---what-is-linux-shell) | Login to Virtual Machine and access the Linux Command Line (CLI) |
| 3 | [Register a GitHub Account](#task-3---register-a-github-account) | Create your GitHub account |
| 4 | [Register or Update LinkedIn](#task-4---register-or-update-linkedin) | Create or improve LinkedIn profile |
| 5 | [Install Git Bash](#task-5---git-bash) | Install Git Bash on Windows |
| 6 | [Visual Studio Code](#task-6---visual-studio-code) | Install Visual Studio Code |
| 7 | [Discord](#task-7---discord) | Install and join Discord |

---
# We are now starting our Linux Journey
Please take this seriously and complete all assignments on time.

# Task 1 - Access your Virtual Machine?
1. Accessing Xen-Orchestra
Click the link below to access the login-page\
[Xen-Orchestra](https://labs.nit.academy)

<img src="../../.github/assets/XO-LOGIN.jpg" width="500">\
Enter your Credentials:
```Text
Username:
Password:
```
2. Navigating your Virtual Machine (VM) Console
Click on the virtual machine that has a "green" dot:\
<img src="../../.github/assets/XO-VM.jpg" width="700">

Review your Virtual Machine Resources:\
<img src="../../.github/assets/XO-VM-CONSOLE.jpg" width="700">

Click on tab "Console":\
<img src="../../.github/assets/XO-LINUX-VM.jpg" width="700">
```Text
Step1 - Click in the "Black Box"
Step2 - Hit the "Enter Key"
```
<img src="../../.github/assets/XO-VM-LOGIN.jpg" width="700">

```bash
   unknowna1alsdjfals5 Login: root
   Password: abc
   Last login: Sat Apr 18 02:51:09 on tty1
```
3. Let us fix this IPv6 overflow issue.
When we learn Networking we will come to understand:
- ip4 vs ipv6
- Importance of Static IP
- Troubleshooting Networking Issues

## Let us fix this issue. Type the following comands in your Virtual Machine (Black Box):

```bash
sysctl -w net.ipv6.conf.all.disable_ipv6=1
```
```bash
sysctl -w net.ipv6.conf.default.disable_ipv6=1
```
### Task is now complete!

# Task 2 - What is Linux Shell?

1. **The Shell (The Interface)**  
   Think of the Shell as the "outer layer" of the operating system (like a shell on a nut). It is the environment where you type your instructions.

   **Analogy:**  
   The Shell is like a chat window between you and the computer. You type something, and it waits for the computer to respond.

2. **The Interpreter (The Translator)**  
   The Interpreter is the program running inside the shell. Computers don't speak English; they speak binary (1s and 0s). The interpreter takes the human-readable words you type and translates them into a language the computer's "brain" (the kernel) understands.

   **Analogy:**  
   The Interpreter is a translator sitting between two people who speak different languages.

3. **The Command Line (The Action)**  
   The Command Line is simply the specific line of text you type to get a job done. It usually follows a simple "Verb + Object" structure.

   Example:
   ```bash
   <root@vm1>#whoami
   ```
   ## The "First Thirteen" Commands

| Command | What it does | Why it matters |
|----------|---------------|----------------|
| `whoami` | Displays your username. | Confirms **who** is talking to the system. |
| `pwd` | **Print** Working Directory. | Tells you **where** you are in the folder system. |
| `ls` | **List** files. | Shows you **what** is inside your current folder. |
| `date` | Displays current time/date. | Simple proof that the **Interpreter** is working. |
| `clear` | Wipes the screen clean. | Essential for reducing "command line anxiety." |
| `ip a` | Displays network interfaces and IP addresses. | Helps you identify your machine on the network. |
| `hostnamectl` | Displays system hostname and operating system details. | Helps identify the machine and system information. |
| `hostnamectl set-hostname <your-hostname>` | Changes the system hostname. | Useful for naming servers and organizing systems in a network or lab. |
| `uptime` | Shows how long the system has been running. | Helps monitor system stability and workload. |
| `dnf update -y` | updates RPM repositories. | Helps to bring all your respositories and versions to current status. |
| `passwd` | Changes a user password. | Essential for account security and user management. |
| `/bin/bash` | Launches a new Bash shell (typically a non-login shell). | Useful for entering a shell environment or troubleshooting. |
| `exit` | Closes the current shell session. | Safely logs out or exits the terminal session. |
   
# Task 3 - Register a GitHub Account
### GIT stands for "Global Information Tracker"
Click on the link https://github.com/
## GitHub Account Setup Steps

| Step | Action | Description |
|------|---------|-------------|
| 1 | Open GitHub Website | Go to https://github.com |
| 2 | Click Sign Up | Press the **Sign up** button on the homepage |
| 3 | Enter Information | Add your email, username, and password |
| 4 | Verify Email | Open your email and click the verification link |
| 5 | Complete Profile | Add profile details if desired |
| 6 | Login | Sign in to your new GitHub account |
| 7 | Create Repository | Click **+** → **New repository** |
| 8 | Add Repository Name | Enter a project/repository name |
| 9 | Initialize README | Check **Add README file** |
| 10 | Create Repository | Click **Create repository** |

# Task 4 - Register or Update Linkedin
Click on the link https://www.linkedin.com/\
Create your account on linkedin
# Task 5 - Git Bash
Click on the link https://git-scm.com/install/windows
## Git Bash Setup Steps

| Step | Action | Description |
|------|---------|-------------|
| 1 | Download Git Bash | Go to https://git-scm.com/download/win |
| 2 | Run Installer | Open downloaded `.exe` file |
| 3 | Start Installation | Click **Next** through setup |
| 4 | Choose PATH Option | Select: **Git from command line and also from 3rd-party software** |
| 5 | HTTPS Backend | Select: **Use the OpenSSL library** |
| 6 | Line Ending Option | Select: **Checkout Windows-style, commit Unix-style line endings** |
| 7 | Install Git | Click **Install** |
| 8 | Finish Setup | Click **Finish** |
| 9 | Open Git Bash | Launch Git Bash from Start Menu |
| 10 | Verify Installation | Run `git --version` |
| 11 | Configure Username | Run `git config --global user.name "Your Name"` |
| 12 | Configure Email | Run `git config --global user.email "you@example.com"` |
| 13 | Verify Config | Run `git config --list` |
| 14 | Generate SSH Key | Run `ssh-keygen -t ed25519 -C "you@example.com"` |
| 15 | Add SSH Key to GitHub | Copy public key to GitHub SSH settings |
| 16 | Test Connection | Run `ssh -T git@github.com` |

# Task 6 - Visual Studio Code
Click on the following link https://code.visualstudio.com/download

# Task 7 - Discord
!! IMPORTANT !!

As stated prior, the discord server is ready for everyone at Nexus to join! Please join through this link: https://discord.gg/UeVHUzz25A

Please also note that we will be using Discord regularly as an additional form of communication alongside Whatsapp

# Final Summary
Today you learned:

- Accessing Virtual Machines
- Linux Shell basics
- Basic Linux commands
- Creating GitHub accounts
- Installing Git Bash
- Installing VS Code
- Setting up Discord

Welcome to your Linux journey at NIT Academy!