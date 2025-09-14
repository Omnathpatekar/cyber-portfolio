# Day 02 — Bandit Level 1 → 2
**Date:** 2025-09-02

## 🔑 Level Goal
Log into bandit1 and find the password for bandit2. The password is stored in a file literally named `-` in the home directory.

## 🛠 Commands used
```bash
# SSH into bandit1 (use password found on previous level)
ssh bandit1@bandit.labs.overthewire.org -p 2220

# List files (including hidden/ odd names)
ls -la

# Read the file literally named '-' (three safe ways)
cat ./-
# or
cat "/home/bandit1/-"
# or (stop option parsing then read file)
cat -- -

📌 Password / Flag

263JGJPfgU6LtdEvgfWU1XP5yac29mFx

🧠 Notes / Lessons

Filenames that start with - are treated as options by many commands; prefix with ./ or use -- to stop option parsing.

Always run ls -la to reveal files that might be hidden or oddly-named.
