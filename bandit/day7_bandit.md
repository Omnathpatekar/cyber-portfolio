# Day 07 — Bandit Level 6 → 7
**Date:** 2025-09-07

## 🔑 Level Goal
Log into `bandit6` and find the password for `bandit7`. The password is stored somewhere on the server and has all of the following properties:
- owned by user `bandit7`
- owned by group `bandit6`
- exactly **33 bytes** in size

## 🛠 Commands used
```bash
# SSH into bandit6 (use password from previous level)
ssh bandit6@bandit.labs.overthewire.org -p 2220

# Search the entire filesystem for a regular file owned by bandit7:bandit6 and 33 bytes in size
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null

# Read the found file (example path)
cat /var/lib/dpkg/info/bandit7.password


🔍 Command explanation

/ → start search from the root of the filesystem (whole server).

-type f → match regular files only.

-user bandit7 → file owner is bandit7.

-group bandit6 → file group is bandit6.

-size 33c → file size exactly 33 bytes (c = bytes).

2>/dev/null → redirect permission error messages away from output to keep results clean.

📌 Password / Flag

morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

🧠 Notes / Lessons

find is the go-to tool for targeted searches on permissions, owner, size, and name.

Always redirect permission errors when searching / to avoid clutter (using 2>/dev/null).
