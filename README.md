import re

import re

# Define a basic email validation pattern
EMAIL_REGEX = r"^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$"

def is_valid_email(email):
    """Checks if the given string matches the email regex pattern."""
    return re.fullmatch(EMAIL_REGEX, email) is not None

# List of emails to test
test_emails = [
    "user@domain.com",
    "invalid-email@",
    "john.doe123@sub.domain.net",
    "missing@dotcom"
]

print("--- Email Validation Results ---")
for email in test_emails:
    validation_status = "✅ VALID" if is_valid_email(email) else "❌ INVALID"
    print(f"Checking: {email:<25} -> {validation_status}")
