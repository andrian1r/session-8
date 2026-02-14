# session-8
A simple Python Caesar Cipher program that performs text encoding and decoding using shift-based encryption logic.
# 🔐 Caesar Cipher Program (Python)

## 📖 Overview

This project is a simple implementation of the Caesar Cipher encryption technique using Python.

The Caesar Cipher is a basic encryption method where each letter in the text is shifted by a certain number of positions in the alphabet.

This program allows users to:

- Encode (encrypt) text
- Decode (decrypt) text
- Enter a custom shift number

---

## 🧠 Concepts Used

- Lists
- Functions
- String manipulation
- Conditional statements
- Modulo operator `%`
- User input handling
- Basic cryptography logic

---

## 🔎 How It Works

1. The user chooses:
   - `encode` → to encrypt
   - `decode` → to decrypt
2. The user enters a message.
3. The user enters a shift number.
4. The program shifts each letter in the alphabet based on the shift value.
5. The result is displayed on the screen.

The modulo operator ensures the alphabet wraps correctly (e.g., shifting after `z` goes back to `a`).

---

## 💻 Full Code

```python
alphabet = ["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"]

direction = input("ketik 'encode' untuk encrypt, ketik 'decode' untuk decrypt\n").lower()
text = input("ketik pesanmu:\n").lower()
shift = int(input("ketik nomor shift:\n"))

def caesar(original_text, shift_amount, encode_or_decode):
    output_text = ""

    if encode_or_decode == "decode":
        shift_amount *= -1

    for letter in original_text:
        shifted_position = alphabet.index(letter) + shift_amount
        shifted_position %= len(alphabet)
        output_text += alphabet[shifted_position]

    print(f"Ini adalah hasil {encode_or_decode}: {output_text}")

caesar(text, shift, direction)
```

---

## 🧪 Example

Input:
```
encode
hello
3
```

Output:
```
khoor
```

---

## 🛠 Requirements

- Python 3.x

---

## 👤 Author

Andrian Wijaya

---

## 📜 License

This project is created for educational purposes.
