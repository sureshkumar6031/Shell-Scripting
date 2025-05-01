Module 3: Variables and Operators



Here's a well-structured content draft for **Module 3: Variables and Operators** — ideal for training documentation or as part of your ongoing shell scripting guide:

---

# 🔰 Module 3: Variables and Operators

## ✅ Defining and Using Variables

Variables store data in shell scripts. They are **case-sensitive** and do **not require declaration of type**.

### ➤ Defining a variable:
```bash
name="John"
age=25
```

> ❗ *No spaces around the `=` sign.*

### ➤ Using a variable:
```bash
echo "Name: $name"
echo "Age: $age"
```

## ✅ Environment Variables

Environment variables are global variables available to all processes and shells.

### ➤ Viewing environment variables:
```bash
printenv
# or
env
```

### ➤ Accessing an environment variable:
```bash
echo "Current user: $USER"
echo "Home directory: $HOME"
```

### ➤ Exporting a variable (to make it available to sub-shells):
```bash
export course="Shell Scripting"
```

> 🧠 Use `export` when you want child processes to inherit the variable.

## ✅ Arithmetic Operators

Use arithmetic operators with `expr` or `$(())` for calculations.

### ➤ Operators:

| Operator | Meaning         |
|----------|-----------------|
| `+`      | Addition         |
| `-`      | Subtraction      |
| `*`      | Multiplication   |
| `/`      | Division         |
| `%`      | Modulus (remainder) |

## ✅ String Operators

| Operator | Description                         |
|----------|-------------------------------------|
| `=`      | Equal to                            |
| `!=`     | Not equal to                        |
| `-z`     | True if string is empty             |
| `-n`     | True if string is not empty         |
| `<` `>`  | Lexicographical comparison (use `[[ ]]`) |

### ➤ Examples:
```bash
str1="hello"
str2="world"

if [ "$str1" = "$str2" ]; then
  echo "Strings are equal"
else
  echo "Strings are different"
fi
```

## ✅ Using `expr` and `$(( ))`

### ➤ `expr` – Evaluates expressions:
```bash
result=$(expr 5 + 3)
echo "Result: $result"
```

> 🚨 Note: Spaces between operators and operands are mandatory in `expr`.

### ➤ `$(( ))` – Recommended method for arithmetic:
```bash
num1=10
num2=5

sum=$((num1 + num2))
echo "Sum: $sum"

product=$((num1 * num2))
echo "Product: $product"
```

> ✅ `$(( ))` is more readable and flexible than `expr`.

---

### 📌 Example Script: `math_demo.sh`

```bash
#!/bin/bash

# Basic arithmetic demo

echo "Enter first number:"
read num1

echo "Enter second number:"
read num2

sum=$((num1 + num2))
echo "Sum: $sum"

difference=$((num1 - num2))
echo "Difference: $difference"

product=$((num1 * num2))
echo "Product: $product"

quotient=$((num1 / num2))
echo "Quotient: $quotient"
```

To run:
```bash
chmod +x math_demo.sh
./math_demo.sh
```

---

Would you like this added to the same Google Docs document along with Module 1 and Module 2?