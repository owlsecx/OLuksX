# 🦉 OLuksX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OLuksX** — Linux Disk-Encryption Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OLuksX is an offline, read-only Linux disk-encryption configuration auditor for LUKS1/LUKS2 headers, crypttab/fstab, TPM2/FIDO2/Clevis tokens, and related dmsetup/clevis outputs. It never decrypts or writes to devices; it scores PBKDF, cipher, keyslot, and unlock-token posture and exports TXT, Markdown, JSON, CSV, or SARIF.

---

## ✨ Features

- Raw LUKS1/LUKS2 binary header parser and `cryptsetup luksDump` / JSON metadata parsers
- PBKDF audit (LUKS1, pbkdf2, Argon2 memory/time/threads, argon2i vs argon2id)
- Cipher audit (cbc-plain/essiv, ECB, XTS key size, cipher_null, legacy ciphers, sector size)
- Keyslot hygiene and token review: systemd-tpm2, FIDO2, Clevis (tang/tpm2/sss)
- crypttab/fstab, swap & /tmp, keyfiles, header backups, dm-integrity, detached headers
- Weighted score/grade, templates, multi-format export, `--demo` and CI severity gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLuksX --scan
./OLuksX --dump luksDump.txt --crypttab /etc/crypttab -f json -o luks.json
./OLuksX --demo --fail-on high
./OLuksX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
