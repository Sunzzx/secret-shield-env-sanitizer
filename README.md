# 🛡️ SecretShield — Client-Side Zero-Knowledge .env Sanitizer & Secret Vault

[![Live Demo](https://img.shields.io/badge/Live-Production-10b981?style=for-the-badge&logo=vercel)](https://secret-shield-env-sanitizer.vercel.app)
[![License: MIT](https://img.shields.io/badge/License-MIT-06b6d4?style=for-the-badge)](LICENSE)
[![Zero Telemetry](https://img.shields.io/badge/Telemetry-Zero%20Data%20Collected-success?style=for-the-badge)](https://secret-shield-env-sanitizer.vercel.app)

> **Never leak your AWS, Stripe, OpenAI, or database credentials to ChatGPT, Claude, Slack, or GitHub issues ever again.**

---

## ⚡ The Problem
Every single developer has accidentally pasted a live `.env` file into:
1. **ChatGPT or Claude** while asking for debugging help.
2. **A public GitHub Issue or PR** while filing a bug report.
3. **A company Slack channel or Discord** while sharing config with a teammate.

The moment a production Stripe `sk_live_...` or AWS `AKIA...` key leaves your machine, bots scrape and drain it within minutes.

## 💡 The Solution: SecretShield
SecretShield is a **100% in-browser, client-side zero-knowledge security workbench**:
- **Zero Server Roundtrips:** Your keys NEVER leave your browser. All computations happen in a local sandbox using the browser's native JavaScript execution engine.
- **40+ Production Secret Signatures:** Detects Stripe keys, AWS Access Keys, OpenAI tokens, Anthropic Claude keys, Google API credentials, PostgreSQL/MySQL database connection URIs with embedded passwords, GitHub Personal Access Tokens (PATs), Slack webhooks, SendGrid tokens, and RSA/SSH private keys.
- **Shannon Entropy Engine:** Computes character-level information entropy to automatically catch unknown proprietary API keys and high-entropy secret hashes.
- **Smart Redaction Modes:** Mask secrets with partial clues (`sk_live_***890x`), explicit type tags (`[REDACTED_STRIPE_SECRET_KEY]`), or dummy placeholders (`your_stripe_secret_key_here`).
- **One-Click `.env.example` Generation:** Automatically comments and formats production-ready `.env.example` templates for your open-source repositories.
- **Client-Side AES-256 Vault:** Encrypt `.env` contents with PBKDF2 (100,000 iterations) + AES-GCM (256-bit) using standard WebCrypto APIs before sending them over insecure chat channels.
- **Pre-Commit Git Defense Hook:** Generates an instant bash hook for `.git/hooks/pre-commit` that aborts git commits whenever raw API keys are staged.

---

## 🛠️ Tech Stack
- **Engine:** Pure Vanilla TypeScript/JavaScript (Web Crypto API, File API, Blob API)
- **UI:** Tailwind CSS (Modern Dark Mode developer aesthetic)
- **Deployment:** Vercel Edge ($0 serverless infrastructure) & GitHub Pages
- **Cost:** $0 / month

---

## 💰 Monetization & Licensing
- **Community Edition:** 100% Free client-side scrubbing, 3 built-in presets, export redacted files, and export `.env.example`.
- **Pro Tier ($14 Lifetime):** Unlimited bulk files, CI/CD GitHub Action integration generator, Custom Enterprise Regex rules, and team vault decryptor links.

---

## 👤 Author
**Ayush Kandwal (@Sunzzx)**  
AI & Quant Researcher (Dual IIT Scholar)  
- Portfolio: [https://sunzzx.github.io/ayush-kandwal-portfolio/](https://sunzzx.github.io/ayush-kandwal-portfolio/)
- GitHub: [@Sunzzx](https://github.com/Sunzzx)
