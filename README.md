# e2ee

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A browser-based helper tool for end-to-end encrypted messaging. It uses Ed25519/X25519 for key exchange and AES-256-GCM for encryption.

## Demo

[E2EE - Ed25519 version](https://code4fukui.github.io/e2ee/)

## Features

-   **Secure Cryptography**: Implements Ed25519 for key pair generation, X25519 for shared secret derivation, and AES-256-GCM for message encryption/decryption.
-   **Browser-Based**: Runs entirely in the browser using the Web Crypto API.
-   **Serverless Operation**: After the initial page load, no further communication is made with the server, ensuring privacy.
-   **Self-Contained**: A single HTML file with no external dependencies to install.

## Usage

The demo provides a simple interface to perform end-to-end encryption.

1.  **Generate Keys**: Click the **"1. Create key pair..."** button to generate your private and public keys. Keep your private key secret.
2.  **Exchange Public Keys**: Share your generated **Public key** with a peer. Paste the public key you receive from them into the **"2. Peer's public key"** field.
3.  **Create Shared Key**: Click the **"3. Create shared key..."** button. This uses your private key and your peer's public key to derive a common shared key that is identical for both of you.
4.  **Encrypt**: Type a message into the left text area and click **"Encrypt →"**. The encrypted ciphertext will appear on the right.
5.  **Decrypt**: To decrypt a message, paste the ciphertext into the right text area and click **"← Decrypt"**. The original message will appear on the left.

## Dependencies

-   [sec.js](https://github.com/code4fukui/sec.js): A library for Ed25519, X25519, and AES-256-GCM using the Web Crypto API.
-   [Base16](https://github.com/code4fukui/Base16): For encoding and decoding keys and ciphertexts.

## See Also

-   [E2EE Cybersecurity at Kamiyama Marugoto Kosen (Blog Post in Japanese)](https://fukuno.jig.jp/3908)

## License

MIT License — see [LICENSE](LICENSE).