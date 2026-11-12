---
nfc: patch
---

Fix `Nfc::scan` failing to decode every scanned tag from Rust. `NfcTag::id` is now `Vec<u8>` and `NfcTag::kind` is `Vec<String>`, matching what Android and iOS send, and the byte fields also accept the signed bytes Android sends for values from `0x80` up.
