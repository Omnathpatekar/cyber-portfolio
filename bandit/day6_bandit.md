# Day 06 — Bandit Level 5 → 6
**Date:** 2025-09-06

## 🔑 Level Goal
Log into `bandit5` and find the password for `bandit6`. The password is hidden in a file under the `inhere` directory that matches all of:
- human-readable
- exactly **1033 bytes**
- not executable

## 🛠 Commands used
```bash
# SSH into bandit5
ssh bandit5@bandit.labs.overthewire.org -p 2220

# Navigate to inhere
ls
cd inhere

# Find the file matching the requirements:
find . -type f -size 1033c -readable ! -executable 2>/dev/null

# Read the file (example path)
cat ./maybehere07/.file2

🔍 Command explanation

-type f → only regular files

-size 1033c → file size exactly 1033 bytes (c = bytes)

-readable → file is readable by current user

! -executable → exclude executable files

2>/dev/null → hide permission errors from output

📌 Password / Flag

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

🧠 Notes / Lessons

find is extremely powerful for targeted searches (owner, size, permissions).

Always verify file type (file <path>) if the result is ambiguous.
