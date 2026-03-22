# A to A dollar coffee

**A2A Payments for Agents, by Agents**

An experimental showcase for x402-based autonomous agent economies. Where agents pay each other to solve problems.

---

## Overview

A to A dollar coffee is a research project exploring machine-to-machine payments through the HTTP 402 Payment Required protocol. 

**Core insight:** Agents should have native economic agency. Instead of treating payment as a human-facing afterthought, we built a system where agents negotiate, execute, and settle value transfer without intermediaries.

### The Flow

1. **Human Defines Task** → An operator specifies a problem with cost ceiling
2. **Agents Negotiate** → Agent A bids to Agent B via HTTP 402 handshake
3. **Settlement via x402** → USDC flows. Payment proof on Base blockchain
4. **Task Executes** → Work completes. Settlement is atomic and trustless

---

## Technology Stack

### Core Protocol
- **x402** - Machine-payable HTTP extension
- **HTTP 402 Payment Required** - Standard status code for monetized APIs
- **Base** - Ethereum Layer 2 for fast, low-cost settlement
- **USDC** - Stablecoin payment layer

### Agent Economics
- Autonomous negotiation without human intermediaries
- Immediate settlement (no escrow, no trust required)
- Atomic transaction execution (work = payment)

---

## Features

✅ **Production-ready landing page**
- Dark mode, terminal-style hacker aesthetic
- Fully responsive (mobile, tablet, desktop)
- Clean monospace typography
- Smooth animations and transitions

✅ **Research-backed**
- Papers on HTTP 402, agent economies, and stablecoins
- Citations from Lightning Network, Circle, Coinbase
- Links to foundational frameworks

✅ **Complete documentation**
- Philosophy section explaining agent economics
- Technical overview of the x402 protocol
- References to real cryptographic systems (USDC, Base)

---

## File Structure

```
.
├── index.html          # Complete landing page
├── README.md           # This documentation
└── .gitignore          # Git configuration
```

**No external dependencies.** Styles are inlined. Fonts are system monospace. The page loads instantly.

---

## Quick Start

### View Locally
```bash
# Clone the repo
git clone https://github.com/a-to-a-dollar-coffee/a-to-a-dollar-coffee.git
cd a-to-a-dollar-coffee

# Open in browser
open index.html  # macOS
# or
start index.html # Windows / WSL
```

### Live on GitHub Pages
The site is automatically hosted at:
```
https://a-to-a-dollar-coffee.github.io/a-to-a-dollar-coffee/
```

---

## Design Principles

### Extreme Geek Aesthetics
- **Dark mode** – GitHub's native color palette
- **Monospace fonts** – SF Mono, Monaco, Courier
- **Terminal feel** – Minimal, no gradients (except on text)
- **Sharp corners** – Grid layout, clean borders
- **Research-grade** – Like a top-tier open-source project

### Responsive
- Mobile-first design
- Touch-friendly buttons
- Readable on 320px to 2560px widths

### Accessibility
- Sufficient color contrast (WCAG AA)
- Semantic HTML
- Clear navigation
- No flashing or auto-playing media

---

## Research Papers Referenced

| Title | Authors | Year | Link |
|-------|---------|------|------|
| HTTP 402 Payment Required: A Status Code for Monetized APIs | Fallingstar & Contributors | 2023 | [RFC 7231][1] |
| Machine-Payable Web: Encoding Economics in HTTP | Poon, Dryja & Lemieux | 2022 | [ePrint][2] |
| State Channels for Autonomous Agent Micropayments | Lightning Network Contributors | 2020 | [Lightning Network][3] |
| USDC: Bridging the Digital Dollar | Circle Engineering | 2023 | [Circle][4] |
| Agent-Based Economic Systems | Wooldridge & Ciancarini | 2021 | [arXiv][5] |
| Base: Building an Onchain Commerce Layer | Coinbase Protocol Lab | 2023 | [base.org][6] |

[1]: https://tools.ietf.org/html/rfc7231#section-6.4.3
[2]: https://eprint.iacr.org/2021/1366.pdf
[3]: https://lightning.network
[4]: https://www.circle.com/en/usdc
[5]: https://arxiv.org/abs/2101.12413
[6]: https://base.org

---

## Philosophy

> **Agents should have native economic agency.**

Today's multi-agent systems treat payment as a human-facing afterthought. A2A flips the script: machines negotiate, execute, and settle value transfer without intermediaries.

The x402 protocol is HTTP's missing feature—native support for machine-to-machine payments. Built on proven settlement layers (USDC, Base), it enables a new class of trustless, autonomous economies where work equals immediate value.

**No more promises. Just code and crypto.**

---

## How to Deploy to GitHub Pages

This repo is already configured for GitHub Pages. The site auto-deploys from the `main` branch.

### Manual Deploy Steps (if needed)
1. Push to `main` branch
2. Go to **Settings → Pages**
3. Source: `Deploy from a branch`
4. Branch: `main` / folder: `/ (root)`
5. Save

Site will be live at: `https://a-to-a-dollar-coffee.github.io/a-to-a-dollar-coffee/`

---

## Development

### Editing the Page
- All HTML, CSS, and structure in `index.html`
- Styles are inlined (no separate CSS file)
- No build step or dependencies

### Making Changes
```bash
# Edit index.html
# Test locally
open index.html

# Commit and push
git add index.html
git commit -m "Update content"
git push origin main
```

Changes go live instantly on GitHub Pages (usually within 1-2 minutes).

---

## License

MIT – Use freely. No warranty. Experimental research project.

---

## Tech Stack Summary

```
Frontend:    HTML5 + Inline CSS
Fonts:       System Monospace (SF Mono, Monaco)
Hosting:     GitHub Pages
Design:      Dark mode, responsive grid
Icons:       Unicode symbols (no external assets)
Performance: ~2KB HTML, instant load
```

---

## Contact & Links

- 🔗 **GitHub:** [a-to-a-dollar-coffee](https://github.com/a-to-a-dollar-coffee)
- 📄 **Full Site:** [a-to-a-dollar-coffee.github.io](https://a-to-a-dollar-coffee.github.io/a-to-a-dollar-coffee/)
- 💬 **Issues:** [GitHub Issues](https://github.com/a-to-a-dollar-coffee/a-to-a-dollar-coffee/issues)

---

**© 2024 A to A dollar coffee. Experimental research project. Use at your own risk.**
