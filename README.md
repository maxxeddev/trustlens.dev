# 🟦 TrustLens

> ⚠️ **Note:** This repository contains the public components of the TrustLens project.  
> The full source code, including certain backend modules and AI detection models, is available upon request for review, collaboration, or audit purposes.  
> Please [open an issue](https://github.com/trustlens/trustlens/issues) or contact the maintainer directly.

**Verify what’s real. Own what’s true.**  
TrustLens is a browser extension and backend platform for detecting synthetic content (like AI-generated media) and issuing **Verifiable Credentials (VCs)** on-chain to prove authenticity. Powered by decentralized identity, encrypted storage, and a pay-per-scan model.

![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)
![Built with TypeScript](https://img.shields.io/badge/code-TypeScript-blue)
![cheqd Verified](https://img.shields.io/badge/VCs-on--chain%20via%20cheqd-purple)
![Leap Wallet](https://img.shields.io/badge/payments-Leap%20Wallet-00ccff)

---

## 🌐 Live Links

- 🔎 **Demo**: [trustlens.dev](https://trustlens.dev)
- 🔐 **Extension**: Chrome dev build (coming soon)
- 🔗 **Blockchain**: [cheqd testnet](https://cheqd.io) 
- 🗄 **Private Storage**: [Verida](https://www.verida.io)

---

## 🚀 What It Does

- 🖼️ **Local Hashing**: Hash content (images, pages) directly in-browser
- 🧠 **Scan with AI**: Check for synthetic generation patterns
- 💸 **Pay-per-Scan**: Use $CHEQ or stablecoins via Leap Wallet
- 🧾 **Get a VC**: Issue a cryptographic Verifiable Credential via cheqd
- 🔐 **Private Report**: Store a detailed result in your personal Verida datastore

No tracking. No uploads without consent. No trust assumptions.

---

## 🧱 Architecture

<pre>
<code>
trustlens/
├── trustlens-extension/    # Browser extension (Chrome)
├── trustlens-server/       # API server for detection + credential issuance
├── packages/
│   ├── shared/             # Shared logic and types
│   └── shared-ui/          # Reusable UI components
├── ai-content-detector/    # Pluggable synthetic content detection models
└── docs/                   # Setup guides, roadmap, architecture
</code>
</pre>


---

## 🛠 Tech Stack

- **Frontend**: TypeScript, React, WebExtension APIs
- **Backend**: Node.js, Express, TypeScript
- **Blockchain**: cheqd (VC issuance + DID resolution)
- **Wallet**: Leap Wallet (testnet)
- **Storage**: Verida (encrypted private report storage)
- **AI**: Modular synthetic content detectors (dockerized)

---

## 🧪 Local Dev Setup

> Detailed instructions in [`docs/`](./docs/)

```bash
yarn install
yarn dev  # Starts extension and server in watch mode
```
🔧 Requires:
	•	Node.js ≥ 18
	•	Yarn (strictly)
	•	Chromium installed locally
	•	Leap Wallet (testnet account)
	•	cheqd testnet tokens (free faucet available)

---


🔐 Privacy & Security
	•	🔒 No user accounts — DID-based auth only
	•	✨ All hashing happens client-side
	•	📜 Public credential: W3C-compliant VC on cheqd
	•	🗃️ Private report: Encrypted via Verida
	•	🔁 All async flows use capped retries (retryWithLimit)

---


💬 Contributing

We welcome feedback, testing, and UI/UX suggestions.

Core detection models and credentialing infrastructure may remain partially closed-source to prevent abuse.

📢 Discussions

Join the conversation via GitHub Discussions or submit a feature request via Issues.

---


📄 License

MIT © TrustLens
This repository is open source, but may reference closed modules during runtime for AI models or secure VC issuance.
All third-party tools are used under their respective licenses.

---


👤 Maintainer

Built by Max, a solo engineer focused on privacy-first tools, decentralized identity, and ethical infrastructure.

“If we can’t trust what we see, let’s at least trust the chain that verified it.”

