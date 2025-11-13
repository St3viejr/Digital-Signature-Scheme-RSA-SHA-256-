# RSA Digital Signature Scheme (Python)

This project demonstrates the core concepts of a digital signature scheme using the **RSA** asymmetric-key algorithm and the **SHA-256** hashing function.

The script performs the three essential stages:
1.  **Key Generation:** Creates a 2048-bit RSA public/private key pair and saves them as `.pem` files.
2.  **Signing:** Creates a digital signature for a file (`testfile.txt`). This process involves hashing the file with SHA-256 and then encrypting that hash with the **private key**.
3.  **Verification:** Verifies the signature. This process uses the **public key** to decrypt the signature, re-computes the hash of the file, and compares the two.

---

### Skills Demonstrated

* Python
* Cryptography (Asymmetric-key)
* RSA Key Generation
* SHA-256 Hashing
* Digital Signatures (Signing & Verification)
* File I/O (Binary Read/Write)

---

### How to Run

1.  **Clone/Download:** Place the script in a new folder.
2.  **Create an Input File:** In the same folder, you **must create a file named `testfile.txt`**. Write any message inside it (e.g., "This is the original message.").
3.  **Set up Environment:** It's best to use a virtual environment.
    ```bash
    # Create the venv
    python -m venv venv

    # Activate the venv
    venv\Scripts\activate
    ```
4.  **Install Dependencies:** This script requires the `cryptography` library.
    ```bash
    pip install cryptography
    ```
5.  **Run the Script:**
    ```bash
    python rsa_digital_signature_verification.py
    ```

### Output

When you run the script, it will:
1.  **Create 3 new files:** `private_key.pem`, `public_key.pem`, and `signature.sig`.
2.  **Print to your terminal:**
    ```
    File has been signed successfully...
    Signature is valid...
    ```
