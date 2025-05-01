Room Title: Cryptography Basics
Difficulty: Easy
Time to Complete: 45 minutes
Skills Covered:

    Plaintext to Ciphertext
    Types of Encryption
    
🏛️ Key Concepts and Lessons Learned
🔹 Plaintext to Ciphertext

     Let’s start with an illustration before introducing the key terms. We begin with the plaintext that we want to encrypt. 
     The plaintext is the readable data; it can be anything from a simple “hello”, a cat photo, credit card information, or medical health records.
     From a cryptography perspective, these are all “plaintext” messages waiting to be encrypted. The plaintext is passed through the encryption function along with a proper key; the encryption function returns a ciphertext. 
     The encryption function is part of the cipher; a cipher is an algorithm to convert a plaintext into a ciphertext and vice versa.
     To recover the plaintext, we must pass the ciphertext along with the proper key via the decryption function, which would give us the original plaintext.

🔹 Types of Encryption

    The two main categories of encryption are symmetric and asymmetric.
    Symmetric Encryption
    Symmetric encryption, also known as symmetric cryptography, uses the same key to encrypt and decrypt the data, as shown in the figure below. Keeping the key secret is a must; it is also called private key cryptography. Furthermore, communicating the key to the intended parties can be challenging as it requires a secure communication channel. Maintaining the secrecy of the key can be a significant challenge, especially if there are many recipients. The problem becomes more severe in the presence of a powerful adversary; consider the threat of industrial espionage, for instance.
    Symmetric encryption uses the shared secret key for encryption and decryption. Consider the simple case where you created a password-protected document to share it with your colleague. 
    You can easily email the encrypted document to your colleague, but most likely, you cannot email them the password. The reason is that anyone with access to their mailbox would access both the password-protected document and its password.
    Therefore, you need to think of a different way, i.e., channel, to share the password. Unless you think of a secure, accessible channel, one solution would be to meet in person and communicate the password to them.

    Examples of symmetric encryption are DES (Data Encryption Standard), 3DES (Triple DES) and AES (Advanced Encryption Standard).

    DES was adopted as a standard in 1977 and uses a 56-bit key. With the advancement in computing power, in 1999, a DES key was successfully broken in less than 24 hours, motivating the shift to 3DES.
    3DES is DES applied three times; consequently, the key size is 168 bits, though the effective security is 112 bits. 3DES was more of an ad-hoc solution when DES was no longer considered secure. 3DES was deprecated in 2019 and should be replaced by AES; however, it may still be found in some legacy systems.
    AES was adopted as a standard in 2001. Its key size can be 128, 192, or 256 bits.

    Asymmetric Encryption

    Unlike symmetric encryption, which uses the same key for encryption and decryption, asymmetric encryption uses a pair of keys, one to encrypt and the other to decrypt, as shown in the illustration below. 
    To protect confidentiality, asymmetric encryption or asymmetric cryptography encrypts the data using the public key; hence, it is also called public key cryptography.

    There are many more symmetric encryption ciphers used in various applications; however, they have not been adopted as standards.

    Examples are RSA, Diffie-Hellman, and Elliptic Curve cryptography (ECC). The two keys involved in the process are referred to as a public key and a private key. Data encrypted with the public key can be decrypted with the private key. Your private key needs to be kept private, hence the name.

    Asymmetric encryption tends to be slower, and many asymmetric encryption ciphers use larger keys than symmetric encryption. For example, RSA uses 2048-bit, 3072-bit, and 4096-bit keys; 2048-bit is the recommended minimum key size. 
    Diffie-Hellman also has a recommended minimum key size of 2048 bits but uses 3072-bit and 4096-bit keys for enhanced security. On the other hand, ECC can achieve equivalent security with shorter keys. 
    For example, with a 256-bit key, ECC provides a level of security comparable to a 3072-bit RSA key.

    Asymmetric encryption is based on a particular group of mathematical problems that are easy to compute in one direction but extremely difficult to reverse. In this context, extremely difficult means practically infeasible.  
    For example, we can rely on a mathematical problem that would take a very long time, for example, millions of years, to solve using today’s technology.

    We will visit various asymmetric encryption ciphers in the next room. For now, the important thing to note is that asymmetric encryption provides you with a public key that you share with everyone and a private key that you keep guarded and secret.

🔍 Reflection

This room helped me to know some more about one of the most important concepts in cybersecurity that is encryption.
