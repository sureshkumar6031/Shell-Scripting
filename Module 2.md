 Module 2: Shell Script Basics
 
 Here’s a clear and organized content draft for **Module 2: Shell Script Basics** – perfect for training materials, documentation, or instructional handouts:

---

# 🔰 Module 2: Shell Script Basics

## ✅ Script Structure: Shebang (`#!/bin/bash`)

The **shebang** is the first line in most shell scripts. It tells the system which interpreter to use when executing the script.

```bash
#!/bin/bash
```

- `#!` is called the shebang.
- `/bin/bash` points to the Bash shell.
- Always include this at the top of your `.sh` script for clarity and portability.

## ✅ Running Shell Scripts

You can run a shell script in several ways:

1. **Direct execution (recommended)**:
   ```bash
   ./script.sh
   ```

2. **Using the bash command**:
   ```bash
   bash script.sh
   ```

3. **Using source or dot (for current shell execution)**:
   ```bash
   source script.sh
   # or
   . script.sh
   ```

> 🔐 If the script doesn’t run directly, check and update its permissions.

## ✅ Script Permissions: `chmod` and `chown`

### `chmod` – Change file permissions:
Make a script executable:

```bash
chmod +x script.sh
```

### `chown` – Change file ownership:
Change the owner of a script:

```bash
sudo chown username:groupname script.sh
```

> 🛡️ Proper permissions help ensure security and functionality.

## ✅ `echo`, `printf`, and `read` Usage

### `echo` – Simple output:
```bash
echo "Hello, World!"
```

### `printf` – Formatted output (similar to C-style `printf`):
```bash
printf "User: %s\nAge: %d\n" "$USER" 25
```

### `read` – Get input from the user:
```bash
echo "Enter your name:"
read name
echo "Hello, $name!"
```

> 🧠 Use `read` to make your scripts interactive.

## ✅ Comments in Shell Scripts

Comments make your scripts readable and maintainable.

- **Single-line comment**:
  ```bash
  # This is a comment
  ```

- **Inline comment**:
  ```bash
  echo "Hello"  # Prints greeting
  ```

> 💡 Comments are ignored during execution but valuable for documentation and teamwork.

---

### 📌 Example Script: `userinfo.sh`

```bash
#!/bin/bash

# This script displays user information

echo "Enter your name:"
read name

echo "Enter your age:"
read age

printf "Hello, %s! You are %d years old.\n" "$name" "$age"
```

To run:
```bash
chmod +x userinfo.sh
./userinfo.sh
```

---

Would you like this added to your existing Google Docs training document?