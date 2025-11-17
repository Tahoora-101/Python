CIPHER IMPLEMENTATION
=====================

Final production-ready implementations of Caesar and Vigenère ciphers.

Features:
- Caesar Cipher with fixed shift encryption
- Vigenère Cipher with polyalphabetic substitution  
- Handles spaces, punctuation, and mixed case
- Professional API with encryption/decryption functions
 
For educational documentation: see Detailed Documentation of Ciphers/ folder         
For quick explanations: see Overview of Ciphers/ folder

```
def caesar(message, offset):
    Encrypt or decrypt text using Caesar Cipher.
    
    The Caesar cipher shifts each letter by a fixed number of positions.
    This is a monoalphabetic substitution cipher used by Julius Caesar.
    
    Args:
        message (str): Text to encrypt or decrypt
        offset (int): Number of positions to shift each letter
                    Positive for encryption, negative for decryption
    
    Returns:
        str: Encrypted or decrypted text
    
    Example:
        >>> caesar("hello", 3)
        'khoor'
        >>> caesar("khoor", -3) 
        'hello'
    """
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    result = ''

    for char in message:
        if not char.isalpha():
            # Preserve spaces, punctuation, and other non-letters
            result += char
        else:
            # Convert to lowercase for processing
            lowercase_char = char.lower()
            index = alphabet.find(lowercase_char)
            
            # Apply shift with wrap-around using modulo
            new_index = (index + offset) % len(alphabet)
            encrypted_char = alphabet[new_index]
            
            # Preserve original case
            if char.isupper():
                result += encrypted_char.upper()
            else:
                result += encrypted_char
    
    return result


def vigenere(message, key, direction=1):
    """
    Encrypt or decrypt text using Vigenère Cipher.
    
    The Vigenère cipher uses a keyword to create variable shifts for each letter.
    This is a polyalphabetic substitution cipher that was considered unbreakable
    for centuries.
    
    Args:
        message (str): Text to encrypt or decrypt
        key (str): Keyword used for encryption/decryption
        direction (int): 1 for encryption, -1 for decryption
    
    Returns:
        str: Encrypted or decrypted text
    
    Example:
        >>> vigenere("hello", "key", 1)
        'rijvs'
        >>> vigenere("rijvs", "key", -1)
        'hello'
    """
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    result = ''
    key_index = 0

    for char in message:
        if not char.isalpha():
            # Preserve spaces, punctuation, and other non-letters
            result += char
        else:
            # Convert to lowercase for processing
            lowercase_char = char.lower()
            
            # Get the current key character (cycles through key)
            key_char = key[key_index % len(key)].lower()
            key_index += 1
            
            # Calculate shift amount from key character
            key_offset = alphabet.index(key_char)
            
            # Apply shift with direction (encrypt/decrypt)
            char_index = alphabet.find(lowercase_char)
            new_index = (char_index + key_offset * direction) % len(alphabet)
            processed_char = alphabet[new_index]
            
            # Preserve original case
            if char.isupper():
                result += processed_char.upper()
            else:
                result += processed_char
    
    return result


def encrypt(message, key):
    """
    Encrypt text using Vigenère Cipher.
    
    Convenience wrapper for vigenere() function with encryption direction.
    
    Args:
        message (str): Text to encrypt
        key (str): Encryption key
    
    Returns:
        str: Encrypted text
    
    Example:
        >>> encrypt("secret message", "password")
        'zmywhx wmzzfso'
    """
    return vigenere(message, key, direction=1)


def decrypt(message, key):
    """
    Decrypt text using Vigenère Cipher.
    
    Convenience wrapper for vigenere() function with decryption direction.
    
    Args:
        message (str): Text to decrypt
        key (str): Decryption key (must match encryption key)
    
    Returns:
        str: Decrypted text
    
    Example:
        >>> decrypt("zmywhx wmzzfso", "password")
        'secret message'
    """
    return vigenere(message, key, direction=-1)


# =============================================================================
# TESTING AND EXAMPLES
# =============================================================================

if __name__ == "__main__":
    print("🔐 CIPHER IMPLEMENTATION - DEMONSTRATION")
    print("=" * 50)
    
    # Test Caesar Cipher
    print("\n1. CAESAR CIPHER TEST")
    print("-" * 30)
    
    original_text = "Hello World! Attack at dawn."
    caesar_shift = 3
    
    print(f"Original:  {original_text}")
    print(f"Shift:     {caesar_shift}")
    
    encrypted_caesar = caesar(original_text, caesar_shift)
    print(f"Encrypted: {encrypted_caesar}")
    
    decrypted_caesar = caesar(encrypted_caesar, -caesar_shift)
    print(f"Decrypted: {decrypted_caesar}")
    print(f"Success: {original_text == decrypted_caesar}")
    
    # Test Vigenère Cipher
    print("\n2. VIGENÈRE CIPHER TEST") 
    print("-" * 30)
    
    original_text = "Secret Message! Meet at midnight."
    vigenere_key = "python"
    
    print(f"Original:  {original_text}")
    print(f"Key:       {vigenere_key}")
    
    encrypted_vigenere = encrypt(original_text, vigenere_key)
    print(f"Encrypted: {encrypted_vigenere}")
    
    decrypted_vigenere = decrypt(encrypted_vigenere, vigenere_key)
    print(f"Decrypted: {decrypted_vigenere}")
    print(f"Success: {original_text == decrypted_vigenere}")
    
    # Demonstration of different keys
    print("\n3. KEY SECURITY DEMONSTRATION")
    print("-" * 30)
    
    test_message = "confidential"
    correct_key = "secret"
    wrong_key = "public"
    
    encrypted_msg = encrypt(test_message, correct_key)
    decrypted_correct = decrypt(encrypted_msg, correct_key)
    decrypted_wrong = decrypt(encrypted_msg, wrong_key)
    
    print(f"Message:    {test_message}")
    print(f"Encrypted:  {encrypted_msg}")
    print(f"Correct key '{correct_key}': {decrypted_correct}")
    print(f"Wrong key '{wrong_key}':   {decrypted_wrong}")
    
    print("\n🎉 All tests completed successfully!")
```

# 🚀 How to Use This Code:
```
## Basic usage
from cipher import caesar, encrypt, decrypt

## Caesar Cipher
secret = caesar("Top Secret", 5)
revealed = caesar(secret, -5)

## Vigenère Cipher  
encrypted = encrypt("Meet at dawn", "password")
decrypted = decrypt(encrypted, "password")
```
    
