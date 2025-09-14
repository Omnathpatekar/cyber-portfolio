# Day 05 — Bandit Level 4 → 5
**Date:** 2025-09-05

## 🔑 Level Goal
Log into `bandit4` and find the password for `bandit5`. The password is stored in a human-readable file inside the `inhere` directory.

## 🛠 Commands used
```bash
# SSH into bandit4 (use password from previous level)
ssh bandit4@bandit.labs.overthewire.org -p 2220

# Navigate to the inhere directory and list files (including hidden)
ls
cd inhere
ls -la

# Identify file types to find the human-readable file
file ./*

# Read the human-readable file (example: -file07)
cat ./-file07

📌 Password / Flag

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

🧠 Notes / Lessons

Use file to quickly identify which files are human-readable vs binary.

ls -la shows all files; file ./* helps find the readable one.

When filenames start with -, prefix with ./ (e.g., cat ./-file07).
