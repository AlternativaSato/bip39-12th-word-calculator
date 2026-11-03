# Critical Security Warnings

*The Bitcoin Card Ritual — Alternativa Sato*

## 1. Purpose and Use Evaluation

This method and its associated tools were developed for **educational
purposes**. Their primary value lies in the learning process itself —
understanding how entropy is generated and how a BIP39 seed is
constructed.

If you decide to go further and use a seed generated this way for real
funds: **don't take our word for it — evaluate the security yourself.**
Audit the method and the tools, and if you have doubts, raise them with
the community before taking that step. That evaluation is your
responsibility, not an optional formality.

## 2. Inherent Risks of Web-Based Tools

Using any web-based tool (HTML/JavaScript), even one downloaded and run
locally, carries risk:

- **Keyloggers or malware** can capture your input.
- **Human error** — such as an accidental clipboard copy left behind —
  can compromise the seed.
- **The device itself** may already be compromised.

## 3. Secure Execution Protocol (Minimum Recommended)

If you decide to use the "Word 12" tool for anything beyond the
educational exercise, follow this protocol without exception:

- ✅ **Use a Live Operating System** (e.g. Tails, Ubuntu Live) booted
  from a USB drive that is new or fully wiped.
- ✅ **Disconnect all networking** — Wi-Fi, Ethernet, Bluetooth — before
  opening the file.
- ✅ **Use a private/incognito browser window.**
- ✅ **Never enter the words into any other software, browser, or text
  field.**
- ✅ **Power off the device** immediately after completing the exercise.

## 4. Network Isolation: The Non-Negotiable Requirement

This is the one rule here that isn't a matter of personal judgment,
because it doesn't depend on how much you trust the code: **a computer
connected to the internet can leak information without you noticing, no
matter how thoroughly audited the tool running on it is.**

> Never enter your seed words — not even the preliminary 11 words or the
> 7 color bits — on a computer that has been, is, or could be connected
> to the Internet.

Evaluate everything else on your own terms; don't negotiate on this one.

## 5. For Real Custody: Hardware Wallet

For real funds, the only safe path is a **certified, open-source
hardware wallet** (such as Trezor, Blockstream Jade, or Coldcard). These
devices apply the same cryptographic principles you just learned —
robust entropy, deterministic generation, verification — inside a
physically isolated, tamper-resistant environment. This educational
method gives you the knowledge to understand *why* those devices are
secure, not to replace them.

## 6. Responsibility and Community Verification

The creator of this method and its tools is not responsible for loss of
funds, theft, or security compromises resulting from the use of this
methodology or its associated tools. Sovereignty implies full personal
responsibility — and that responsibility starts with verifying before
trusting, not after.

---

A project by [Alternativa Sato](https://alternativasato.gitbook.io/alternativasato) · *Don't trust, verify.*
