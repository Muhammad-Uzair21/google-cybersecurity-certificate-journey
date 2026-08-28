# 🐍 Automate Cybersecurity Tasks with Python

> Course 7 of the **Google Cybersecurity Professional Certificate**.

This course introduced Python for cybersecurity automation, with a focus on using Python to analyze data, work with files, apply regular expressions, and debug scripts.

> **Note:** This course is beginner-oriented. Since I already had prior programming experience, I skipped documenting foundational topics such as variables, data types, loops, and basic functions, and focused these notes on concepts that were new or particularly relevant to cybersecurity.

---

## 📚 Topics Covered

### 1. Python Modules & Libraries

- **Module:** A Python file containing reusable code such as functions, variables, and classes.
- **Library:** A collection of modules that provides reusable functionality.

#### Python Standard Library

Common modules relevant to cybersecurity:

- `re` → regular expressions and pattern matching
- `csv` → working with CSV files
- `os` / `glob` → interacting with files and directories
- `time` / `datetime` → timestamps and date/time operations
- `statistics` → statistical calculations

#### Importing

`import statistics`

`statistics.mean(data)`

`from statistics import mean, median`

`mean(data)`

External libraries must generally be installed before importing:

`%pip install numpy`

`import numpy`

---

### 2. Python Style & PEP 8

**PEP 8** is Python's style guide for writing readable and consistent code.

Key practices:

- Use consistent **indentation**.
- Follow standard naming and formatting conventions.
- Keep code readable and maintainable.

---

### 3. Regular Expressions

A **regular expression (regex)** is a sequence of characters that defines a pattern for searching text.

In cybersecurity, regex can be used to extract patterns such as:

- IP addresses
- usernames
- device IDs
- emails
- log information

Python's `re` module provides regex functionality.

`import re`

#### `re.findall()`

Returns all matches of a regex pattern as a list.

`re.findall(pattern, string)`

#### Common Regex Symbols

| Symbol | Meaning | Example |
|---|---|---|
| `\w` | Alphanumeric character or `_` | `ID_A17` → `I,D,_,A,1,7` |
| `\d` | Single digit `0–9` | `ID_A17` → `1,7` |
| `\s` | Whitespace | Space, tab, newline |
| `.` | Any character except newline | — |
| `\.` | Literal `.` | Matches an actual period |
| `+` | One or more occurrences | `\d+` → `32`, `17`, `825` |
| `*` | Zero or more occurrences | `\d*` |
| `{n}` | Exactly `n` occurrences | `\d{4}` → `1234` |
| `{m,n}` | Between `m` and `n` occurrences | `\d{1,3}` → `7`, `32`, `825` |

Python scans strings from **left to right** when matching patterns.

#### Building Patterns

Patterns can be combined to extract specific information.

For example:

`\w+:\s\d+`

Can identify a username followed by a colon, whitespace, and one or more login-attempt digits:

- `bmoreno: 12`
- `tshah: 7`
- `sgilmore: 5`

#### Regex Activity

Practiced using regex to:

- Extract device IDs containing specific characters associated with an operating system requiring an update.
- Extract IP addresses from logs and compare them against a list of flagged addresses.

---

## 4. Working with Files

Security analysts frequently work with **log files**, which record events occurring within systems and networks.

### Opening Files

`with open("update_log.txt", "r") as file:`

`    updates = file.read()`

- `with` → manages the file resource and closes it automatically.
- `open()` → opens a file.
- `as` → assigns the opened file to a variable.

### File Modes

| Mode | Purpose |
|---|---|
| `r` | Read |
| `w` | Write/overwrite or create |
| `a` | Append to existing content |

### Reading

`.read()` converts file contents into a string.

`with open("update_log.txt", "r") as file:`

`    updates = file.read()`

### Writing

`.write()` writes string data to a file.

`with open("access_log.txt", "a") as file:`

`    file.write(line)`

---

## 5. Parsing File Contents

**Parsing** means converting data into a structure that is easier to process or interpret.

### `.split()`

Converts a string into a list using a specified separator.

`approved_users.split(",")`

Without an argument, `.split()` separates on whitespace.

Useful when file contents need to be processed item-by-item.

### `.join()`

Converts an iterable such as a list into a string.

`",".join(approved_users)`

A newline can also be used as the separator:

`"\n".join(approved_users)`

### Common Workflow

**File → `.read()` → string → `.split()` → list**

**List → `.join()` → string → `.write()` → file**

### File Activities

Practiced:

- Importing and parsing security log files for analysis.
- Developing an algorithm to parse an authorized-IP list and remove addresses that no longer have access to restricted content.

---

## 6. Debugging Python Code

### Types of Errors

- **Syntax Error** → invalid Python syntax.
- **Logic Error** → code runs but produces an unintended result.
- **Exception** → syntactically valid code that cannot execute.

### Common Exceptions

| Error | Meaning |
|---|---|
| `NameError` | Undefined variable or function |
| `IndexError` | Index does not exist |
| `TypeError` | Incompatible data types |
| `FileNotFoundError` | File/path does not exist |
| `IndentationError` | Incorrect indentation |

### Debugging Techniques

**Error messages**

- Identify the error and affected line.
- Python generally reports errors one at a time, so fix the first before addressing subsequent ones.

**Debugger**

- Uses **breakpoints** to pause execution.
- Allows inspection of program flow and variable values.

**Print statements**

- Temporarily print values or checkpoints to identify where unexpected behavior occurs.
- Useful for locating logic errors.

**AI coding assistants**

- Can assist with analyzing and debugging code.
- AI-generated code or suggestions should always be reviewed and validated before execution.

---

## 🎯 Key Takeaways

- Python modules and libraries provide reusable functionality for cybersecurity automation.
- **Regex** can efficiently extract patterns from logs and other security data.
- Python's `re.findall()` returns all matches for a given pattern.
- Files can be read, modified, parsed, and written using Python.
- `.split()` converts strings into lists, while `.join()` converts lists back into strings.
- Understanding syntax errors, logic errors, and exceptions makes debugging more effective.
- These capabilities can be combined to automate repetitive security-analysis tasks.