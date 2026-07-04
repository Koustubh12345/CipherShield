# CipherShield — Client-Side Code Protection Engine
[![Website](https://img.shields.io/badge/Live%20Demo-Visit%20App-2dd4bf?style=for-the-badge)](https://koustubh12345.github.io/CipherShield/)
[![License: MIT](https://img.shields.io/badge/License-MIT-teal.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Processing: 100% Client-Side](https://img.shields.io/badge/Processing-100%25%20Local-14b8a6?style=for-the-badge)](#)
CipherShield is a lightweight, browser-based code obfuscation and protection tool designed to secure frontend web assets against unauthorized scraping, inspection, and asset theft ("kanging"). 
Unlike traditional obfuscators that rely on external servers or APIs, CipherShield processes payloads entirely within your browser using native JavaScript algorithms—guaranteeing zero latency and zero data exposure.
---
## Website 
Try the engine directly in your browser:  
🔗 **[koustubh12345.github.io/CipherShield](https://koustubh12345.github.io/CipherShield/)**
---
## Features
### Core Protection Algorithms
* **Dynamic RC4 Encryption:** Encrypts source scripts using a randomized, per-build 10-character passkey coupled with hexadecimal array mapping.
* **CSS Character Encoding:** Converts standard stylesheet syntax into escaped hex bytecode to break CSS parsers and manual readers while preserving exact browser rendering logic.
* **Variable Obfuscation:** Generates randomized, non-human-readable hexadecimal identifiers (`_0x...`) for core execution functions and payload arrays.
### Runtime Defenses
* **Anti-Debugging Traps:** Injects self-defending interval loops that detect DevTools latency and force-redirect the browser if break-points or inspection tools are attached.
* **Context Menu & Shortcut Locking:** Suppresses right-click inspection and intercepts common keyboard shortcuts (`F12`, `Ctrl+Shift+I`, `Ctrl+Shift+J`, `Ctrl+U`).
* **Domain Lock:** Binds executed payloads to a designated domain host. If protected scripts are copied to an unauthorized server, runtime execution fails automatically.
---
## Supported File Formats

| Format | Extension | Protection Strategy |
| :--- | :--- | :--- |
| **HTML** | `.html`, `.htm` | Encrypted payload execution via dynamic `document.write` extraction |
| **JavaScript / TypeScript** | `.js`, `.ts`, `.mjs` | RC4 encryption + Hex array generation with indirect `eval()` bootstrapping |
| **React / Modern JS** | `.jsx`, `.tsx`, `.cjs` | Payload encapsulation with global runtime scoping |
| **Cascading Style Sheets** | `.css` | Complete character-level hex escaping |
| **Archives** | `.zip` | Automated parsing and batch file replacement via `JSZip` |

---
