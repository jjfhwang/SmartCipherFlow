# SmartCipherFlow: Streamlined Data Encryption and Decryption

SmartCipherFlow is a Python library designed to simplify and automate data encryption and decryption processes. It provides a robust and efficient framework for securing sensitive information across various applications, from local file storage to network communication. This project aims to abstract away the complexities of cryptographic algorithms, allowing developers to focus on their core business logic while ensuring data security.

The library offers a modular architecture that supports multiple encryption algorithms, including AES, RSA, and ChaCha20, with configurable key lengths and operating modes. SmartCipherFlow streamlines the integration of encryption into existing workflows by providing a consistent and intuitive API for encryption, decryption, key generation, and key management. It features automatic salt generation, IV handling, and padding schemes to prevent common cryptographic vulnerabilities. The library's design emphasizes performance, security, and ease of use, making it suitable for both small-scale projects and enterprise-level applications.

Beyond basic encryption and decryption, SmartCipherFlow provides advanced features like secure key storage using industry-standard techniques such as Argon2 for password hashing and key derivation. It also supports key rotation mechanisms for enhanced security and compliance with regulatory requirements. The library includes comprehensive error handling and logging capabilities, enabling developers to easily diagnose and resolve encryption-related issues. SmartCipherFlow is committed to providing a secure and reliable solution for data protection, with ongoing updates and security audits to address emerging threats.

### Key Features

*   **Multi-Algorithm Support:** Supports AES (Advanced Encryption Standard) with configurable key sizes (128, 192, 256 bits) and modes (CBC, CTR, GCM), RSA (Rivest-Shamir-Adleman) with customizable key lengths, and ChaCha20 stream cipher for high-performance encryption. The choice of algorithm is configurable via a simple API call.
*   **Automated Key Management:** Generates secure random keys, salts, and Initialization Vectors (IVs) automatically. Implements secure key derivation using Argon2 to protect master keys derived from passwords. Supports key rotation for improved security posture.
*   **Secure Key Storage:** Allows for secure storage of encryption keys using operating system-specific keychains (e.g., Keychain on macOS, Credential Vault on Windows) or encrypted storage mechanisms with strong authentication.
*   **Padding Schemes:** Implements PKCS#7 padding and supports disabling padding for scenarios where data is already properly formatted, preventing padding oracle attacks.
*   **Error Handling and Logging:** Provides detailed error messages and logging capabilities to facilitate debugging and troubleshooting. Includes robust input validation to prevent common vulnerabilities.
*   **Streaming Encryption:** Supports streaming encryption and decryption for handling large files efficiently without loading the entire file into memory.
*   **Configurable Cipher Parameters:** Allows developers to fine-tune cipher parameters such as block size, key derivation functions, and iteration counts for optimal performance and security based on the application's requirements.

### Technology Stack

*   **Python:** The primary programming language used for development. Python's versatility and rich ecosystem make it an ideal choice for building a robust and user-friendly encryption library.
*   **Cryptography:** The `cryptography` library provides low-level cryptographic primitives and building blocks. SmartCipherFlow leverages this library to implement the core encryption and decryption functionalities.
*   **Argon2-cffi:** Used for password-based key derivation. Argon2 is a modern key derivation function that is resistant to various attacks, including brute-force and rainbow table attacks.
*   **OS:** Provides access to operating system functionalities for secure key storage and retrieval. The `OS` module is used to interact with system-level keychains and credential vaults.
*   **Logging:** Python's built-in logging module is used for comprehensive logging and debugging. Logs can be configured to output to files, consoles, or other logging services.

### Installation

1.  **Prerequisites:** Ensure that Python 3.7 or higher is installed on your system.

2.  **Install using pip:** Open your terminal or command prompt and run the following command:

    `pip install SmartCipherFlow`

3.  **Verify Installation:** After the installation is complete, you can verify it by importing the library in a Python interpreter:

    `python`
    `import SmartCipherFlow`
    `print("SmartCipherFlow installed successfully!")`

### Configuration

SmartCipherFlow utilizes environment variables for configuration. While the default settings are sufficient for most use cases, you can customize the behavior of the library by setting the following environment variables:

*   `SMARTCIPHERFLOW_DEFAULT_ALGORITHM`: Specifies the default encryption algorithm to use (e.g., "AES", "RSA", "ChaCha20"). Defaults to "AES".
*   `SMARTCIPHERFLOW_AES_KEY_SIZE`: Specifies the key size for AES encryption (e.g., 128, 192, 256). Defaults to 256.
*   `SMARTCIPHERFLOW_ARGON2_SALT_LENGTH`: Specifies the length of the salt used for Argon2 key derivation. Defaults to 16.

These environment variables can be set in your system's environment settings or within your application's configuration file.

### Usage

**Encryption and Decryption:**

Consider this example for using AES encryption:



**Key Generation and Management:**



### Contributing

We welcome contributions to SmartCipherFlow! To contribute, please follow these guidelines:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Write clear and concise code with detailed comments.
4.  Add unit tests to verify the correctness of your changes.
5.  Submit a pull request with a clear description of your changes.

### License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/jjfhwang/SmartCipherFlow/blob/main/LICENSE) file for details.

### Acknowledgements

We would like to thank the developers of the `cryptography` and `argon2-cffi` libraries for their invaluable contributions to the field of cryptography.