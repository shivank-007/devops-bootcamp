# 🐧 Day 1 - Linux Fundamentals

> **Author:** Shivank Srivastava  
> **Bootcamp:** 10-Day DevOps Bootcamp  
> **Day:** 1

---

# 📖 Introduction

Linux is one of the most popular open-source operating systems in the world. It is widely used in servers, cloud platforms, DevOps, cybersecurity, networking, embedded systems, and enterprise applications.

Most cloud providers such as AWS, Azure and Google Cloud use Linux-based servers because Linux is secure, stable, lightweight and highly customizable.

For a DevOps Engineer, Linux is the first and most important skill because almost every production server runs Linux.

---

# Module 1 — Linux Introduction

## What is Linux?

Linux is an open-source operating system kernel created by Linus Torvalds in 1991.

An Operating System is software that acts as a bridge between the user and computer hardware.

Example:

User
↓
Linux Shell (Bash)
↓
Linux Kernel
↓
Hardware

---

## Why Linux?

Linux is preferred because it is:

- Free and Open Source
- Secure
- Stable
- Fast
- Multi-user
- Multi-tasking
- Highly Customizable
- Powerful Command Line Interface

---

## Where is Linux Used?

Linux is used in:

- Web Servers
- Cloud Computing
- DevOps
- Docker
- Kubernetes
- Android
- Banking Systems
- Supercomputers
- Networking Devices

---

## Popular Linux Distributions

| Distribution | Purpose |
|--------------|----------|
| Ubuntu | Beginners & Servers |
| Debian | Stable Systems |
| CentOS | Enterprise Servers |
| Red Hat Enterprise Linux | Commercial Enterprise |
| Rocky Linux | Enterprise |
| Kali Linux | Cyber Security |
| Arch Linux | Advanced Users |

---

## Linux Architecture

```

User

↓

Shell (Bash)

↓

Kernel

↓

Hardware

```

### User

The person who interacts with the computer.

### Shell

The command interpreter.

Example:

```bash
pwd
ls
mkdir
```

The shell converts user commands into instructions that the kernel understands.

### Kernel

Kernel is the core of the operating system.

Responsibilities:

- Memory Management
- Process Management
- CPU Scheduling
- Device Management
- File System Management

---

# Module 2 — Linux File System

## What is Linux File System?

Linux stores everything inside a hierarchical directory structure.

Everything in Linux is treated as a file.

The highest directory is called the Root Directory.

```

/

```

All other directories start from here.

---

## Important Directories

### /

Root Directory

The starting point of the Linux File System.

---

### /home

Stores personal files of users.

Example:

```

/home/shivank

```

---

### /etc

Contains system configuration files.

Examples:

- passwd
- hostname
- hosts
- ssh configuration

---

### /var

Stores variable data.

Examples:

- Logs
- Cache
- Mail
- Databases

---

### /usr

Contains installed applications and libraries.

---

### /tmp

Stores temporary files.

Linux automatically clears this directory after reboot in many distributions.

---

### /bin

Contains essential Linux commands.

Examples:

```

ls

cp

mv

cat

```

---

### /sbin

Contains system administration commands.

Usually used by the root user.

Examples:

```

reboot

shutdown

fsck

```

---

### /dev

Contains device files.

Example:

Hard Disk

USB

Keyboard

Mouse

---

### /proc

Virtual file system containing process and kernel information.

Example:

CPU Information

Memory Information

Running Processes

---

## Interview Questions

### Q1. What is Linux?

Linux is an open-source operating system kernel used in servers, cloud computing and DevOps.

### Q2. Why is Linux preferred in DevOps?

Because it is secure, stable, lightweight, free and almost all cloud servers use Linux.

### Q3. What is the root directory?

The root directory (/) is the top-most directory of the Linux File System.

### Q4. What is stored inside /etc?

Configuration files.

---

# ✅ Module 1 & 2 Completed

---

# Module 3 — Linux Core Commands

Core commands are the basic commands that every Linux user must know. They help users navigate directories, create files, read file contents, and manage the file system.

---

## 1. pwd (Present Working Directory)

### What is pwd?

The `pwd` command displays the absolute path of the current working directory.

### Why do we use it?

Before creating, deleting, or editing files, it is important to know where you are currently working.

### Syntax

```bash
pwd
```

### Example

```bash
$ pwd
/home/shivank/Desktop/devops-bootcamp
```

### Output Explanation

- `/home` → Home directory
- `shivank` → User folder
- `Desktop` → Desktop folder
- `devops-bootcamp` → Current project directory

### Real-world Use

Before deploying applications or deleting files, DevOps engineers always verify their current location.

---

## 2. ls (List)

### What is ls?

Displays files and directories.

### Syntax

```bash
ls
```

Useful options

```bash
ls -l
ls -a
ls -lh
```

### Options

`-l` → Long listing

`-a` → Hidden files

`-h` → Human readable file size

---

## 3. cd (Change Directory)

Changes the current directory.

### Syntax

```bash
cd foldername
```

Examples

```bash
cd Documents

cd ..

cd ~

cd /
```

---

## 4. mkdir

Creates a new directory.

### Syntax

```bash
mkdir Project
```

Create multiple directories

```bash
mkdir -p DevOps/Linux/Notes
```

### Why use -p?

Creates parent directories automatically.

---

## 5. rmdir

Deletes an empty directory.

```bash
rmdir Demo
```

---

## 6. touch

Creates an empty file.

```bash
touch notes.txt
```

Create multiple files

```bash
touch file1 file2 file3
```

---

## 7. cat

Displays file contents.

```bash
cat notes.txt
```

Also used to combine files.

---

## 8. less

Displays large files page by page.

Useful for reading log files.

```bash
less /var/log/syslog
```

Exit

```
q
```

---

## 9. more

Similar to less but with fewer features.

---

## 10. clear

Clears the terminal screen.

```bash
clear
```

Shortcut

```
Ctrl + L
```

---

## 11. history

Shows previously executed commands.

```bash
history
```

Useful during troubleshooting.

---

## 12. man

Displays command documentation.

```bash
man ls
```

Exit

```
q
```

---

# Module 4 — File Operations

File operations help manage files and directories.

---

## cp (Copy)

Copies files or folders.

Syntax

```bash
cp source destination
```

Example

```bash
cp notes.txt backup.txt
```

Copy folder

```bash
cp -r Project Backup
```

`-r` means Recursive.

---

## mv (Move)

Moves or renames files.

Example

Rename

```bash
mv old.txt new.txt
```

Move

```bash
mv notes.txt Documents/
```

---

## rm (Remove)

Deletes files.

```bash
rm file.txt
```

Delete folder

```bash
rm -r Folder
```

Force delete

```bash
rm -rf Folder
```

⚠️ **Warning:** Never run `rm -rf /` because it attempts to remove the entire filesystem.

---

## find

Searches files by name.

Example

```bash
find . -name "*.txt"
```

Search from root

```bash
find / -name git
```

---

## locate

Quickly searches files using a prebuilt database.

```bash
locate bashrc
```

If results are outdated, update the database:

```bash
sudo updatedb
```

---

## whereis

Shows the location of commands, binaries, source files and manuals.

```bash
whereis git
```

Example Output

```
git: /usr/bin/git /usr/share/man/man1/git.1.gz
```

---

## file

Identifies file type.

Example

```bash
file hello.sh
```

Output

```
Bourne-Again shell script
```

---

# Interview Questions

### What is the difference between cp and mv?

- `cp` creates a copy.
- `mv` moves or renames the original file.

---

### What is the difference between rm and rmdir?

- `rm` deletes files (and directories with `-r`).
- `rmdir` deletes only empty directories.

---

### Why do we use mkdir -p?

To create nested directories in a single command.

---

### Difference between less and cat?

- `cat` displays the entire file at once.
- `less` displays the file page by page and is better for large files.

---

# ✅ Module 3 & 4 Completed

---
---

# Module 5 — Linux File Permissions

## What are File Permissions?

Linux is a multi-user operating system. To keep files secure, Linux controls who can read, write, or execute a file using **permissions**.

Every file and directory has an owner, a group, and permissions assigned to them.

---

## Permission Types

Linux uses three basic permissions:

| Permission | Symbol | Meaning |
|------------|--------|---------|
| Read | r | View file contents |
| Write | w | Modify or delete the file |
| Execute | x | Run the file as a program |

---

## Permission Categories

Permissions are divided into three groups:

| Category | Meaning |
|----------|---------|
| User (u) | Owner of the file |
| Group (g) | Users in the same group |
| Others (o) | Everyone else |

Example:

```bash
-rwxr-xr--
```

Breakdown:

```
-        → File type
rwx      → Owner
r-x      → Group
r--      → Others
```

---

## Understanding Numeric Permissions

Linux also represents permissions using numbers.

| Number | Permission |
|--------|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

Examples:

### 755

Owner

```
rwx
```

Group

```
r-x
```

Others

```
r-x
```

### 644

Owner

```
rw-
```

Group

```
r--
```

Others

```
r--
```

---

## chmod (Change Mode)

Changes file permissions.

### Syntax

```bash
chmod permissions filename
```

Example

```bash
chmod 755 script.sh
```

Symbolic Method

```bash
chmod u+x script.sh
```

Remove permission

```bash
chmod g-w file.txt
```

---

## chown (Change Owner)

Changes file ownership.

Syntax

```bash
sudo chown username filename
```

Example

```bash
sudo chown shivank notes.txt
```

Change owner and group together

```bash
sudo chown shivank:developers notes.txt
```

---

## chgrp (Change Group)

Changes the group of a file.

Syntax

```bash
sudo chgrp developers notes.txt
```

---

## Viewing Permissions

```bash
ls -l
```

Example Output

```text
-rw-r--r-- 1 shivank shivank 120 notes.txt
```

Explanation

- File Type → -
- Owner Permission → rw-
- Group Permission → r--
- Others Permission → r--

---

## Real-world Example

Suppose a Bash deployment script needs to be executed.

Initially:

```bash
-rw-r--r--
```

Running the script:

```bash
./deploy.sh
```

Error

```
Permission denied
```

Solution

```bash
chmod +x deploy.sh
```

Now execute

```bash
./deploy.sh
```

---

## Best Practices

✔ Never use **777** unless absolutely necessary.

✔ Give minimum required permissions.

✔ Use **755** for scripts.

✔ Use **644** for text/configuration files.

---

# Module 6 — Package Management

## What is Package Management?

Package management allows users to install, update, remove and manage software.

Ubuntu uses the **APT Package Manager**.

---

## apt update

Updates the package index.

```bash
sudo apt update
```

It downloads the latest package information but **does not install updates**.

---

## apt upgrade

Installs the latest versions of installed packages.

```bash
sudo apt upgrade
```

Difference:

| Command | Purpose |
|----------|----------|
| apt update | Refresh package list |
| apt upgrade | Upgrade installed software |

---

## apt install

Installs software.

Example

```bash
sudo apt install git
```

---

## apt remove

Removes software but keeps configuration files.

```bash
sudo apt remove git
```

---

## apt purge

Removes software along with configuration files.

```bash
sudo apt purge git
```

---

## Difference between remove and purge

| remove | purge |
|---------|--------|
| Removes application | Removes application + configuration files |

---

## dpkg

Low-level package management tool.

List installed packages

```bash
dpkg -l
```

Check Git installation

```bash
dpkg -l | grep git
```

Meaning

- Shows installed packages.
- Filters only packages related to Git.

---

## Real-world Example

Before starting GitHub work, verify Git installation.

```bash
dpkg -l | grep git
```

If Git is missing:

```bash
sudo apt install git
```

---

# Interview Questions

### Difference between apt update and apt upgrade?

- `apt update` refreshes the package list.
- `apt upgrade` installs newer versions of installed packages.

---

### Difference between apt remove and apt purge?

- `remove` keeps configuration files.
- `purge` removes both application and configuration files.

---

### What does chmod do?

Changes file permissions.

---

### What does chown do?

Changes file ownership.

---

### Why should we avoid chmod 777?

It gives full permissions to everyone, creating security risks.

---

# ✅ Module 5 & 6 Completed

---

# Module 7 — Linux Networking Fundamentals

## What is Networking?

Networking is the process of connecting two or more computers or devices so they can communicate and share resources.

In DevOps, networking is essential because servers, applications, databases, and cloud services constantly communicate over a network.

---

# Important Networking Concepts

## IP Address

An IP (Internet Protocol) Address is a unique address assigned to every device connected to a network.

Example

```
192.168.1.10
```

or

```
10.203.45.20
```

Both are valid private IP addresses.

---

## Public IP vs Private IP

| Public IP | Private IP |
|------------|------------|
| Accessible over the Internet | Used inside local networks |
| Assigned by ISP | Assigned by Router/DHCP |
| Unique globally | Can repeat in different networks |

Private IP ranges

```
10.0.0.0 – 10.255.255.255

172.16.0.0 – 172.31.255.255

192.168.0.0 – 192.168.255.255
```

---

## localhost

```
127.0.0.1
```

localhost always points to your own computer.

It is used to test applications running on your local machine.

---

# Networking Commands

## ip a

Displays network interfaces and IP addresses.

Syntax

```bash
ip a
```

Example Output

```
2: eth0
inet 10.203.45.20/24
```

Explanation

- eth0 → Network Interface
- inet → IPv4 Address
- /24 → Subnet Mask

---

## ifconfig

Shows network configuration.

```bash
ifconfig
```

Older Linux systems use ifconfig.

Modern Linux uses **ip a** instead.

---

## ping

Checks network connectivity.

Syntax

```bash
ping google.com
```

Send only four packets

```bash
ping -c 4 google.com
```

Meaning of **-c 4**

Only four ICMP packets will be sent.

---

## curl

Transfers data from servers.

Check only HTTP headers

```bash
curl -I https://google.com
```

Returns

- HTTP Status Code
- Server
- Date
- Content-Type

without downloading the page.

---

## wget

Downloads files from the Internet.

Example

```bash
wget https://example.com/file.zip
```

Useful for downloading software packages.

---

## ss

Displays active network connections.

```bash
ss -tuln
```

Meaning

```
t → TCP

u → UDP

l → Listening Ports

n → Numeric Output
```

---

## Why is ss replacing netstat?

Because

- Faster
- Uses less memory
- More accurate
- Installed by default on modern Linux

---

# DNS

DNS converts

```
google.com
```

into

```
142.x.x.x
```

Without DNS we would need to remember IP addresses instead of domain names.

---

# Real-world Example

Suppose users cannot access your web server.

Steps

1.

```bash
ping google.com
```

Check Internet.

2.

```bash
ip a
```

Check IP address.

3.

```bash
ss -tuln
```

Verify whether the web server is listening on Port 80 or 443.

---

# Module 8 — User Management

Linux supports multiple users.

Each user has

- Username
- Password
- Home Directory
- Group

---

## useradd

Creates a new user.

```bash
sudo useradd rahul
```

Create home directory

```bash
sudo useradd -m rahul
```

---

## passwd

Sets or changes password.

```bash
sudo passwd rahul
```

---

## usermod

Modifies existing user.

Example

Add user to sudo group.

```bash
sudo usermod -aG sudo rahul
```

Meaning

```
-a → Append

-G → Secondary Group
```

---

## userdel

Deletes user.

```bash
sudo userdel rahul
```

Delete user along with home directory

```bash
sudo userdel -r rahul
```

---

## groups

Shows groups of a user.

```bash
groups
```

or

```bash
groups rahul
```

---

## whoami

Displays current logged-in user.

```bash
whoami
```

---

## id

Displays detailed user information.

```bash
id
```

Example

```
uid=1000(shivank)

gid=1000(shivank)

groups=1000(shivank),27(sudo)
```

---

# User Management Lab

Create User

```bash
sudo useradd -m testuser
```

Set Password

```bash
sudo passwd testuser
```

Check User

```bash
id testuser
```

Delete User

```bash
sudo userdel -r testuser
```

---

# Interview Questions

### What does ip a display?

It displays network interfaces and IP addresses.

---

### Why do we use ping -c 4?

To send only four ICMP packets instead of continuous ping.

---

### What does curl -I return?

Only HTTP response headers.

---

### Why is ss preferred over netstat?

Because it is faster, modern, and provides more efficient socket information.

---

### Difference between useradd and usermod?

- useradd creates a new user.
- usermod modifies an existing user.

---

### What does passwd do?

Sets or changes a user's password.

---

# ✅ Module 7 & 8 Completed

---

# Module 9 — Bash Scripting & Linux Services

## What is Bash?

Bash (Bourne Again Shell) is the default command-line shell in most Linux distributions. It allows users to execute commands, automate repetitive tasks, and write scripts.

A Bash script is simply a text file containing Linux commands that can be executed together.

Example:

```bash
#!/bin/bash

echo "Hello DevOps"
```

Save as:

```bash
hello.sh
```

Give execute permission:

```bash
chmod +x hello.sh
```

Run:

```bash
./hello.sh
```

Output:

```
Hello DevOps
```

---

## Variables

Variables store values.

Example

```bash
#!/bin/bash

name="Shivank"

echo $name
```

Output

```
Shivank
```

---

## User Input

```bash
#!/bin/bash

echo "Enter your name"

read name

echo "Welcome $name"
```

---

## If Statement

```bash
#!/bin/bash

age=20

if [ $age -ge 18 ]
then
    echo "Eligible"
fi
```

---

## If Else

```bash
#!/bin/bash

age=16

if [ $age -ge 18 ]
then
    echo "Adult"
else
    echo "Minor"
fi
```

---

## For Loop

```bash
for i in {1..5}
do
echo $i
done
```

Output

```
1
2
3
4
5
```

---

## While Loop

```bash
count=1

while [ $count -le 5 ]
do
echo $count
count=$((count+1))
done
```

---

## Functions

```bash
hello(){

echo "Welcome to DevOps"

}

hello
```

---

## Arguments

```bash
echo $1
echo $2
```

Run

```bash
./script.sh Shivank MCA
```

Output

```
Shivank

MCA
```

---

# Linux Service Management

Linux services run in the background.

Examples

- SSH
- Docker
- Jenkins
- Apache
- Nginx

---

## systemctl

Check service

```bash
systemctl status ssh
```

Start service

```bash
sudo systemctl start ssh
```

Stop

```bash
sudo systemctl stop ssh
```

Restart

```bash
sudo systemctl restart ssh
```

Enable

```bash
sudo systemctl enable ssh
```

Disable

```bash
sudo systemctl disable ssh
```

---

## journalctl

Displays system logs.

View logs

```bash
journalctl
```

Latest logs

```bash
journalctl -xe
```

Logs for SSH

```bash
journalctl -u ssh
```

---

## Cron Jobs

Cron automates tasks.

Open cron

```bash
crontab -e
```

Example

```
0 8 * * * /home/shivank/backup.sh
```

Meaning

Every day at 8 AM execute backup.sh

---

# Git & GitHub Commands

## git clone

Downloads an existing GitHub repository.

```bash
git clone https://github.com/user/repo.git
```

---

## git status

Shows repository status.

```bash
git status
```

---

## git add

Adds changes to staging area.

```bash
git add .
```

---

## git commit

Creates a snapshot of current changes.

```bash
git commit -m "Added Linux notes"
```

---

## git push

Uploads commits to GitHub.

```bash
git push
```

---

## git pull

Downloads latest changes from GitHub.

```bash
git pull origin main
```

---

## git log

Shows commit history.

```bash
git log --oneline
```

---

# Git vs GitHub

| Git | GitHub |
|------|---------|
| Version Control System | Cloud Hosting Platform |
| Tracks Changes | Stores Repositories |
| Local Machine | Online Platform |

---

# Linux Commands Cheat Sheet

```bash
pwd
ls
cd
mkdir
touch
cp
mv
rm
find
chmod
chown
chgrp
grep
sort
uniq
wc
ps
top
kill
apt update
apt upgrade
ip a
ping
curl
wget
ss
useradd
passwd
usermod
userdel
git status
git add .
git commit -m
git push
```

---

# Common Interview Questions

### What is Linux?

An open-source operating system kernel used in servers, cloud computing, and DevOps.

---

### What is Bash?

A command-line shell used to execute Linux commands and scripts.

---

### Difference between Git and GitHub?

Git is a version control system.

GitHub is a cloud platform that hosts Git repositories.

---

### Why do we use git commit?

To save a snapshot of changes in the repository.

---

### Why do we use git push?

To upload local commits to GitHub.

---

### What does git clone do?

Downloads an existing remote repository to your local machine.

---

### What is systemctl?

A command used to manage Linux services.

---

### What is journalctl?

A command used to view system logs managed by systemd.

---

### Why are cron jobs used?

To automate repetitive tasks like backups, updates, and maintenance.

---

# Mini Lab

✔ Create a directory

✔ Create files using touch

✔ Copy files

✔ Move files

✔ Delete files

✔ Change permissions

✔ Create a user

✔ Set password

✔ Check IP Address

✔ Test Internet using ping

✔ Install Git

✔ Create Git Repository

✔ Push Repository to GitHub

✔ Write Bash Script

✔ Execute Bash Script

---

# Day 1 Summary

Today I learned:

- Linux Basics
- Linux Architecture
- Linux File System
- Core Linux Commands
- File Operations
- Permissions
- Package Management
- Networking Basics
- User Management
- Bash Scripting
- Linux Service Management
- Git & GitHub Fundamentals

---

# Skills Gained

✅ Linux Basics

✅ Command Line Navigation

✅ File Management

✅ User Management

✅ Networking Basics

✅ Bash Scripting

✅ Package Management

✅ Git & GitHub

---

# Author

**Shivank Srivastava**

MCA (2025)

Aspiring Linux | Cloud | DevOps Engineer

GitHub: https://github.com/YOUR_USERNAME

---

> 📌 Day 1 Completed Successfully.




























