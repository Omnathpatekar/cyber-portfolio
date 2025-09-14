# Day 09 — Bandit Level 8 → 9
**Date:** 2025-09-09

## 🔑 Level Goal
Log into `bandit8` and find the password for `bandit9`. The password is the **only line** in `data.txt` that appears **once**.

## 🛠 Commands used
```bash
# SSH into bandit8
ssh bandit8@bandit.labs.overthewire.org -p 2220

# Find the unique line (password) in data.txt
sort data.txt | uniq -u

📌 Why it works (short)

sort data.txt — arranges all lines so duplicates are adjacent.

uniq -u — prints only lines that appear exactly once.

Together: returns the single unique password line.

📌 Password / Flag

4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

🧠 Notes / Lessons

For large files: sort | uniq -u is a fast way to find unique entries.
