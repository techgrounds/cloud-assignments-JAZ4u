# [4/ Symmetric encryption]

Encryption is an important tool for securing data. Be it data at rest, or data in motion. A lot of what you do on your computer and the Internet is encrypted.

Throughout history humanity has come up with many ciphers to encode information. Most of these are symmetric ciphers, the most famous one being the Caesar cipher.

In this assignment you will learn about the basics of cryptography, starting with symmetrical encryption.

## Key-terms

- Symmetric encryption
  
  Symmetric encryption is a type of encryption where the same key is used for both the encryption and decryption of data. In symmetric encryption, the sender and receiver share a secret key, which they use to encrypt and decrypt messages or data. This contrasts with asymmetric encryption, where a pair of keys (a public key and a private key) are used for encryption and decryption, respectively.
  
  Here's how symmetric encryption works:
  
  1. **Key Generation**: Both the sender and receiver agree on a secret key before communication begins. This key must be kept confidential and securely shared between the parties involved.
  
  2. **Encryption**: The sender uses the shared secret key to encrypt the plaintext (unencrypted message or data), transforming it into ciphertext (encrypted message or data). The encryption process scrambles the plaintext using mathematical algorithms, making it unreadable to anyone without the key.
  
  3. **Transmission**: The encrypted ciphertext is transmitted over a communication channel, such as the internet, a network, or physical media.
  
  4. **Decryption**: The receiver uses the same shared secret key to decrypt the ciphertext, reversing the encryption process and recovering the original plaintext.
  
  Key characteristics of symmetric encryption include:
  
  - **Efficiency**: Symmetric encryption algorithms are typically faster and more computationally efficient than asymmetric encryption algorithms, making them well-suited for encrypting large volumes of data.
  - **Security**: The security of symmetric encryption relies on the secrecy and strength of the shared secret key. If an attacker gains access to the key, they can decrypt the encrypted data. Therefore, the key must be securely stored and exchanged between the communicating parties.
  - **Scalability**: Symmetric encryption is scalable and can be used to secure communication between multiple parties by sharing a unique secret key for each pair of communicating entities.
  
  Common symmetric encryption algorithms include AES (Advanced Encryption Standard), DES (Data Encryption Standard), 3DES (Triple DES), and Blowfish. Symmetric encryption is widely used in various applications, including secure communication, data storage, and encryption of sensitive information in databases and applications.

- Caesar Cipher
  
  The Caesar cipher is one of the simplest and most well-known substitution ciphers in cryptography. It is named after Julius Caesar, who is believed to have used this cipher to encrypt messages.
  
  In a Caesar cipher, each letter in the plaintext (unencrypted message) is shifted a certain number of places down or up the alphabet. For example, with a shift of 3, 'A' would be replaced by 'D', 'B' would become 'E', and so on. When the end of the alphabet is reached, the cipher loops back to the beginning.
  
  Here's a simplified explanation of how the Caesar cipher works:
  
  1. Choose a shift value (also known as the key or offset). This value determines how many positions each letter in the plaintext will be shifted.
  2. Encrypt the plaintext by shifting each letter in the message according to the chosen offset.
  3. Decrypt the ciphertext by shifting each letter in the encrypted message in the opposite direction of the chosen offset.
  
  For example, using a Caesar cipher with a shift of 3:
  
  - Plaintext: "HELLO"
  - Encrypted: "KHOOR"
  - Decrypted: "HELLO"
  
  The Caesar cipher is a form of symmetric encryption, meaning the same key is used for both encryption and decryption. However, due to its simplicity, the Caesar cipher is easily breakable using brute-force or frequency analysis methods. Despite its lack of security, the Caesar cipher serves as a basic introduction to encryption concepts and is often used in educational settings or as a building block for more complex ciphers.

- digital ciphers
  
  Digital ciphers, also known as cryptographic ciphers or encryption algorithms, are mathematical techniques used to secure digital data by transforming plaintext (unencrypted data) into ciphertext (encrypted data). Ciphers play a crucial role in ensuring the confidentiality and integrity of sensitive information transmitted over digital networks or stored in electronic devices.
  
  There are two main categories of digital ciphers:
  
  1. **Symmetric Key Ciphers (Secret Key Ciphers)**:
     
     - In symmetric key cryptography, the same key is used for both encryption and decryption.
     - Examples of symmetric key ciphers include:
       - **AES (Advanced Encryption Standard)**: A widely used symmetric encryption algorithm that encrypts data in blocks and supports key sizes of 128, 192, or 256 bits.
       - **DES (Data Encryption Standard)**: An older symmetric encryption algorithm that operates on 64-bit blocks and uses a 56-bit key.
       - **3DES (Triple DES)**: A variant of DES that applies the DES algorithm three times with different keys for increased security.
       - **RC4 (Rivest Cipher 4)**: A stream cipher designed for use in cryptographic protocols, such as SSL/TLS.
  
  2. **Asymmetric Key Ciphers (Public Key Ciphers)**:
     
     - In asymmetric key cryptography, a pair of keys (public key and private key) is used for encryption and decryption, respectively.
     - Examples of asymmetric key ciphers include:
       - **RSA (Rivest-Shamir-Adleman)**: A widely used asymmetric encryption algorithm based on the difficulty of factoring large prime numbers.
       - **DSA (Digital Signature Algorithm)**: An asymmetric algorithm used for digital signatures, often used in conjunction with other algorithms like SHA (Secure Hash Algorithm).
       - **ECC (Elliptic Curve Cryptography)**: A modern asymmetric encryption algorithm based on elliptic curves, known for its efficiency and strong security.
  
  Digital ciphers can further be classified based on their operation mode, such as block ciphers (encrypting fixed-size blocks of data) or stream ciphers (encrypting data bit by bit), and their security properties, such as symmetric ciphers' resistance to brute-force attacks and asymmetric ciphers' reliance on the difficulty of mathematical problems.
  
  Overall, digital ciphers are fundamental tools in the field of cryptography, enabling secure communication, data storage, and online transactions in today's digital age. They provide a means of protecting sensitive information from unauthorized access or interception by adversaries.

- Historic Ciphers
  
  Historic ciphers, also known as classical ciphers, are encryption methods that were used before the advent of modern cryptographic techniques. These ciphers were often based on simple algorithms and relied on secrecy rather than complex mathematical principles for security. While many historic ciphers are now obsolete due to advancements in cryptanalysis, they played a significant role in the history of cryptography and are studied for their historical and educational value.
  
  Some common types of historic ciphers include:
  
  1. **Caesar Cipher**: Named after Julius Caesar, this substitution cipher involves shifting each letter of the plaintext by a fixed number of positions down or up the alphabet.
  
  2. **Monoalphabetic Substitution Cipher**: In this type of cipher, each letter of the plaintext is replaced by another letter based on a predetermined substitution key. Examples include the Atbash cipher and the simple substitution cipher.
  
  3. **Polyalphabetic Substitution Cipher**: These ciphers use multiple substitution alphabets to encrypt the plaintext, making them more resistant to frequency analysis. The Vigenère cipher is a well-known example of a polyalphabetic substitution cipher.
  
  4. **Transposition Cipher**: Transposition ciphers involve rearranging the order of the letters in the plaintext according to a specific rule or permutation. Examples include the Rail Fence cipher and the Columnar transposition cipher.
  
  5. **Playfair Cipher**: Developed in the 19th century, the Playfair cipher uses a 5x5 grid of letters to encrypt pairs of plaintext letters. It was used by diplomats and military organizations for secure communication.
  
  6. **Enigma Machine**: The Enigma machine was a complex electromechanical device used by the German military during World War II to encrypt and decrypt secret messages. It employed multiple rotors and plugboard connections to perform polyalphabetic substitution.
  
  While historic ciphers are generally considered insecure by modern standards, they remain an important part of cryptography history and are often used for educational purposes to understand the evolution of cryptographic techniques. Many historic ciphers have been extensively studied and broken using modern cryptanalysis methods, highlighting the importance of constantly advancing cryptographic techniques to ensure secure communication and data protection.
  
  

## Assignment

- Find one more historic cipher besides the Caesar cipher.
- Find two digital ciphers that are being used today.
- Send a symmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key you share with them. Try to think of a way to share this encryption key without revealing it to everyone. You are not allowed to use any private messages or other communication channels besides the public Slack channel. Analyse the shortcomings of symmetric encryption for sending messages.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

- Find one more historic cipher besides the Caesar cipher.
- Find two digital ciphers that are being used today.
- Send a symmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key you share with them. Try to think of a way to share this encryption key without revealing it to everyone. You are not allowed to use any private messages or other communication channels besides the public Slack channel. Analyse the shortcomings of symmetric encryption for sending messages.