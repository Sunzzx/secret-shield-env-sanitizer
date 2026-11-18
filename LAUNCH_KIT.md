# 🚀 Launch Kit: SecretShield

## 📌 One-Liner
Zero-knowledge client-side .env sanitizer and secret leak scrubber. Never paste AWS, Stripe, or OpenAI keys into ChatGPT, Claude, or GitHub again.

---

## 🌐 Assets
- **Live URL:** https://secret-shield-env-sanitizer.vercel.app
- **GitHub Repository:** https://github.com/Sunzzx/secret-shield-env-sanitizer
- **Monetization:** Free Client-Side -> $14 Lifetime Pro (Stripe Checkout)

---

## 💬 Show HN Copy
**Title:** Show HN: SecretShield – Zero-Knowledge Client-Side .env Sanitizer & Secret Vault

**Body:**
Hey HN,

A few weeks ago, a teammate accidentally pasted an unredacted `.env` into ChatGPT to debug a database connection issue. The prompt contained our production Stripe secret key and an AWS access token. Within hours, we were rotating credentials in a panic.

Almost every developer has done this at least once—either in LLM chats, Slack, or GitHub issues.

I built **SecretShield** to kill this problem permanently: https://secret-shield-env-sanitizer.vercel.app

What it does:
- **Zero Server Roundtrips:** It runs 100% locally in your browser. Absolutely zero data is sent over the wire or stored on any server.
- **Deep Detection Engine:** Scans for 40+ specific token types (Stripe, OpenAI, Anthropic, AWS, GitHub PATs, DB URIs with embedded passwords, RSA private keys) + Shannon entropy calculation for custom proprietary secrets.
- **Instant Outputs:**
  1. Redacted .env (safe to paste directly into ChatGPT/Claude)
  2. Production-ready `.env.example` with documented comments
  3. Client-side AES-256-GCM encrypted vault with password protection (using native WebCrypto)
  4. Git pre-commit hook script to prevent staging keys

It's completely free to use. Code is on GitHub: https://github.com/Sunzzx/secret-shield-env-sanitizer

Would love your thoughts, feedback, and edge cases to test!

---

## 💬 Reddit Copy (r/SideProject, r/webdev)
**Title:** I built an in-browser zero-knowledge tool to sanitize .env files before sharing with ChatGPT or Git

**Body:**
Hey everyone! Like many of you, I constantly use ChatGPT and Claude to debug backend code, but I was always paranoid about accidentally pasting `.env` variables with live AWS, Stripe, or Supabase credentials.

I built **SecretShield**: https://secret-shield-env-sanitizer.vercel.app

It's a client-side micro-utility that:
1. Detects 40+ production key formats and calculates Shannon entropy on high-entropy strings.
2. Replaces live keys with clean masks or type tags.
3. Automatically generates your `.env.example` template with 1 click.
4. Lets you encrypt `.env` files with AES-256-GCM right in the browser before sending them to coworkers.
5. Exports a `.git/hooks/pre-commit` script to block accidental commits.

Zero server infrastructure, zero data collection. Try it out and let me know what key formats you'd like added!
