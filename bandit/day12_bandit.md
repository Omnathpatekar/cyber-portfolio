# Day 12 — Bandit Level 11 → 12
**Date:** 2025-09-12

## 🔑 Level Goal
Log into `bandit11` and find the password for `bandit12`. The file `data.txt` has all letters rotated by 13 positions (ROT13). Decode it to reveal the password.

## 🛠 Commands used
```bash
# SSH into bandit11
ssh bandit11@bandit.labs.overthewire.org -p 2220

# View file (optional)
cat data.txt

# Decode ROT13 to reveal the password
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

📌 Why it works 

ROT13 shifts letters 13 positions: a ↔ n, A ↔ N.

tr (translate) maps characters; the 'A-Za-z' 'N-ZA-Mn-za-m' mapping performs ROT13.

📌 Password / Flag

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

🧠 Notes / Lessons

For simple substitution ciphers like ROT13, tr is the fastest tool.

If output garbles your terminal, redirect to a file:
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' > output.txt && cat output.txt
