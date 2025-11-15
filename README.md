# Cipher Implementation Project

## Overview
A comprehensive Python implementation of classical cryptographic ciphers for educational purposes. This project demonstrates the evolution from simple Caesar cipher to complex Vigenère cipher through 96 documented learning steps.

## Features
- 🔐 **Caesar Cipher** - Fixed shift encryption/decryption
- 🗝️ **Vigenère Cipher** - Polyalphabetic substitution with keywords  
- 📝 **Educational Focus** - Step-by-step learning progression
- 🛡️ **Robust Handling** - Spaces, punctuation, and edge cases

---

## Quick Start

### Basic Usage
```python
from cipher import caesar, encrypt, decrypt

# Caesar Cipher
encrypted = caesar("hello world", 3)
print(encrypted)  # "khoor zruog"

decrypted = caesar("khoor zruog", -3) 
print(decrypted)  # "hello world"

# Vigenère Cipher
encrypted = encrypt("secret message", "key")
decrypted = decrypt(encrypted, "key")
```

---

## Installation
```
# Just download cipher.py and import it!
# No dependencies required
```

---

## User Paths
```markdown
## Documentation Paths

### 🚀 **Quick Understanding** (5-minute read)
For a brief overview of how the ciphers work:
[Quick Reference Guide](./quick_reference/cipher_quick_review.md)

### 📚 **Deep Learning** (30+ minute study)  
For the complete implementation journey:
[96-Step Detailed Documentation](./detailed_documentation/caesar_vigenere_96_steps.md)
```

---

## Technical Details
```
## Technical Implementation

### Caesar Cipher
- Fixed shift algorithm
- Wrap-around using modulo operator
- Handles lowercase conversion

### Vigenère Cipher  
- Polyalphabetic substitution
- Keyword-based shifting
- Automatic key repetition for long messages

## Project Structure
project/
├── detailed_documentation/ # 96-step learning journey
├── quick_reference/ # TL;DR explanations
└── README.md # You are here!
```
