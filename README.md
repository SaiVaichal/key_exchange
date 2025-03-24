Key Exchange and Management System

Overview
This project implements a secure key management system using RSA, Diffie-Hellman, and AES encryption. The system allows for secure key generation, exchange, and management while mitigating potential security threats.

Features:

-RSA Key Pair Generation: Generates public-private key pairs for asymmetric encryption.
-Diffie-Hellman Key Exchange: Securely establishes shared secrets between parties.
-AES Symmetric Key Generation: Creates a symmetric key for fast encryption and decryption.
-In-Memory Key Storage: Keys are stored in memory instead of files for ease of use in Colab.
-Key Revocation: Allows removal of compromised keys.

Requirements

-Python 3.x
-Cryptography library (pip install cryptography)

Usage

Initialize the Key Management System:

              kms = KeyManagementSystem()

Generate keys:

              kms.generate_rsa_keys()
              kms.generate_diffie_hellman_keys()
              kms.generate_symmetric_key()

Perform secure key exchange:

              shared_secret = kms.diffie_hellman_key_exchange()

Revoke a key if compromised:

               kms.revoke_key("rsa_private")

Security Measures:

Uses strong cryptographic algorithms.
Prevents unauthorized access with key revocation.
Securely exchanges keys using Diffie-Hellman.
