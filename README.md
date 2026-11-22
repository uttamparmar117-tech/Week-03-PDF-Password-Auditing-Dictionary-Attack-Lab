🔐 Week 03 – PDF Password Auditing & Dictionary Attack Lab

- Author: Uttam Parmar
- Program & Batch: Cybersecurity & Ethical Hacking Internship – Batch B084
- Assessment Date: 22 November 2026
- Repository: "networkwalks-week3-pdf-password-auditing"

---

📌 Project Overview

This repository contains practical exercises performed during Week 03 of the Networkwalks Cybersecurity Internship. It covers PDF password auditing, cryptographic hash extraction, dictionary-based password recovery, and Capture-The-Flag (CTF) verification.

The practical sessions focused on examining password-protected PDF files using John the Ripper and the Networkwalks Academy Dictionary Attack Lab ("$pdf$" hash matching).

The following three targets were successfully audited:

- Target 1 ("My Locked PDF1.pdf"): Extracted the "$pdf$" encryption hash and used a dictionary-based attack to recover the passphrase ("good-luck"), successfully obtaining Flag 1.
- Target 2 ("My Locked PDF2.pdf"): Analyzed the PDF Revision 4 (128-bit) encryption hash against a wordlist and recovered the password ("password1"), obtaining Flag 2.
- Target 3 ("My Locked PDF3.pdf"): Performed offline dictionary auditing through John the Ripper in "format=PDF" mode and recovered the keyboard-pattern password ("1qaz2wsx"), obtaining Flag 3.

---

⚠️ Legal & Ethical Disclaimer

All password auditing and hash recovery activities documented here were performed strictly within an authorized educational environment.

- "My Locked PDF1.pdf", "My Locked PDF2.pdf", and "My Locked PDF3.pdf" were official sandbox CTF training files supplied by Networkwalks Academy for Week 03 practical exercises.
- These exercises were conducted only for learning and understanding PDF security mechanisms.

Important: Never perform password recovery, hash extraction, or dictionary attacks on files or systems without obtaining explicit written permission from the owner.

---

🧰 Tools & Environment

Tool / Utility| Environment| Purpose
Johnny (John the Ripper GUI)| Windows Host| Loading offline "$pdf$" hashes, executing dictionary attacks, and validating recovered passwords
Networkwalks Hash Calculator & Dictionary Lab| Web Lab Environment| Extracting "$pdf$" hashes and evaluating dictionary attack performance
PDF Viewer (Browser / Adobe)| Windows Host| Opening audited PDF documents using recovered passphrases to verify CTF flags

---

🔎 Summary of Key Findings & Audited Targets

Target File| Encryption Format| Recovered Passphrase| Attack Method| Result
My Locked PDF1.pdf| "$pdf$" hash| "good-luck"| Dictionary Attack (Johnny & Web Cracker – 3,456/3,556 words)| Flag 1 Captured
My Locked PDF2.pdf| "$pdf$" hash| "password1"| Dictionary Attack (Johnny & Built-in 100-word list – 91/100 words)| Flag 2 Captured
My Locked PDF3.pdf| "$pdf$" hash| "1qaz2wsx"| Dictionary Attack (Johnny – format=PDF)| Flag 3 Captured

---

🔗 Key Technical Takeaways

1. Offline Attack Speed & Weak Passwords

Common dictionary terms such as "good-luck", predictable passwords like "password1", and keyboard sequences such as "1qaz2wsx" can be recovered very quickly once the PDF encryption hash is available.

2. Hash Extraction Process

Tools such as "pdf2john" and John the Ripper help extract PDF encryption information from the PDF trailer, including dictionary objects such as "/O", "/U", "/P", "/R", and "/V".

This information is converted into a standardized "$pdf$" hash format, allowing password candidates to be tested offline without modifying the original PDF file.

---

🛡️ Defensive Recommendations

1. Use Strong Passphrases: Avoid common dictionary words, predictable combinations like "password1", and keyboard patterns such as "1qaz2wsx". Prefer randomly generated passphrases with at least 14 characters.

2. Improve PDF Encryption: Use modern AES-256 encryption supported by PDF 2.0 instead of relying on older 128-bit RC4/AES configurations.

3. Apply Access Controls: Keep confidential PDF documents in restricted-access storage and enable MFA and audit logging instead of depending only on file-level passwords.

---

## 📂 Repository Structure

```text
Week-03-PDF-Password-Auditing-Dictionary-Attack-Lab/
│
├── README.md
│
├── hashcracker.jpeg
│
├── johnny.jpeg
│
├── pdf1-johnny-cracked.jpeg
│
├── pdf1-johnny-passwordcracked.jpeg
│
├── pdf2-web-cracker.jpeg
│
├── pdf3-web-cracker.jpeg
│
├── web-hash-calculator.jpeg
│
└── web-cracker-pdf3.jpeg
```

👤 Author

Uttam Parmar

Cybersecurity & Ethical Hacking Intern – Batch B084

Program: Networkwalks Cybersecurity Internship (Week 03)
