Module 4: Conditional Statements

Here’s the complete content for **Module 4: Conditional Statements** — structured for clarity and ideal for training or documentation:

---

# 🔰 Module 4: Conditional Statements

## ✅ `if`, `if-else`, `if-elif-else` Statements

Conditional statements allow scripts to make decisions based on conditions.

### ➤ Basic `if` Statement:
```bash
if [ condition ]; then
  # commands
fi
```

### ➤ `if-else` Statement:
```bash
if [ condition ]; then
  # commands if true
else
  # commands if false
fi
```

### ➤ `if-elif-else` Statement:
```bash
if [ condition1 ]; then
  # commands if condition1 is true
elif [ condition2 ]; then
  # commands if condition2 is true
else
  # commands if none are true
fi
```

> ✅ Always ensure there are **spaces** around brackets and between keywords.

---

## ✅ `test` Command and `[ ]` Syntax

The `test` command or `[ ]` is used to evaluate expressions (they are interchangeable).

Example:
```bash
if test $a -gt 10; then
  echo "a is greater than 10"
fi

# Equivalent using [ ]
if [ $a -gt 10 ]; then
  echo "a is greater than 10"
fi
```

> 🚨 Don’t forget the space after `[` and before `]`.

---

## ✅ Using Comparison Operators

### ➤ Numeric Comparison:
| Operator | Meaning                |
|----------|------------------------|
| `-eq`    | Equal to               |
| `-ne`    | Not equal to           |
| `-gt`    | Greater than           |
| `-lt`    | Less than              |
| `-ge`    | Greater than or equal  |
| `-le`    | Less than or equal     |

Example:
```bash
if [ $num -eq 5 ]; then
  echo "Number is 5"
fi
```

### ➤ String Comparison:
| Operator | Meaning              |
|----------|----------------------|
| `=`      | Equal                |
| `!=`     | Not equal            |
| `-z`     | True if string is empty |
| `-n`     | True if string is not empty |

---

## ✅ File Test Operators

These operators check file attributes and existence:

| Operator | Description                          |
|----------|--------------------------------------|
| `-f`     | True if file exists and is a regular file |
| `-d`     | True if it's a directory             |
| `-e`     | True if the file or directory exists |
| `-r`     | True if file is readable             |
| `-w`     | True if file is writable             |
| `-x`     | True if file is executable           |

### ➤ Example:
```bash
file="script.sh"

if [ -f "$file" ]; then
  echo "$file exists and is a regular file"
fi

if [ -x "$file" ]; then
  echo "$file is executable"
fi
```

---

### 📌 Example Script: `check_file.sh`

```bash
#!/bin/bash

echo "Enter file name:"
read file

if [ -e "$file" ]; then
  echo "File exists."

  if [ -f "$file" ]; then
    echo "It's a regular file."
  fi

  if [ -r "$file" ]; then
    echo "File is readable."
  fi

  if [ -w "$file" ]; then
    echo "File is writable."
  fi

  if [ -x "$file" ]; then
    echo "File is executable."
  fi
else
  echo "File does not exist."
fi
```

To run:
```bash
chmod +x check_file.sh
./check_file.sh
```

---

Would you like me to insert this content directly into your shared Google Docs document alongside the previous modules?