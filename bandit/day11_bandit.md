# Day 11 — Bandit Level 10 → 11
**Date:** 2025-09-11

## 🔑 Level Goal
Log into `bandit10` and find the password for `bandit11`. The file `data.txt` contains **Base64-encoded** data — decode it to get the password.

## 🛠 Commands used
```bash
# SSH into bandit10
ssh bandit10@bandit.labs.overthewire.org -p 2220

# View file (optional)
cat data.txt

# Decode Base64 to reveal the password
base64 -d data.txt

📌 Why it works 

Base64-encoded text uses characters A–Z, a–z, 0–9, +, / and = padding.

base64 -d decodes that back into readable text or binary. If output garbles your terminal, pipe to a file: base64 -d data.txt > output && file output.

📌 Password / Flag

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

🧠 Notes / Lessons

When you see the base64 character set, think base64 -d.

If decoding creates binary data, write to a file and run file to determine type, then extract appropriately.
