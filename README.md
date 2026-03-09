# passVault — password manager

a browser-based password manager built as a computer security project. 
demonstrates core security concepts including encryption, password strength analysis, and cryptographically secure random generation.

---

## features

- **master password gate** — vault is locked until authenticated
- **XOR encryption** — passwords are encrypted in memory using a master key
- **password strength analysis** — scores passwords on length, complexity, and character variety
- **secure password generator** — uses `crypto.getRandomValues()` (not `Math.random()`) for true randomness
- **add, edit, delete, search** credentials
- **show/hide and copy** passwords with one click

---

## security concepts demonstrated

| concept | implementation |
|---|---|
| symmetric encryption | XOR cipher with master key |
| password entropy | strength scoring across 5 criteria |
| secure randomness | web crypto API (`getRandomValues`) |
| zero-knowledge design | no data ever leaves the browser |

---

## privacy by design

this app stores all data **in memory only** — nothing is written to a server, database, or local storage. every session starts fresh. this is an intentional design choice: there is no attack surface for a data breach because no data is ever persisted.

> **future improvement:** persistent storage could be added using `localStorage` with AES-256 encryption via the Web Crypto API, or a backend with hashed user accounts.

---

## tech stack

- vanilla HTML, CSS, JavaScript — no frameworks, no dependencies
- web crypto API for password generation
- deployed via GitHub Pages

---

## live demo

[https://undariya-purevdorj.github.io/passvault-/](https://undariya-purevdorj.github.io/passvault-/)

---

## run locally

no build steps needed. just open `index.html` in any browser.

```bash
git clone https://github.com/Undariya-Purevdorj/passvault-.git
cd passvault-
open index.html
```

---

## Author

me
