# Task 6: Password Strength Analysis

This report documents the process and findings for Task 6 of the cybersecurity internship. The objective is to understand what makes a password strong by testing several passwords of varying complexity and researching related security concepts.

## 1. Objective

The goal of this task is to:
* Understand the criteria for a strong password.
* Test multiple passwords against an online password strength checker (`passwordmeter.com`).
* Analyze the scores and feedback from the tool.
* Research common password attacks and best practices.
* Summarize the findings and key learnings.

## 2. Password Test Results

Five passwords were created and tested. The results show a clear progression from "Very Weak" to "Very Strong" based on added complexity and length.

| Password Tested | Score | Complexity Rating |
| :--- | :--- | :--- |
| `123456` | 4% | Very Weak |
| `Harry123` | 63% | Strong |
| `Harry@123` | 81% | Very Strong |
| `Harry@#123@` | 100% | Very Strong |
| `Harry@07/07/2000` | 100% | Very Strong |

### Test Result Screenshots

Below are the detailed screenshots from `passwordmeter.com` for each test.

**(Note: You must upload your screenshots to GitHub and then replace the "PASTE-LINK-HERE" text with the actual link to your image.)**

---
**Test 1: `123456` (Score: 4%)**
* ![Test 1 - Top](https://github.com/HanumandlaHarikrishna07/elevatelabs-cyber-task-6/blob/main/screenshots/common.png)
* ![Test 1 - Bottom](https://github.com/HanumandlaHarikrishna07/elevatelabs-cyber-task-6/blob/main/screenshots/common%20test%20results.png)

---
**Test 2: `Harry123` (Score: 63%)**
* ![Test 2 - Top](PASTE-SCREENSHOT-165924.png-LINK-HERE)
* ![Test 2 - Bottom](PASTE-SCREENSHOT-165934.png-LINK-HERE)

---
**Test 3: `Harry@123` (Score: 81%)**
* ![Test 3 - Top](PASTE-SCREENSHOT-170005.png-LINK-HERE)
* ![Test 3 - Bottom](PASTE-SCREENSHOT-170015.png-LINK-HERE)

---
**Test 4: `Harry@#123@` (Score: 100%)**
* ![Test 4 - Top](PASTE-SCREENSHOT-170115.png-LINK-HERE)
* ![Test 4 - Bottom](PASTE-SCREENSHOT-170122.png-LINK-HERE)

---
**Test 5: `Harry@07/07/2000` (Score: 100%)**
* ![Test 5 - Top](PASTE-SCREENSHOT-170158.png-LINK-HERE)
* ![Test 5 - Bottom](PASTE-SCREENSHOT-170209.png-LINK-HERE)

---

## 3. Analysis of Results

The test results clearly demonstrate how password complexity and length directly impact security:

* **`123456` (4%):** This password failed badly. It only contains numbers and is sequential. The tool applied heavy deductions for "Numbers Only" and "Sequential Numbers (3+)." It lacks any uppercase letters, lowercase letters, or symbols.
* **`Harry123` (63%):** This was a major improvement. Adding uppercase letters (`+14` bonus), lowercase letters (`+8` bonus), and increasing the character count (`+32` bonus) gave it a "Strong" rating. However, it still lost points for consecutive lowercase letters (`arry`) and consecutive numbers (`123`).
* **`Harry@123` (81%):** The *only* change was adding one symbol (`@`). This single addition gave a `+6` bonus for "Symbols" and a `+10` bonus for "Requirements," pushing the password into the "Very Strong" category.
* **`Harry@#123@` (100%):** This password improved on the previous one by adding more symbols and increasing the length to 11 characters. This increased the "Number of Characters" bonus to `+44` and the "Symbols" bonus to `+18`.
* **`Harry@07/07/2000` (100%):** This password also scored 100%, primarily due to its **excellent length** (16 characters), which gave it a `+64` bonus. It also has a good mix of all character types. **However, it has a human-readable flaw:** it's a date. While the tool only penalized it for "Repeat Characters" (the 0s and 7s), a real-world attacker would use common date patterns in a targeted attack.

## 4. Common Password Attacks

Two common attacks were researched as part of this task:

* **Brute Force Attack:** This is a password-guessing attack that systematically tries every possible combination of letters, numbers, and symbols until the correct one is found. Longer and more complex passwords make this attack exponentially harder and slower.
* **Dictionary Attack:** This is a more targeted attack that uses a "dictionary"—a pre-made list of millions of common words, phrases, and previously leaked passwords (like `password123` or `admin`). It's much faster than a brute force attack because it tries high-probability guesses first.

## 5. Best Practices & Key Learnings

Based on the task and test results, the following best practices are essential:

1.  **Length is King:** Increasing password length is the most effective way to increase its strength against brute force attacks. Aim for 12-16 characters or more.
2.  **Use Complexity:** A strong password must use a mix of all four character types: uppercase letters, lowercase letters, numbers, and symbols.
3.  **Avoid Predictability:** Do not use common words (dictionary attack), sequential numbers (`123`), or personal information (like names or birthdays, e.g., `Harry` or `07/07/2000`).
4.  **Use a Passphrase:** A long phrase made of multiple random words (e.g., `Correct-Horse-Battery-Staple`) can be both very strong and easier to remember.
5.  **Use a Password Manager:** These tools generate and store extremely strong, unique passwords for all your accounts. You only need to remember one master password.
6.  **Enable Multi-Factor Authentication (MFA):** This is the most critical security layer. Even if an attacker steals your password, they cannot log in without the second factor (e.g., a code from your phone).
