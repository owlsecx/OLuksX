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

Linux disk-encryption (LUKS / crypttab / TPM2 / FIDO2) configuration auditor

---

## ✨ Features

- Read-only raw LUKS1 / LUKS2 binary header parser (struct; primary + secondary header, SHA-256 csum, LUKS2 JSON metadata area) for devices and images
- `cryptsetup luksDump` text parser (LUKS1 & LUKS2) and `--dump-json-metadata` JSON parser
- PBKDF audit — LUKS1, pbkdf2, iterations, Argon2 memory / time / threads, argon2i vs argon2id
- Cipher audit — cbc-plain, cbc-essiv, ECB, XTS key size, cipher_null, legacy ciphers, sector size
- Keyslot hygiene — count, stale / unbound slots, AF stripes, keyslot encryption, recovery options
- Tokens — systemd-tpm2 (PIN, PCRs, bank), FIDO2 (up / uv / clientPin), Clevis (tang http, tpm2, sss)
- /etc/crypttab, /etc/fstab, swap & /tmp, keyfiles, header backups, dm-integrity, detached headers
- `clevis luks list` and `dmsetup table` parsers (volume keys are never displayed or stored)
- Weighted score + A+…F grade, hardened templates
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OLuksX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
