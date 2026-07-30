# 🐧 Linux Notes

> Detailed notes for **Modules 1–3** of **Course 4 – Tools of the Trade: Linux and SQL** from the Google Cybersecurity Professional Certificate.

---

# 📑 Contents

- Module 1 — Operating Systems Fundamentals
- Module 2 — Linux Fundamentals
- Module 3 — Linux Commands in the Bash Shell

---

<details>
<summary><h1>📘 Module 1 — Operating Systems Fundamentals</h1></summary>

## 🎯 What This Module Covers

An introduction to operating systems, how they interact with hardware and software, and how they manage system resources, processes, and memory.

---

## 💻 Operating System (OS)

An **Operating System (OS)** is system software that acts as an interface between the user, applications, and computer hardware.

### Responsibilities

- Manages hardware resources
- Runs applications
- Allocates memory
- Schedules processes
- Provides a user interface
- Handles input/output operations

---

## ⚙️ Process Management

A **process** is a program that is currently running.

The operating system is responsible for:

- Creating processes
- Scheduling CPU time
- Managing multiple running processes
- Ending completed processes

### Key Points

- Enables multitasking
- Prevents process conflicts
- Improves CPU efficiency

---

## 🧠 Memory Management

Memory management controls how RAM is allocated and released.

### Responsibilities

- Allocates memory to applications
- Frees unused memory
- Prevents memory conflicts
- Protects one process from another
- Improves stability and performance

---

## 🎯 Key Takeaways

- The operating system connects hardware and software.
- Processes are managed and scheduled by the OS.
- Memory is allocated dynamically to running applications.
- Proper process and memory management improve overall system performance.

</details>

---

<details>
<summary><h1>📘 Module 2 — Linux Fundamentals</h1></summary>

## 🎯 What This Module Covers

Introduction to Linux, its architecture, distributions, and why it is widely used in cybersecurity.

---

# 🐧 Linux

Linux is an **open-source operating system** based on the Unix operating system.

### Why Linux is Popular

- Free and open source
- Stable and reliable
- Highly customizable
- Secure by design
- Powerful command-line interface
- Widely used in servers and cloud environments

### Linux in Cybersecurity

Linux is commonly used for:

- Security Operations Centers (SOC)
- System Administration
- Cloud Infrastructure
- Ethical Hacking
- Penetration Testing
- Digital Forensics

---

# 📦 Linux Distributions

A **distribution (distro)** is a version of Linux packaged with its own software and tools.

### Common Linux Distributions

- Ubuntu
- Debian
- Kali Linux
- Fedora
- Red Hat Enterprise Linux (RHEL)

---

# 🏗 Linux Architecture

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

---

## Components

| Component | Purpose |
|-----------|---------|
| User | Interacts with the operating system |
| Applications | Software programs executed by the user |
| Shell | Command interpreter between the user and the kernel |
| Filesystem Hierarchy Standard (FHS) | Organizes files and directories |
| Kernel | Core of Linux that manages hardware and system resources |
| Hardware | Physical components of the computer |

---

## 🖥 Kernel

The **kernel** is the core component of Linux.

### Responsibilities

- Process management
- Memory management
- Device management
- File system management
- Hardware communication

---

## 💻 Shell

The **shell** is a command-line interpreter that accepts commands from the user and communicates with the kernel.

Examples:

- Bash
- Zsh
- Fish

Throughout this course, the **Bash Shell** is used.

---

## 📂 Filesystem Hierarchy Standard (FHS)

The **Filesystem Hierarchy Standard (FHS)** defines how Linux organizes files and directories.

It provides a standardized directory structure across Linux distributions.

---

## 🎯 Why Linux Matters for Security Analysts

Security analysts frequently use Linux to:

- Investigate systems
- Analyze logs
- Manage servers
- Configure permissions
- Automate repetitive tasks
- Perform incident response
- Execute security tools

---

## 🎯 Key Takeaways

- Linux is the dominant operating system for cybersecurity.
- Different Linux distributions serve different purposes.
- The kernel manages hardware and system resources.
- The shell allows users to interact with Linux.
- The Filesystem Hierarchy Standard (FHS) organizes Linux storage consistently.

</details>

---

<details open>
<summary><h1>📘 Module 3 — Linux Commands in the Bash Shell</h1></summary>

## 📂 Linux Filesystem

The **Filesystem Hierarchy Standard (FHS)** defines how Linux organizes files and directories.

### Standard Directories

| Directory | Purpose |
|-----------|---------|
| `/` | Root directory |
| `/home` | User home directories |
| `/bin` | Executable programs |
| `/etc` | System configuration files |
| `/tmp` | Temporary files (commonly targeted by attackers) |
| `/mnt` | Mounted storage devices |

---

## 📍 File Paths

### Absolute Path

Starts from the root directory.

Example:

```text
/home/analyst/projects
```

### Relative Path

Starts from the current working directory.

Example:

```text
projects/
```

### Shortcuts

| Symbol | Meaning |
|---------|---------|
| `~` | Home directory |
| `.` | Current directory |
| `..` | Parent directory |

---

<details>
<summary><h2>🧭 Navigation Commands</h2></summary>

| Command | Purpose |
|----------|---------|
| `pwd` | Print current working directory |
| `whoami` | Display current username |
| `ls` | List directory contents |
| `ls -a` | Show hidden files |
| `ls -l` | Long listing with permissions |
| `ls -la` | Long listing including hidden files |
| `cd` | Change directory |

### Example

```bash
pwd
ls -la
cd Documents
whoami
```

</details>

---

<details>
<summary><h2>📖 Reading File Contents</h2></summary>

| Command | Purpose |
|----------|---------|
| `cat` | Display entire file |
| `head` | Display first 10 lines |
| `tail` | Display last 10 lines |
| `less` | View file page-by-page |

### Examples

```bash
cat notes.txt

head logs.txt

tail auth.log

less report.txt
```

> `tail` is commonly used to monitor recent log entries.

</details>

---

<details>
<summary><h2>📁 Managing Files & Directories</h2></summary>

| Command | Purpose |
|----------|---------|
| `mkdir` | Create directory |
| `rmdir` | Delete empty directory |
| `touch` | Create empty file |
| `rm` | Delete file |
| `mv` | Move or rename file |
| `cp` | Copy file or directory |
| `nano` | Terminal text editor |

### Examples

```bash
mkdir reports

touch notes.txt

cp notes.txt backup.txt

mv backup.txt archive/

rm notes.txt

nano report.txt
```

### Output Redirection

| Operator | Purpose |
|-----------|---------|
| `>` | Overwrite file |
| `>>` | Append to file |

Examples

```bash
echo "Hello" > notes.txt

echo "New line" >> notes.txt
```

</details>

---

<details>
<summary><h2>🔍 Filtering Information</h2></summary>

Filtering allows security analysts to quickly locate files or specific information.

### grep

Searches files for matching text.

```bash
grep "error" logs.txt
```

---

### Pipe (`|`)

Passes the output of one command as the input to another.

```bash
ls | grep report
```

---

### find

Searches for files and directories.

Useful options:

- `-name`
- `-iname`
- `-mtime`
- `-mmin`

Examples

```bash
find /home -name "*.log"

find /home -mtime -3

find /projects -iname "*report*"
```

</details>

---

<details>
<summary><h2>🔐 File Permissions</h2></summary>

Permission format:

```text
-rwxrwxrwx
```

### Permission Types

- Read (`r`)
- Write (`w`)
- Execute (`x`)

### Permission Owners

- User
- Group
- Others

---

### Viewing Permissions

```bash
ls -l
```

```bash
ls -la
```

---

### chmod

Changes file or directory permissions.

Operators:

- `+` Add permission
- `-` Remove permission
- `=` Assign exact permissions

Example

```bash
chmod u+rwx,g-r,o-r file.txt
```

---

## Principle of Least Privilege (PoLP)

Users should only receive the minimum permissions required to perform their tasks.

Benefits:

- Reduces attack surface
- Prevents unauthorized access
- Improves security
- Limits accidental changes

</details>

---

<details>
<summary><h2>👤 Authentication & Authorization</h2></summary>

### Authentication

Verifies the identity of a user.

### Authorization

Determines what resources a user is allowed to access.

---

## sudo

Temporarily grants elevated (administrative) privileges.

### Best Practices

- Prefer `sudo` over logging in as root.
- Only use when necessary.
- Avoid blindly executing internet commands with `sudo`.

</details>

---

<details>
<summary><h2>👥 User & Ownership Management</h2></summary>

## useradd

Create a new user.

Useful options:

- `-g` → Primary group
- `-G` → Supplementary groups

Example

```bash
sudo useradd -g security uzair
```

---

## usermod

Modify an existing user.

Useful options:

- `-g`
- `-a -G`
- `-d`
- `-l`
- `-L`

Example

```bash
sudo usermod -a -G admin uzair
```

---

## userdel

Delete a user.

Option:

- `-r` → Remove home directory

```bash
sudo userdel -r uzair
```

---

## chown

Change ownership of files and directories.

Examples

```bash
sudo chown uzair report.txt

sudo chown :security report.txt
```

</details>

---

<h2>🧪 Hands-on Labs Completed</h2>

Throughout this module, I completed guided labs after learning each major concept.

### Linux Labs

- Linux filesystem navigation
- Reading and analyzing files
- Creating and managing directories
- Creating, copying, moving and deleting files
- Using Nano text editor
- Output redirection
- Filtering with grep, pipes and find
- Managing file permissions using chmod
- Applying the Principle of Least Privilege
- Managing Linux users and groups
- Using sudo responsibly
- Changing file ownership with chown

---

<h2>🎯 Module 3 Summary</h2>

By completing this module, I learned how to:

- Navigate the Linux filesystem confidently
- Read and manage files from the terminal
- Search and filter information efficiently
- Create, modify and organize files/directories
- Understand and manage Linux permissions
- Apply the Principle of Least Privilege (PoLP)
- Manage users, groups and ownership
- Use `sudo` securely for administrative tasks
- Reinforce every concept through practical Bash labs

---
