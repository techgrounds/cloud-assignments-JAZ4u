# [5/ Asymmetric encryption]

The previous assignment introduced you to cryptography and symmetric encryption. In the previous exercise, you shared your encryption key with the recipient of your message. This means that anyone who has the key can decrypt the message.

Asymmetric encryption solves this issue. Instead of 1 key, you get 2: A public key, and a private key.

## Key-terms

- Asymmetric encryption
  
  Asymmetric encryption, also known as public-key cryptography, is a cryptographic technique that uses a pair of keys for encryption and decryption: a public key and a private key. These keys are mathematically related, but they are not the same. The public key is freely available to anyone and is used for encryption, while the private key is kept secret and is used for decryption.
  
  Here's how asymmetric encryption works:
  
  1. **Key Generation**: A user generates a pair of keys—a public key and a private key. These keys are mathematically linked, but it is computationally infeasible to derive the private key from the public key.
  
  2. **Encryption**: To send an encrypted message to a recipient, the sender obtains the recipient's public key. The sender then uses this public key to encrypt the message, transforming it into ciphertext.
  
  3. **Decryption**: The recipient receives the ciphertext and uses their private key to decrypt it, recovering the original plaintext message. Only the recipient, who possesses the corresponding private key, can decrypt the message.
  
  Key characteristics of asymmetric encryption include:
  
  - **Security**: Asymmetric encryption provides strong security, as the private key is kept secret and never shared or transmitted. Even if an attacker obtains the public key, they cannot decrypt messages without the corresponding private key.
  
  - **Authentication**: Asymmetric encryption can also be used for authentication purposes. A sender can encrypt a message using their private key, and recipients can verify the sender's identity by decrypting the message with the sender's public key. This process ensures message integrity and non-repudiation.
  
  - **Key Distribution**: Asymmetric encryption eliminates the need for secure key exchange, as each user generates their own key pair. Public keys can be freely distributed and shared, while private keys are kept confidential.
  
  - **Computational Complexity**: Asymmetric encryption algorithms are typically slower and more computationally intensive than symmetric encryption algorithms. Therefore, they are often used for securing communication channels, digital signatures, and key exchange protocols rather than encrypting large volumes of data.
  
  Common asymmetric encryption algorithms include RSA (Rivest-Shamir-Adleman), Elliptic Curve Cryptography (ECC), and Diffie-Hellman key exchange. Asymmetric encryption is widely used in various applications, including secure communication, digital signatures, and securing online transactions.

- Public key
  
  A public key is a cryptographic key that is made available to the public and is used in asymmetric encryption systems, such as RSA or ECC (Elliptic Curve Cryptography). In asymmetric encryption, each participant has a pair of keys: a public key and a private key.
  
  The public key is used for encryption and verifying digital signatures. It is freely distributed and can be shared with anyone. However, it cannot be used to decrypt data encrypted with it. Instead, data encrypted with a public key can only be decrypted by its corresponding private key.
  
  Key properties of a public key include:
  
  1. **Encryption**: A sender who wants to send an encrypted message to a recipient uses the recipient's public key to encrypt the message. Once encrypted, only the recipient, who possesses the corresponding private key, can decrypt the message.
  
  2. **Verification**: Digital signatures are often used for authentication and message integrity. A sender can create a digital signature by encrypting a message hash with their private key. The recipient can then verify the signature using the sender's public key. If the signature is valid, it provides assurance that the message was indeed sent by the claimed sender and has not been altered in transit.
  
  3. **Key Distribution**: Public keys are distributed widely and can be shared openly. They are often published in public key directories or included in digital certificates, which are used to authenticate the identity of individuals, organizations, or websites.
  
  It's important to note that while public keys are publicly available and can be shared openly, the corresponding private keys must be kept confidential and securely stored by the key owner. If a private key is compromised, it can lead to unauthorized access to encrypted data or impersonation in digital signatures.

- Private key
  
  A private key is a cryptographic key that is kept secret and known only to the owner. It is used in asymmetric encryption systems, such as RSA or ECC (Elliptic Curve Cryptography), alongside a corresponding public key.
  
  In asymmetric encryption, each participant has a pair of keys: a public key and a private key. The private key is used for decryption and signing digital signatures. It is crucial to keep the private key confidential and securely stored, as its compromise can lead to unauthorized access to encrypted data or impersonation in digital signatures.
  
  Key properties of a private key include:
  
  1. **Decryption**: A recipient who receives an encrypted message uses their private key to decrypt the message. The message was likely encrypted using the recipient's corresponding public key.
  
  2. **Digital Signatures**: A sender can create a digital signature by encrypting a message hash with their private key. This signature can be verified by anyone with access to the sender's public key. If the signature is valid, it provides assurance that the message was indeed sent by the claimed sender and has not been altered in transit.
  
  3. **Key Generation**: Private keys are generated along with their corresponding public keys in asymmetric encryption systems. The private key is typically generated randomly and must be sufficiently long and complex to resist brute-force attacks.
  
  4. **Key Storage**: Private keys must be securely stored to prevent unauthorized access. They are often stored in encrypted form on secure hardware devices called cryptographic tokens or in software-based secure storage known as key stores.
  
  5. **Key Usage**: Private keys are used for sensitive cryptographic operations and should not be shared or exposed to unauthorized parties. They are used to protect confidential data, authenticate users, and sign digital transactions.
  
  Overall, private keys play a critical role in ensuring the security and integrity of encrypted communications, digital signatures, and other cryptographic operations in asymmetric encryption systems. It is essential to follow best practices for private key management to prevent security breaches and maintain trust in cryptographic systems.

- Key pair
  
  A key pair refers to a pair of cryptographic keys that are mathematically related to each other in asymmetric encryption systems. This pair consists of a public key and a private key, both of which are generated simultaneously.
  
  Here's how a key pair works:
  
  1. **Public Key**: The public key is made available to anyone and is used for encryption and verifying digital signatures. It can be freely distributed and shared openly. However, it cannot be used to decrypt data encrypted with it.
  
  2. **Private Key**: The private key is kept secret and known only to the owner. It is used for decryption and signing digital signatures. The private key must be securely stored and kept confidential, as its compromise can lead to unauthorized access to encrypted data or impersonation in digital signatures.
  
  Key pairs are generated using cryptographic algorithms, such as RSA (Rivest-Shamir-Adleman) or ECC (Elliptic Curve Cryptography). These algorithms produce a pair of keys that are mathematically linked, meaning that data encrypted with one key can only be decrypted with the other key in the pair.
  
  Key pairs are used in various cryptographic applications, including:
  
  - **Secure Communication**: Key pairs are used to establish secure communication channels between parties. One party encrypts data using the recipient's public key, and the recipient decrypts the data using their corresponding private key.
  
  - **Digital Signatures**: Key pairs are used to create and verify digital signatures, which provide authentication and message integrity. A sender signs a message using their private key, and recipients can verify the signature using the sender's public key.
  
  - **Authentication**: Key pairs are used for user authentication in systems such as SSH (Secure Shell) and SSL/TLS (Secure Sockets Layer/Transport Layer Security). Users authenticate themselves by presenting credentials signed with their private keys, which can be verified using their corresponding public keys.
  
  Overall, key pairs play a crucial role in ensuring the security and integrity of cryptographic operations in asymmetric encryption systems. They enable secure communication, authentication, and digital signatures, helping to protect sensitive data and ensure trust in digital transactions.
  
  

## Assignment

- Generate a key pair.
- Send an asymmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key. The recipient should be able to read the message, but it should remain a secret to everyone else. You are not allowed to use any private messages or other communication channels besides the public Slack channel. Analyse the difference between this method and symmetric encryption.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

- Generate a key pair.
- Send an asymmetrically encrypted message to one of your peers via the public Slack channel. They should be able to decrypt the message using a key. The recipient should be able to read the message, but it should remain a secret to everyone else. You are not allowed to use any private messages or other communication channels besides the public Slack channel. Analyse the difference between this method and symmetric encryption.