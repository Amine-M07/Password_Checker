# Password Checker

**Password Checker** is a Python-based tool to evaluate the strength of a password. It checks whether a password meets specific security criteria, including the presence of lowercase letters, uppercase letters, numbers, and special characters. The tool also ensures the password is not a common or easily guessable one.

## Features
- **Checks Password Strength:** Evaluates if the password meets criteria such as minimum length, mix of characters (uppercase, lowercase, digits, and special characters).
- **Common Password Detection:** Flags passwords that are too common (e.g., `password`, `1234`, `qwerty`).
- **User Feedback:** Provides feedback on how to improve password strength.

## Project Overview

This project aims to help users create stronger passwords by analyzing the security of their chosen passwords. Password strength is rated based on the following criteria:
1. **Length:** The password must be at least 8 characters long.
2. **Character Diversity:** The password must contain:
   - At least one uppercase letter
   - At least one lowercase letter
   - At least one number
   - At least one special character (e.g., `@`, `#`, `!`, etc.)
3. **Common Passwords:** The password is checked against a list of common, easily guessable passwords.

## Installation

1. **Clone the Repository:**
   First, clone the repository to your local machine using the following command:
   ```bash
   git clone https://github.com/Amine-M07/Password_Checker.git
