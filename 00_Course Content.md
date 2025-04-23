## 🐧 Shell Scripting Course Curriculum for DevOps & Cloud Engineers

---

### 🔰 **Level 1: Basic Shell Scripting (Beginner Level)**

#### **Module 1: Introduction to Shell and Shell Scripting**
- What is a shell?
- Types of shells (sh, bash, ksh, zsh)
- Shell vs Bash
- Setting up a Linux environment (Ubuntu 22.04 LTS on AWS, Azure, or local)
- First shell script (`.sh` file)

#### **Module 2: Shell Script Basics**
- Script structure: shebang (`#!/bin/bash`)
- Running shell scripts
- Script permissions (`chmod`, `chown`)
- `echo`, `printf` and `read` usage
- Comments in shell scripts

#### **Module 3: Variables and Operators**
- Defining and using variables
- Environment variables
- Arithmetic operators
- String operators
- Using `expr` and `$(( ))`

#### **Module 4: Conditional Statements**
- `if`, `if-else`, `if-elif-else`
- `test` command and `[ ]`
- Using comparison operators
- File test operators (`-f`, `-d`, `-e`, `-r`, `-w`, `-x`)

#### **Module 5: Looping Constructs**
- `for` loop
- `while` loop
- `until` loop
- `break` and `continue`

#### **Module 6: User Input & Basic Functions**
- Reading input from user
- Command line arguments (`$1`, `$2`, `$@`, `$#`)
- Creating and calling functions
- `return` and exit status

---

### 🛠️ **Level 2: Intermediate Shell Scripting**

#### **Module 7: Working with Files and Directories**
- Creating, renaming, deleting files/folders
- File input/output operations
- Redirection operators (`>`, `>>`, `<`, `2>`, `&>`)
- `cat`, `cut`, `awk`, `sed` basics

#### **Module 8: String and Text Processing**
- String manipulation techniques
- Using `awk`, `sed` and `cut` for log analysis
- Pattern matching and regular expressions
- Real-time examples (e.g., parsing logs, extracting email IDs)

#### **Module 9: Arrays and Advanced Functions**
- One-dimensional and associative arrays
- Iterating over arrays
- Functions with arguments and return values
- Scope of variables (`local`, `global`)

#### **Module 10: Scheduling & Automation**
- Introduction to `cron` and `crontab`
- Scheduling backup scripts
- Monitoring and notification scripts
- Logging in shell scripts

#### **Module 11: Exit Status and Error Handling**
- `$?` exit codes
- Trap command
- Try-catch equivalent using conditions
- Debugging scripts (`set -x`, `set -e`, `trap`)

---

### 🚀 **Level 3: Advanced Shell Scripting for DevOps**

#### **Module 12: Working with External Commands and Tools**
- Piping and redirection
- Calling external programs in scripts
- Handling command output (`command substitution`)
- Background jobs and process management

#### **Module 13: Log Monitoring and Alerting Scripts**
- Real-time log parsing
- Monitoring CPU/Memory/Disk
- Sending alerts using `mail`, `sendmail`, or integration with Slack/Teams

#### **Module 14: Shell Scripting for DevOps Tools**
- Automating Docker container tasks
- Triggering Jenkins jobs from scripts
- Managing Git repositories via shell
- Interfacing with AWS CLI and Azure CLI

#### **Module 15: Writing Menu-Driven Shell Scripts**
- Building interactive menus
- Options handling using `select`, `case`, `getopts`
- Case study: menu-driven server administration

#### **Module 16: Project & Capstone**
- **Mini Projects:**
  - Automated user creation & permission assignment
  - System health check dashboard
  - Backup and restore automation
- **Capstone Project:** Real-world DevOps use-case combining monitoring, automation, alerts, and logs management with shell scripting.

---

### 📝 Bonus Content (Optional)
- Shell scripting best practices
- Script optimization and maintainability
- Version control for scripts (Git)
- Interview questions & mock tests
