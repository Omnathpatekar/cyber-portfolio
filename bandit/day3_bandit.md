# Day 03 — Bandit Level 2 → 3
**Date:** 2025-09-03

## 🔑 Level Goal
Log into `bandit2` and find the password for `bandit3`. The password is stored in a file named:  
`--spaces in this filename--` (note: filename contains spaces and starts with `--`).

## 🛠 Commands used
```bash
# SSH into bandit2 (use password from previous level)
ssh bandit2@bandit.labs.overthewire.org -p 2220

# List files (show hidden items and details)
ls -la

# Safely read a filename that contains spaces and starts with dashes:
cat "./--spaces in this filename--"

# Alternative forms:
cat ./--spaces\ in\ this\ filename--
# or use "--" to stop option parsing:
cat -- --spaces\ in\ this\ filename--



📌 Password / Flag
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

🧠 Notes / Lessons
Filenames with spaces must be quoted or escaped ("file name" or file\ name).

Filenames beginning with - are treated as options; either prepend ./ or use -- to stop option parsing.

Habit: always ls -la first, then file or cat carefully.

