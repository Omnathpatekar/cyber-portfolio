# Day 08 — Bandit Level 7 → 8
**Date:** 2025-09-08

## 🔑 Level Goal
Log into `bandit7` and find the password for `bandit8`. The password is located in `data.txt` next to the word **millionth**.

## 🛠 Commands used
```bash
# SSH into bandit7
ssh bandit7@bandit.labs.overthewire.org -p 2220

# Search for the keyword "millionth" in data.txt
grep millionth data.txt

📌 Password / Flag

dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

🧠 Notes / Lessons

grep finds lines matching a pattern; useful to search very large files quickly.

When extracting a password from a matched line, copy carefully to avoid leading/trailing whitespace.
