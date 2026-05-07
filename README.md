# Triple DES (3DES) Encryption

A from-scratch Python implementation of the **Triple DES (3DES)** encryption algorithm, built as part of the **Information Security** course at **German International University (GIU)**, Spring 2026.

## Overview

The project implements DES encryption and decryption step by step, then extends it to the full 3DES EDE (Encrypt-Decrypt-Encrypt) scheme, and finally applies it to encrypt a multi-block plaintext message.

## What's Implemented

### Stage 1 — DES Core
A full 16-round DES encryption function that displays the output of every intermediate step:
- Initial Permutation (IP)
- Expansion (32 → 48 bits)
- Key Mixing (XOR with round key)
- S-Box Substitution (48 → 32 bits)
- Permutation P
- Half-swap after round 16
- Final Permutation (FP)

### Stage 2 — Triple DES (EDE)
Extends DES to the 3DES EDE structure using three independent keys:
```
Encrypt with K1 → Decrypt with K2 → Encrypt with K3
```
Shows the output after each of the three stages for a 64-bit block.

### Stage 3 — Multi-block Encryption
Encrypts a full plaintext string (`"Hello 3DES Encryption"`) by splitting it into 64-bit blocks with padding, applying 3DES to each block, and displaying the ciphertext.

## Keys Used

| Key | Hex Value |
|-----|-----------|
| K1 | `0x0123456789ABCDEF` |
| K2 | `0xFEDCBA9876543210` |
| K3 | `0x89ABCDEF01234567` |

## Project Structure

```
3DES-Encryption/
├── TeamNotebook.ipynb    # Full implementation notebook
└── README.md
```

## Technologies

- Python 3
- Google Colab
- No external libraries — pure Python implementation

## Author

**Ahmed Saadallah** — 16008325

**Course:** Information Security — GIU, Spring 2026
