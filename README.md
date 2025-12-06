import re

# Define a basic email validation pattern (e.g., something@domain.com)
# This pattern checks for:
# ^: Start of string
# [A-Za-z0-9._%+-]+: One or more alphanumeric chars, dots, underscores, percents, plus, or minus
# @: The required '@' symbol
# [A-Za-z0-9.-]+: One or more alphanumeric chars, dots, or minus signs for the domain
# \.: A literal dot
# [A-Za-z]{2,}: Two or more letters for the top-level domain (e.g., com, org, net)
# $: End of string
EMAIL_REGEX = r"^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$"

# Email to test
test_email = "test.user@example.com"

# Validate the email
if re.fullmatch(EMAIL_REGEX, test_email):
    print(f"Email '{test_email}' is VALID.")
else:
    print(f"Email '{test_email}' is INVALID.")
