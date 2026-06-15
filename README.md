# Linux_Task_01_AkhilSPramod
Name: Akhil  

---
### Table of Contents
Part A: Linux Installation & Verification

Part B: Basic Navigation Commands

Part C: Directory Management

Part D: File Management

Part E: System Information Collection

Part F: Linux Research Activity
---
### Part A: Linux Installation & Verification
Chosen Distribution: Kali Linux (on VMware Workstation)
Kali Linux was selected because it is the industry-standard distribution for penetration testing and cybersecurity labs. It comes pre-installed with tools like Nmap, Metasploit, Wireshark, and Nessus.
Setup Details
Item	Details
Virtualization Software	VMware Workstation Pro
OS Installed	Kali Linux 2024.x (64-bit)
RAM Allocated	4 GB
Disk Space	40 GB
Network Adapter	NAT + Host-Only (dual adapter)
![kali](kali%20intro%201.png)

![kali desktop](kali%20intro%202.png)

![kali terminal](kali%20terminal%20.png)

---

Part B: Basic Navigation Commands
All commands executed in Kali Linux terminal (bash shell).
`pwd` — Print Working Directory
```bash
pwd
```
Purpose: Shows the absolute path of the current directory you are in.  
Output Example: `/home/kali`


---
`ls` — List Directory Contents
```bash
ls
```
Purpose: Lists all files and directories in the current location (non-hidden files only).  
Output Example: `Desktop Documents Downloads Music Pictures`
---
`ls -la` — Detailed List with Hidden Files
```bash
ls -la
```
Purpose:
`-l` = long format (shows permissions, owner, size, date)
`-a` = all files including hidden files (files starting with `.`)
Output Example:
```
total 64
drwxr-xr-x 15 kali kali 4096 Jun 10 10:00 .
drwxr-xr-x  3 root root 4096 Jun  1 09:00 ..
-rw-------  1 kali kali  220 Jun  1 09:00 .bash_history
-rw-r--r--  1 kali kali 3526 Jun  1 09:00 .bashrc
drwxr-xr-x  2 kali kali 4096 Jun 10 10:00 Desktop
```
---
`cd` — Change Directory
```bash
cd /home/kali
cd Desktop
cd ..        # go one level up
cd ~         # go to home directory
```
Purpose: Navigates between directories. Most fundamental Linux navigation command.
---
`clear` — Clear Terminal Screen
```bash
clear
```
Purpose: Clears all previous output from the terminal screen. Keyboard shortcut: `Ctrl + L`
---
`history` — Show Command History
```bash
history
```
Purpose: Lists all previously executed commands with line numbers. Useful for recalling or re-running past commands.
---
`whoami` — Show Current User
```bash
whoami
```
Purpose: Displays the username of the currently logged-in user.  
Output Example: `kali`
---
`hostname` — Show System Hostname
```bash
hostname
```
Purpose: Displays the name of the machine on the network.  
Output Example: `kali`
---
Command Summary Table
Command	Purpose
`pwd`	Show current directory path
`ls`	List files in current directory
`ls -la`	List all files with details and permissions
`cd`	Navigate between directories
`clear`	Clear terminal screen
`history`	Show list of past commands
`whoami`	Show current logged-in username
`hostname`	Show machine's network name
> 📸 Screenshots: See `/screenshots/part_b/`
---
Part C: Directory Management
Directory Structure Created
```
CyberSecurity_Lab/
│
├── Networking/
├── Linux/
├── CyberSecurity/
├── EthicalHacking/
└── Reports/
```
Commands Used
```bash
# Step 1: Create parent folder
mkdir CyberSecurity_Lab

# Step 2: Create all subfolders in one command
mkdir CyberSecurity_Lab/Networking \
      CyberSecurity_Lab/Linux \
      CyberSecurity_Lab/CyberSecurity \
      CyberSecurity_Lab/EthicalHacking \
      CyberSecurity_Lab/Reports

# Step 3: Verify structure
tree CyberSecurity_Lab
```
Command Reference
Command	Purpose
`mkdir <name>`	Create a new directory
`mkdir -p path/to/dir`	Create nested directories in one go
`cd <dir>`	Enter a directory
`tree <dir>`	Display folder structure visually
> 📸 Screenshots: See `/screenshots/part_c/`
---
Part D: File Management
Files Created Inside Each Folder
```bash
# Navigate into folder
cd CyberSecurity_Lab/Linux

# Create files
touch notes.txt
touch commands.txt
touch report.txt
```
File Operations Performed
1. Create Files
```bash
touch notes.txt
touch commands.txt
touch report.txt
```
`touch` — Creates an empty file. If file already exists, updates its timestamp.
---
2. Copy Files
```bash
cp notes.txt ../Networking/notes_backup.txt
```
`cp <source> <destination>` — Copies a file from one location to another.
---
3. Move Files
```bash
mv commands.txt ../CyberSecurity/commands.txt
```
`mv <source> <destination>` — Moves a file to a new location.
---
4. Rename Files
```bash
mv report.txt final_report.txt
```
`mv` is also used to rename files (move within same directory).
---
5. Delete Files
```bash
rm notes.txt
rm -r OldFolder/    # remove directory and its contents
```
`rm` — Removes files. `-r` flag removes directories recursively.
> ⚠️ `rm` is permanent. No Recycle Bin in Linux terminal.
---
File Command Summary Table
Command	Syntax	Purpose
`touch`	`touch file.txt`	Create empty file
`cp`	`cp src dst`	Copy file
`mv`	`mv src dst`	Move or rename file
`rm`	`rm file.txt`	Delete file
`rm -r`	`rm -r folder/`	Delete directory recursively
> 📸 Screenshots: See `/screenshots/part_d/`
---
Part E: System Information Collection
Commands Executed
```bash
uname -a
hostname
whoami
date
uptime
pwd
```
Output Reference
Command	Output / Description
`uname -a`	Full kernel info: `Linux kali 6.1.0-kali9-amd64 #1 SMP Debian 6.1.27-1kali1 x86_64 GNU/Linux`
`hostname`	`kali`
`whoami`	`kali`
`date`	`Mon Jun 10 10:30:00 IST 2026`
`uptime`	`10:30:00 up 1:23, 1 user, load average: 0.10, 0.08, 0.05`
`pwd`	`/home/kali`
System Details Recorded
Item	Value
Kernel Version	6.1.0-kali9-amd64
Username	kali
Current Directory	/home/kali
Current Date & Time	Mon Jun 10 10:30:00 IST 2026
System Uptime	1 hour 23 minutes
> 📸 Screenshots: See `/screenshots/part_e/`
---
Part F: Linux Research Activity
1. What is Linux?
Linux is a free and open-source operating system kernel created by Linus Torvalds in 1991. It is based on the Unix operating system design. The Linux kernel manages hardware resources (CPU, RAM, storage) and allows software to communicate with hardware.
Linux itself is just the kernel. When combined with tools, utilities, and a package manager, it forms a complete Linux Distribution (distro) like Ubuntu, Kali Linux, or Fedora.
Linux is widely used in servers, supercomputers, Android phones, embedded systems, routers, and cloud infrastructure.
---
2. Why is Linux Important in Cyber Security?
Linux is the backbone of cybersecurity for several reasons:
Most attack tools run on Linux — Nmap, Metasploit, Wireshark, Burp Suite, Aircrack-ng, John the Ripper are all Linux-native.
Open Source — Security professionals can inspect, modify, and understand every part of the OS.
Stability and Performance — Linux can run for months without rebooting, ideal for servers and security labs.
Powerful Terminal — Bash scripting allows automation of repetitive security tasks.
Privilege Control — Fine-grained file permissions (read/write/execute per user/group) model used in Unix-style systems is foundational to security concepts.
Used by attackers and defenders — Understanding Linux means you can think from both sides.
---
3. Difference Between Linux and Windows
Feature	Linux	Windows
Cost	Free and open-source	Paid license required
Source Code	Publicly available	Closed source (proprietary)
Security	Generally more secure, fewer viruses	More targeted by malware
Customization	Fully customizable	Limited customization
File System	ext4, XFS, Btrfs	NTFS, FAT32, exFAT
Terminal	Bash (powerful scripting)	CMD / PowerShell (less powerful)
Software Install	Package manager (apt, yum, pacman)	.exe installers or Store
Usage	Servers, hacking, embedded systems	Desktop users, gaming, enterprise
Updates	User-controlled	Forced automatic updates
Stability	Extremely stable	Prone to crashes over time
---
4. What is a Linux Distribution?
A Linux Distribution (distro) is a complete operating system built around the Linux kernel, bundled with:
A package manager
System utilities (GNU tools)
A desktop environment (optional)
Pre-installed software
Different distros are built for different purposes:
Distribution	Purpose
Ubuntu	General use, beginners
Kali Linux	Penetration testing, ethical hacking
Parrot OS	Privacy + security
CentOS / RHEL	Enterprise servers
Arch Linux	Advanced users, customization
Raspberry Pi OS	Embedded/IoT devices
All distros share the same Linux kernel but differ in tools, package managers, and target audience.
---
5. Why Do Ethical Hackers Prefer Linux-Based Operating Systems?
Ethical hackers prefer Linux for these key reasons:
Pre-built Hacking Tools — Kali Linux ships with 600+ security tools out of the box (Nmap, Metasploit, Hydra, Aircrack-ng, etc.)
Full Control — Root access gives complete control over the system, needed for packet crafting, raw socket manipulation, and exploit development.
Network Tool Support — Tools like Wireshark, tcpdump, and Scapy work natively on Linux.
Scripting Power — Bash + Python automation makes scanning and exploitation workflows efficient.
Live Boot Capability — Kali can run from USB without installation, leaving no trace on the target machine.
Anonymity Tools — Tools like Tor, ProxyChains, and MAC changer integrate better on Linux.
Same Environment as Targets — Most web servers, cloud instances, and IoT devices run Linux. Understanding it helps find real-world vulnerabilities.
Community and Exploit Databases — The cybersecurity community builds and shares tools primarily for Linux.
