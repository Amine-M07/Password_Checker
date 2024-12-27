import re
import getpass

def check_password_strength(password):
    # Criteria checks
    min_length = 8

    has_lowercase = bool(re.search(r"[a-z]", password))
    has_uppercase = bool(re.search(r"[A-Z]", password))
    has_number = bool(re.search(r"\d", password))
    has_special = bool(re.search(r"[^a-zA-Z\d\s]", password))

    common_passwords = ["password", "1234", "qwerty", "admin"]
    is_common = any(password.lower() == common for common in common_passwords)

    # Rating password strength
    if len(password) < min_length:
        return "Weak", "Password must be at least 8 characters long."
    
    if is_common:
        return "Weak", "Password is too common and easily guessable."
    
    if has_lowercase and has_uppercase and has_number and has_special:
        return "Very Strong", "Great password! It meets all criteria."
    
    if (has_lowercase or has_uppercase) and has_number:
        return "Moderate", "Consider adding special characters and more variety to your password."
    
    return "Weak", "Password should include a mix of uppercase, lowercase, numbers, and special characters."

if __name__ == "__main__":
    password = getpass.getpass("Enter your password to check its strength: ")
    strength, feedback = check_password_strength(password)
    print(f"Your password is {strength}: {feedback}")
