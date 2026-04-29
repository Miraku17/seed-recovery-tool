# Seed Recovery Tool

Single-file offline form that builds the exact `recover.py` command for restoring a partially-known BIP39 seed phrase on a rented server.

## How to use

Open https://miraku17.github.io/seed-recovery-tool/ in your browser **with Wi-Fi off**, fill the form, copy the two commands it generates, and paste them on your recovery server.

## Security

- Page is fully self-contained — no external scripts, no network calls.
- CSP `connect-src 'none'` enforces it: even if the page tried to phone home, the browser would block it.
- Your seed words never leave the page.
- The recovery script's SHA-256 is embedded; the generated run command verifies it on the server before executing.

## What's in this repo

- `index.html` — the form (60 KB, includes the embedded BIP39 wordlist + base64-encoded `recover.py`)

## Source

This file is built from the seed-recovery toolkit in a private repo. The `recover.py` source is open and inspectable via the form's "Advanced" download.
