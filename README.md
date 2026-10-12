# Global Reach — Consent-Based Discord Campaign Management & Community Outreach

**Global Reach** (Discord Application ID: `722756633499009045`) is a consent-based Discord campaign management and community announcement utility for server administrators. It helps Discord communities coordinate administrator-approved announcements to explicitly opted-in notification roles using the official Discord Bot API.

This repository hosts the **public website, installation and permission documentation, legal policies ([Terms of Service](./terms.html) and [Privacy Policy](./privacy.html)), contributor guidelines, and issue templates** for Global Reach.

> **Current Pre-Verification Status:** Global Reach (`722756633499009045`) is currently in **pre-verification preview** and is not yet deployed as an always-on hosted service. Core compliance, cryptographic consent verification, administrator campaign approval, channel permission evaluation, and data-removal capabilities are implemented and tested offline, while hosted cloud webhook listeners, interactive in-Discord opt-in buttons, and `/campaign` slash commands are scheduled for deployment following Discord verification.

---

## Core Compliance Principles

Discord server owners and community managers often need a structured, auditable way to publish sponsored or community announcements in designated `#announcements` channels without sending unsolicited Direct Messages (DMs) or spamming `@everyone`. Global Reach is built around four strict compliance principles:

1. **Official Bot Authentication Only:** Operates exclusively as a registered Discord Bot application via official OAuth2 permissions. Personal user-account automation ("self-botting") is strictly prohibited.
2. **Verified Individual User Consent:** Never treats an administrator-assigned Discord role as proof of individual consent; requires a signature-verified, user-initiated Discord interaction and enforces global opt-out precedence.
3. **Administrator Approval & Tamper Resistance:** Requires explicit approval from a verified server administrator bound to a cryptographic SHA-256 campaign digest, with single-dispatch locking to prevent duplicate announcement posts.
4. **Channel-Scoped Delivery Only:** Posts announcements strictly to authorized server text or announcement channels after verifying channel permission overrides.

---

## Capability Overview

| Capability | Current Status | Summary |
|---|---|---|
| **Official Bot Identity & OAuth2 Authorization** | **Available (Preview)** | Server administrators can review requested permissions and authorize the application (`722756633499009045`) in test or target servers. |
| **Cryptographic Interaction & Consent Verification** | **Implemented Core Capability** | Validates Ed25519 interaction signatures, prevents interaction replay, excludes bot accounts, and enforces persistent individual opt-in and opt-out rules. |
| **Channel Permission & Campaign Approval Engine** | **Implemented Core Capability** | Evaluates `@everyone`, role, and member-specific channel overrides (`View Channels`, `Send Messages`, `Embed Links`) and binds administrator approvals to SHA-256 campaign digests. |
| **Operator Privacy & Snapshot Cleanup Controls** | **Implemented Core Capability** | Supports permanent user opt-out recording, multi-store user data removal, and cleanup of expired temporary audience snapshots. |
| **Hosted Interaction Webhook & Gateway Listener** | **Planned (Post-Verification)** | Always-on cloud listener to receive live interactive events from Discord. |
| **In-Discord Opt-In Buttons & `/campaign` Slash Commands** | **Planned (Post-Verification)** | Interactive message components and slash commands inside Discord chat. |

---

## Documentation & Website Navigation

- **Public Website (GitHub Pages):** `https://punit-20.github.io/global-reach-public/`
- **Discord Bot OAuth2 Authorization (Preview):** `https://discord.com/oauth2/authorize?client_id=722756633499009045&permissions=274877910016&scope=bot%20applications.commands`
- **Landing Page:** [`index.html`](./index.html)
- **Documentation Hub:** [`docs/index.html`](./docs/index.html)
- **Installation & Permissions Guide:** [`docs/installation.html`](./docs/installation.html)
- **Product Features & Compliance Architecture:** [`docs/features.html`](./docs/features.html)
- **Frequently Asked Questions (FAQ):** [`docs/faq.html`](./docs/faq.html)
- **Terms of Service:** [`terms.html`](./terms.html)
- **Privacy Policy & Data Retention:** [`privacy.html`](./privacy.html)
- **Support & Troubleshooting:** [`support.html`](./support.html)

---

## Permissions & Privacy Summary

- **OAuth2 Scopes:** `bot`, `applications.commands`
- **Permission Integer (`274877910016`):**
  - `View Channels` (`1024`) — verify target announcement channel visibility and permission overrides.
  - `Send Messages` (`2048`) — post approved announcements in designated server channels.
  - `Embed Links` (`16384`) — render structured campaign embeds with clear sponsor attribution.
  - `Read Message History` (`65536`) — included in the default OAuth2 install integer for standard channel compatibility (Global Reach never reads or stores user chat messages).
  - `Use Application Commands` (`2147483648`) — reserved for planned slash-command registration.
- **Privileged Intent (`GUILD_MEMBERS`):** Required by Discord only when verifying that current non-bot holders of a server's configured notification role have active individual consent records.
- **Privacy & Deletion Boundaries:** See [`privacy.html`](./privacy.html) for complete details on processed Discord data categories, 7-day temporary snapshot retention, and user data deletion scope. Never post personal Discord User IDs, Server IDs, or tokens in public GitHub Issues.

---

## Contributing & Security Reporting

- **Contributing:** Read [`CONTRIBUTING.md`](./CONTRIBUTING.md) before opening pull requests for documentation, accessibility, or policy improvements.
- **Public Bug Reports & Feature Requests:** Use the [Bug Report](https://github.com/punit-20/global-reach-public/issues/new?template=bug_report.yml) or [Feature Request](https://github.com/punit-20/global-reach-public/issues/new?template=feature_request.yml) issue templates, or start a thread in [GitHub Discussions](https://github.com/punit-20/global-reach-public/discussions).
- **Private Security Vulnerability Reporting:** Do not report software vulnerabilities or exposed credentials in public issues. Follow [`SECURITY.md`](./SECURITY.md) to submit a private report via [GitHub Security Advisories](https://github.com/punit-20/global-reach-public/security/advisories/new).

---

## License

Released under the [MIT License](./LICENSE). Copyright (c) 2026 Global Reach Team (`punit-20`).
