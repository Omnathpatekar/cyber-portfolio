# Day 04 — Bandit Level 3 → 4
**Date:** 2025-09-04

## 🔑 Level Goal
Log into `bandit3` and find the password for `bandit4`. The password is stored in a hidden file inside the `inhere` directory.

## 🛠 Commands used
```bash
# SSH into bandit3 (use password from previous level)
ssh bandit3@bandit.labs.overthewire.org -p 2220

# Navigate and list hidden files
ls
cd inhere
ls -la

# Read the hidden file (example name: .hidden)
cat .hidden

# Alternative full path
cat /home/bandit3/inhere/.hidden

📌 Password / Flag

2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

🧠 Notes / Lessons

Hidden files begin with a dot (.). Use ls -la to reveal them.

cat ./filename or cat /full/path/filename safely prints file contents.
