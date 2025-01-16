up:: [[Computer Science MOC]]
tags:: #Programming  
# Brute Force Attacks
- A method to gain access to information by repeatedly trying every possible combination of passwords
- [[Dictionaries]] based attack - Using a pre-defined list of words (dictionary) to attempt to find the password
- Highly inefficient, time-consuming, and resource-intensive, especially with strong passwords.
## Sample [[Python MOC]] Implementation
```
import itertools
import string

def brute_force_attack(target_password, max_length):
    characters = string.ascii_lowercase  # Lowercase letters
    for length in range(1, max_length + 1):
        for guess in itertools.product(characters, repeat=length):
            guess_password = ''.join(guess)
            print(f"Trying password: {guess_password}")
            if guess_password == target_password:
                return f"Password found: {guess_password}"
    return "Password not found"

# Example usage
target_password = "abc"
max_length = 3  # Maximum length of the password to try
result = brute_force_attack(target_password, max_length)
print(result)

```