# Day 10 — Bandit Level 9 → 10
**Date:** 2025-09-10

## 🔑 Level Goal
Log into `bandit9` and find the password for `bandit10`. The password is hidden in `data.txt` among a few human-readable strings and is **preceded by several `=` characters**.

## 🛠 Commands used
```bash
# SSH into bandit9
ssh bandit9@bandit.labs.overthewire.org -p 2220

# Extract readable strings and filter lines that contain "==="
strings data.txt | grep "==="

📌 Why it works 

strings extracts human-readable text from a binary/messy file.

grep "===" filters only the lines that contain multiple = characters — the password appears just after those = signs.

📌 Password / Flag

FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

🧠 Notes / Lessons

Use strings when a file contains mixed binary and text; it pulls out readable fragments.

When looking for patterns, pipe into grep to isolate likely candidate lines.
