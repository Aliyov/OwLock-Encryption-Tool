# 🔐 OwLock – Secure File Manager

OwLock is a **modern file encryption manager** built with **Python (Tkinter + Cryptography)**.  
It allows you to securely encrypt and decrypt files with **AES-256-GCM**, manage storage in a hidden folder, and protect access with a stylish **login system**.


---

## ✨ Features

- 🔑 **AES-256-GCM Encryption**
  - Industry-standard encryption with nonce + tag for integrity.
  - Prevents double encryption of `.enc` files.
- 📂 **Secure File Storage**
  - Files stored inside a hidden folder (`.my_hidden_folder`).
  - Option to remove originals after encryption.
- 🔒 **Login System**
  - User authentication before accessing OwLock.
  - Sleek modern login UI inspired by Adobe/Meta design.
- 🎨 **Modern Themed UI**
  - Tokyo Night inspired dark theme.
  - Custom pill-shaped buttons and Audiowide font integration.
- 🗂 **File Management**
  - Add, move, open, and view encrypted files directly from the UI.
- 🔐 **Key Management**
  - Generate secret key (`secret.key`) once, reuse across sessions.
  - Option to **save internally** or **export** to a custom location.
  - Automatically deletes `secret.key` after decryption for extra security.

---

