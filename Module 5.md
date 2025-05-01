Module 5: Looping Constructs

Here’s the content for **Module 5: Looping Constructs**—structured and ready for your shell scripting documentation or training material:

---

# 🔰 Module 5: Looping Constructs

## ✅ `for` Loop

The `for` loop allows you to repeat a set of commands a specific number of times or over a range of items.

### ➤ Syntax:
```bash
for variable in list
do
  # commands
done
```

### ➤ Example: Looping over a range:
```bash
for i in {1..5}
do
  echo "Number: $i"
done
```

### ➤ Example: Looping over a list:
```bash
for fruit in apple banana orange
do
  echo "Fruit: $fruit"
done
```

> 🔎 You can also loop over a range with `seq`:
```bash
for i in $(seq 1 5)
do
  echo "Number: $i"
done
```

---

## ✅ `while` Loop

The `while` loop repeats commands as long as a specified condition is true.

### ➤ Syntax:
```bash
while [ condition ]
do
  # commands
done
```

### ➤ Example:
```bash
count=1
while [ $count -le 5 ]
do
  echo "Count: $count"
  ((count++))
done
```

> 🧠 The condition is checked **before** executing the commands.

---

## ✅ `until` Loop

The `until` loop is similar to the `while` loop, but it executes commands as long as the condition is **false**.

### ➤ Syntax:
```bash
until [ condition ]
do
  # commands
done
```

### ➤ Example:
```bash
count=1
until [ $count -gt 5 ]
do
  echo "Count: $count"
  ((count++))
done
```

> 🧠 The condition is checked **before** executing the commands, and the loop runs as long as the condition is **false**.

---

## ✅ `break` and `continue`

- **`break`** – Exits from the loop immediately.
- **`continue`** – Skips the current iteration and moves to the next iteration of the loop.

### ➤ Example with `break`:
```bash
for i in {1..10}
do
  if [ $i -eq 5 ]; then
    break
  fi
  echo "Number: $i"
done
```
In this example, the loop will stop when `i` equals 5.

### ➤ Example with `continue`:
```bash
for i in {1..5}
do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo "Number: $i"
done
```
In this example, when `i` equals 3, the `continue` statement skips the `echo` command for that iteration.

---

### 📌 Example Script: `loop_example.sh`

```bash
#!/bin/bash

# Using a for loop to display numbers 1 to 5
echo "For loop example:"
for i in {1..5}
do
  echo "Number: $i"
done

# Using a while loop to display numbers 1 to 5
echo -e "\nWhile loop example:"
count=1
while [ $count -le 5 ]
do
  echo "Count: $count"
  ((count++))
done

# Using an until loop to display numbers 1 to 5
echo -e "\nUntil loop example:"
count=1
until [ $count -gt 5 ]
do
  echo "Count: $count"
  ((count++))
done

# Using break and continue in a loop
echo -e "\nBreak and Continue example:"
for i in {1..5}
do
  if [ $i -eq 3 ]; then
    echo "Skipping $i"
    continue
  fi
  echo "Number: $i"
  if [ $i -eq 4 ]; then
    echo "Breaking loop"
    break
  fi
done
```

To run:
```bash
chmod +x loop_example.sh
./loop_example.sh
```

---

Would you like me to add this to the same Google Docs document you’re working on? Let me know if you need further customization!