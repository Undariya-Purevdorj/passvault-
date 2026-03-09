# PassVault — Password Manager

A browser-based password manager built as a computer security project. Demonstrates core security concepts including encryption, password strength analysis, and cryptographically secure random generation.

---

## Features

- **Master password gate** — vault is locked until authenticated
- **XOR encryption** — passwords are encrypted in memory using a master key
- **Password strength analysis** — scores passwords on length, complexity, and character variety
- **Secure password generator** — uses `crypto.getRandomValues()` (not `Math.random()`) for true randomness
- **Add, edit, delete, search** credentials
- **Show/hide and copy** passwords with one click

---

## Security Concepts Demonstrated

| Concept | Implementation |
|---|---|
| Symmetric encryption | XOR cipher with master key |
| Password entropy | Strength scoring across 5 criteria |
| Secure randomness | Web Crypto API (`getRandomValues`) |
| Zero-knowledge design | No data ever leaves the browser |

---

## Privacy by Design

This app stores all data **in memory only** — nothing is written to a server, database, or local storage. Every session starts fresh. This is an intentional design choice: there is no attack surface for a data breach because no data is ever persisted.

> **Future improvement:** Persistent storage could be added using `localStorage` with AES-256 encryption via the Web Crypto API, or a backend with hashed user accounts.

---

## Tech Stack

- Vanilla HTML, CSS, JavaScript — no frameworks, no dependencies
- Web Crypto API for password generation
- Deployed via GitHub Pages

---

## Live Demo

[https://undariya-purevdorj.github.io/passvault-/](https://undariya-purevdorj.github.io/passvault-/)

---

## Run Locally

No build steps needed. Just open `index.html` in any browser.

```bash
git clone https://github.com/Undariya-Purevdorj/passvault-.git
cd passvault-
open index.html
```

---

## Author

me
