# 🔐 ElGamal Encryption and Decryption

An educational implementation of **ElGamal Asymmetric Cryptography** using Python to demonstrate message encryption, ciphertext generation, and decryption using public and private keys.

## 📌 About the Project

ElGamal is a public-key cryptographic algorithm that uses two different keys:
- **Public Key:** Used to encrypt messages.
- **Private Key:** Used to decrypt messages.

This project demonstrates how a plaintext message is converted into numerical values, encrypted using modular arithmetic, and recovered through decryption.

## ✨ Features

- Public and private key generation
- Text-to-numeric conversion
- ElGamal message encryption
- Ciphertext generation using `(c1, c2)` pairs
- Decryption using the private key
- Modular exponentiation and modular inverse calculations
- Original message recovery

## 🛠️ Technologies Used

- Python 3.8+
- SymPy (for modular inverse calculations)

## ⚙️ Installation

**1. Clone the repository**

```bash
git clone https://github.com/YOUR_USERNAME/elgamal-encryption-decryption.git
```

**2. Open the project folder**

```bash
cd elgamal-encryption-decryption
```

**3. Install the required library**

```bash
pip install sympy
```

## ▶️ How to Run

Run the Python program:

```bash
python elgamal.py
```

## 🔢 How It Works

### 1. Key Generation

Choose the public parameters `p` and `g`, and a private key `x`.

Calculate the public key:

\[
y = g^x \bmod p
\]

### 2. Encryption

Convert each character into a numerical value `m`, then choose a random ephemeral key `k`.

Calculate:

\[
c_1 = g^k \bmod p
\]

\[
c_2 = m \times y^k \bmod p
\]

The ciphertext is represented as:

`(c1, c2)`

### 3. Decryption

Calculate the shared secret:

\[
s = c_1^x \bmod p
\]

Calculate its modular inverse \(s^{-1}\), then recover the message:

\[
m = c_2 \times s^{-1} \bmod p
\]

Finally, convert the numerical values back into characters.

## 💻 Example

**Input:**

```text
HELLO
```

**Output:**

```text
Original Message: HELLO
Encrypted Message: [(c1, c2), ...]
Decrypted Message: HELLO
```

The actual ciphertext values depend on the encryption parameters and ephemeral keys.

## 🎯 Learning Objectives

- Understand asymmetric cryptography.
- Learn public-key and private-key concepts.
- Practice modular arithmetic and exponentiation.
- Understand encryption and decryption workflows.
- Explore how plaintext is transformed into ciphertext.

## ⚠️ Disclaimer

This project is intended for **educational purposes only**. The small demonstration parameters and fixed ephemeral key used in a basic example are not suitable for real-world security. Production cryptographic systems require secure randomness, appropriate parameter sizes, and carefully reviewed implementations.



⭐ If you find this project useful, consider giving the repository a star!
