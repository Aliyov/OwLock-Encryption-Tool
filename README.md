# 🦉 OwLock – File Encryption v1.0

OwLock is a **modern file encryption manager** built with **Python (Tkinter + Cryptography)**.  
It allows you to securely encrypt and decrypt files with **AES-256-GCM**, manage storage in a hidden folder, and protect access with a **login system**.

<img width="1210" height="803" alt="Image" src="https://github.com/user-attachments/assets/dac80000-e74e-4310-b1ce-67cfafc99184" />


## 🔐 AES-256-GCM Encryption

OwLock uses **AES-256 (Advanced Encryption Standard)** in **GCM (Galois/Counter Mode)** to secure your files.

### What is AES-256?
- **AES** is a symmetric block cipher standardized by NIST.
- **256-bit key length** provides extremely strong security, brute-force attacks are practically impossible with today’s computing power.
- Adopted by governments, enterprises, and security experts as the gold standard for encryption.

### What is GCM (Galois/Counter Mode)?
- GCM is an **authenticated encryption mode** that combines:
  - **Confidentiality** (keeps your data secret).
  - **Integrity** (ensures no one can tamper with your files).
- Each file uses a unique **nonce (96-bit random value)** to prevent replay or duplication attacks.
- A **16-byte authentication tag** is appended to every encrypted file to verify data integrity.

### How OwLock Uses AES-256-GCM
1. **Encryption**
   - Generates a **256-bit random key** (stored as `secret.key` or exported).
   - Creates a **unique 96-bit nonce** per file.
   - Encrypts the file content into **ciphertext**.
   - Appends a **16-byte authentication tag** to detect tampering.

2. **Decryption**
   - Reads the nonce, ciphertext, and authentication tag from the `.enc` file.
   - Verifies the tag before decryption (if verification fails, the file is rejected).
   - Restores the original file when authentication passes.

### Security Benefits
-  **Confidentiality**: Your files remain unreadable without the secret key.  
-  **Integrity**: Even a one-byte modification causes decryption to fail.  
-  **Performance**: GCM is optimized for modern CPUs, making it both fast and secure.  

---

<img width="1127" height="997" alt="Image" src="https://github.com/user-attachments/assets/31a5fad0-c050-4937-972c-2a1bb3680633" />

---------------------

<img width="619" height="566" alt="Image" src="https://github.com/user-attachments/assets/c36df997-13b9-4e18-b9e8-a3d7e3e55e17" />

---------------------

<img width="689" height="708" alt="Image" src="https://github.com/user-attachments/assets/d1679d7c-8a4e-43a2-8dd2-218d7b0ee218" />

---------------------

##  Features

-  **AES-256-GCM Encryption**
  - Industry-standard encryption with nonce + tag for integrity.
  - Prevents double encryption of `.enc` files.
-  **Secure File Storage**
  - Files stored inside a hidden folder (`.my_hidden_folder`).
  - Remove originals after encryption.
-  **Login System**
  - User authentication before accessing OwLock.
-  **File Management**
  - Add, move, open, and view encrypted files directly from the UI.
-  **Key Management**
  - Generate secret key (`secret.key`) once, reuse across sessions.
  - Option to **save internally** or **export** to a custom location.
  - Automatically deletes `secret.key` after decryption for extra security.

---

