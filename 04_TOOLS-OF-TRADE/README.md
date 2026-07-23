# 🐧 Course 4 — Tools of the Trade: Linux and SQL

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Platform](https://img.shields.io/badge/Platform-Coursera-0056D2)
![Issuer](https://img.shields.io/badge/Issuer-Google-4285F4)

> Learning the essential tools every entry-level cybersecurity analyst uses daily.
> This course focuses on Linux system administration, the Bash shell, user and permission management, and SQL for querying security data.

---

# 📑 Module Index

- Module 1 — Introduction to Operating Systems
- Module 2 — The Linux Operating System
- Module 3 — Linux Commands in the Bash Shell
- Module 4 — Database & SQL *(In Progress)*

---

# 📘 Module 1 — Operating Systems Fundamentals

## What This Module Covers

An introduction to operating systems, how they interact with hardware and applications, and how processes and memory are managed.

## Key Concepts Learned

### 💻 Operating System

- Interface between hardware and software
- First software loaded during system boot
- Responsible for process execution and memory management

### ⚙️ Process Management

- Processes are programs currently being executed
- Operating system schedules and manages multiple running processes

### 🧠 Memory Management

- Allocates and frees memory for applications
- Prevents conflicts between running processes
- Improves stability and efficiency

---

# 📘 Module 2 — Linux Fundamentals

## What This Module Covers

Introduction to Linux, why it is widely used in cybersecurity, and the architecture of a Linux operating system.

## Key Concepts Learned

### 🐧 Linux

- Open-source operating system
- Commonly used for servers, cloud platforms, penetration testing and security operations

### 📦 Linux Distributions

Examples include:

- Ubuntu
- Debian
- Kali Linux
- Fedora
- Red Hat Enterprise Linux

### ⚙️ Linux Architecture

```
User
↓
Applications
↓
Shell
↓
Filesystem Hierarchy Standard (FHS)
↓
Kernel
↓
Hardware
```

### Components

- **User** — interacts with the system
- **Applications** — software programs
- **Shell** — command interpreter
- **Kernel** — core of the operating system
- **Hardware** — physical components

---

# 📘 Module 3 — Linux Commands & System Administration

## What This Module Covers

Using Bash to navigate Linux, manage files, filter information, administer users, and apply the Principle of Least Privilege.

---

## 📂 Linux Filesystem

### Filesystem Hierarchy Standard (FHS)

Common directories:

| Directory | Purpose |
|-----------|---------|
| `/` | Root directory |
| `/home` | User home directories |
| `/bin` | Executable programs |
| `/etc` | System configuration files |
| `/tmp` | Temporary files |
| `/mnt` | Mounted storage devices |

### File Paths

- Absolute path → starts from `/`
- Relative path → starts from current directory
- `~` → user's home directory
- `.` → current directory
- `..` → parent directory

---

## 🧭 Navigation Commands

| Command | Purpose |
|----------|---------|
| `pwd` | Current directory |
| `whoami` | Current user |
| `ls` | List directory contents |
| `ls -a` | Include hidden files |
| `ls -l` | Detailed file information |
| `ls -la` | Detailed + hidden files |
| `cd` | Change directory |

---

## 📖 Reading Files

| Command | Purpose |
|----------|---------|
| `cat` | Display entire file |
| `head` | First lines |
| `tail` | Last lines |
| `less` | Scroll through file |

---

## 📁 Managing Files

| Command | Purpose |
|----------|---------|
| `mkdir` | Create directory |
| `rmdir` | Delete empty directory |
| `touch` | Create file |
| `rm` | Delete file |
| `mv` | Move / Rename |
| `cp` | Copy |
| `nano` | Terminal text editor |

### Output Redirection

- `>` overwrite file
- `>>` append to file

---

## 🔍 Filtering Information

### grep

Searches files for matching text.

### Pipe (`|`)

Passes output from one command into another.

### find

Locate files by:

- Name (`-name`, `-iname`)
- Modification time (`-mtime`, `-mmin`)
- Directory location

---

## 🔐 File Permissions

Permission format:

```
-rwxrwxrwx
```

Permissions:

- Read (r)
- Write (w)
- Execute (x)

Permission owners:

- User
- Group
- Others

### chmod

Modify permissions using:

- `+`
- `-`
- `=`

### Principle of Least Privilege

Users should receive only the minimum permissions required to perform their job.

---

## 👤 Authentication & Authorization

### Authentication

Verifies user identity.

### Authorization

Determines what resources a user may access.

---

## 🛡️ sudo

- Temporary administrative privileges
- Safer than logging in as root
- Use only when necessary

---

## 👥 User Management

### useradd

Create users.

Options:

- `-g` → primary group
- `-G` → supplementary groups

### usermod

Modify existing users.

Common options:

- `-g`
- `-a -G`
- `-d`
- `-l`
- `-L`

### userdel

Delete users.

- `-r` → remove home directory

### chown

Change ownership of files/directories.

---

## 🧪 Hands-on Labs Completed

- Linux filesystem navigation
- Reading and analyzing files
- Creating, moving, copying and deleting files/directories
- Filtering files with grep, pipes and find
- Managing file permissions with chmod
- Applying Principle of Least Privilege
- Managing Linux users and groups
- Changing ownership using chown
- Using sudo responsibly for administrative tasks

---

# 📘 Module 4 — SQL

*Coming soon...*

---

# 💭 Reflection

> Compared to the networking course, this course has been far more hands-on.
> Almost every concept is reinforced through terminal labs, making Linux feel
> much more natural with practice. Bash commands initially seem overwhelming,
> but after repeated labs they become muscle memory. Understanding permissions,
> ownership, and the Principle of Least Privilege especially helped connect Linux
> administration with real-world security operations.
