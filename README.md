# The Bitcoin Card Ritual

> **"Forge your Bitcoin Seed with certainty and the entropy of your hands"**

*By Degú / Alternativa Sato*

---

## What is This Project?

This repository contains **The Bitcoin Card Ritual**, an educational and verifiable protocol to generate a Bitcoin mnemonic seed using only a common deck of 52 playing cards as an entropy source.

This method transforms a critical act for any bitcoiner into a tangible experience of **cryptographic sovereignty**. We call it a ritual because it's a repeatable and reproducible way to remember the elements of privacy and security that are intrinsic to the Bitcoin protocol.

### The Companion Tool

Included is the **Word 12 Calculator** (`12thWord_AlternativaSato.html`), a multi-language BIP39 calculator that:
- Verifies your entropy mathematically
- Calculates SHA256 hashes transparently
- Derives the 12th word of your mnemonic seed
- Demonstrates cryptographic principles visually

---

## Why Use a Deck?

Stories of lost Bitcoin are numerous and painful. Their root is usually not technical, but **human and cognitive**. The Ritual addresses three critical cognitive failures:

1. **Blind Trust** - We delegate to algorithms we don't understand
2. **Ephemeral Act** - A click generates a seed in milliseconds with no weight or meaning
3. **Cryptographic Ignorance** - We ignore the pillars of entropy and verification

Using a deck reverses this dynamic by serving as a **bridge between the physical-cultural world and the digital-mathematical world**, transforming abstract concepts into lived experience.

### Core Principles

1. **Memory Through Effort** - Humans remember experiences and narratives, not data
2. **Verification With Hands** - Shift trust from software to physics and mathematics
3. **True Entropy vs. Pseudorandom** - Create authentic physical entropy
4. **Discipline Over Product** - Security is not a device you buy, but a discipline you practice
5. **Symbolism And Technology** - Cards resonate deeply with Bitcoin fundamentals

---

## ⚠️ CRITICAL SECURITY WARNINGS

### Purpose and use evaluation
This method and its associated tools were developed for **educational purposes**. Their main value lies in the **learning process** of how entropy is generated and a BIP39 seed is built.

If you decide to go further and use a seed generated this way for real funds: **don't take our word for it — evaluate the security yourself**. Audit the method and the tools, and if you have doubts, raise them openly with the community in this repository (issues, pull requests, audits) before taking that step. That prior evaluation is your responsibility, not an optional formality.

### Inherent Risks of Web Tools
Using any web tool (HTML/JavaScript), even downloaded locally, carries risks:
- Keyloggers or malware may capture input
- Human error (like accidental copy to persistent clipboard) may compromise the seed
- The device itself may be compromised

### Secure execution protocol (minimum recommended)
If you decide to use the HTML tool for something beyond the educational exercise, follow this protocol without exceptions::
- ✅ Use a Live Operating System (e.g., Tails, Ubuntu Live) from a new or completely erased USB
- ✅ Disconnect ALL NETWORKS (Wi-Fi, Ethernet, Bluetooth) BEFORE opening the file
- ✅ Use private/incognito browsing window
- ✅ NEVER introduce the words into any other software or browser
- ✅ Shut down the device immediately after completing the exercise

### Network isolation: the non-negotiable requirement
This is the one rule in this document that isn't a matter of personal judgment, because it doesn't depend on how much you trust the code: **a computer connected to the internet can leak information without you noticing, no matter how thoroughly audited the tool you're running on it is**.

>Never enter your seed words (not even the preliminary 11 words or the 7 bits) on a computer that has been, is, or could be connected to the Internet.

Evaluate everything else on your own terms; don't negotiate on this one.

### For Real Custody: Hardware Wallet
For real funds, the only safe recommendation is a **certified, open-source hardware wallet**. These devices implement the same cryptographic principles in an isolated, verified, and robust way. This educational method gives you the knowledge to understand why those devices are secure — **not to replace them**.

### Responsibility and community verification
The creator of this method and its tools is **not responsible for loss of funds, theft, or security compromises** resulting from the use of this methodology or associated tools. Sovereignty implies full personal responsibility — and that responsibility starts with verifying before trusting, not after.

---

## Required Materials

### 1. Physical Source of Entropy
- Common (French) deck of 52 playing cards
- Function: Physical and verifiable entropy generator

### 2. The Cryptographic Dictionary
- BIP39 mnemonic word list (standard, in English)
- Function: Vocabulary of 2048 words that translates bits into memorable phrases

### 3. The Translation Table
- Table of values for playing cards (0-51)
- Function: Map each card to a unique number

### 4. The Cryptographic Verifier
- Web Tool "Word 12" (included in this repository)
- Function: Perform SHA256 calculations and verify the process

### 5. Pencil and Paper
- For recording your entropy and calculations

---

## What is a Mnemonic Seed?

A mnemonic seed is the master key to your Bitcoin ownership. It's the root from which billions of unique Bitcoin addresses can be deterministically generated.

### Why "Mnemonic"?
It's designed to be memorized by humans through three ingenious characteristics:

1. **Limited and optimal vocabulary** - 2048 words from the BIP39 standard
2. **Identification by prefix** - Any word can be uniquely identified by its first four letters
3. **Anti-confusion design** - Words were selected not to sound or look alike

### The 12-Word Structure
- **11 words** - Generated randomly using your deck (121 bits of entropy)
- **7 bits** - User-provided entropy (from card colors)
- **4 bits** - Checksum derived from SHA256 hash of the 128-bit entropy

Total: 132 bits of structured data encoding your cryptographic keys.

---

## The Process: Step by Step

### Step 1: Generate the First 11 Words

**Procedure for each word:**

1. Establish your numbering system (0-51) for the 52 cards
2. Thoroughly shuffle the complete deck
3. Take two topmost cards and note their values (e.g., 17 and 42)
4. Calculate: `(First_Card × 52) + Second_Card` → e.g., `17 × 52 + 42 = 926`
5. Evaluate:
   - If result < 2048 → This is your BIP39 index! Find the corresponding word
   - If result ≥ 2048 → Discard the pair and try the next two cards
6. Write down the new word
7. For the next word: Return to step 2 (shuffle the WHOLE deck again)

**Technical Notes:**
- The formula `(c1 × 52) + c2` allows us to map the 2,652 possible ordered card pairs to the 2,048 BIP39 words
- BIP39 allows word repetitions; each word is an independent 11-bit number
- There are ~643 out-of-range results; statistically requires ~7 shuffles per word

### Step 2: Generate the 7 Random Bits

What is a bit? A **bit** (binary digit) is the fundamental unit of information: either 0 or 1.

**The Ritual: Flipping a "Coin" of Two Colors**

Simple rule:
- ⚫ **BLACK Card** (Clubs ♣ or Spades ♠) → Bit **0**
- 🔴 **RED Card** (Diamonds ♦ or Hearts ♥) → Bit **1**

**Procedure:**
1. Shuffle the full deck thoroughly
2. Take 7 cards, one at a time, recording only their color
3. Write down the sequence of 7 bits in order: e.g., `1 0 1 1 0 0 0`
4. Verify you have exactly 7 binary digits

**Why is this secure?**
Card color in a well-shuffled deck has essentially 50/50 probability (26 black vs. 26 red). Seven independent decisions generate 2⁷ = 128 possible combinations, adding significant entropy to your seed.

### Step 3: Calculate Word 12 (The Cryptographic Seal)

All 12 words collectively encode a 132-bit sequence:
- **128 bits** - Original entropy (121 bits from your 11 words + 7 color bits)
- **4 bits** - Checksum, derived from applying SHA256 to those 128 bits

**Two Paths:**

**Path A: Using the Word 12 Tool (Recommended)**
1. Enter your 11 words and 7-bit sequence in the tool
2. The tool automatically:
   - Concatenates the 128-bit entropy
   - Calculates the SHA256 hash
   - Extracts the first 4 bits as checksum
   - Forms the final 11 bits (7 bits + 4-bit checksum)
   - Returns word 12

**Path B: Manual Verification (For Deep Learning)**
See the appendix in "The Bitcoin Card Ritual.txt" for step-by-step instructions on manual calculation.

---

## The Mathematics Behind Your Security

### Entropy Calculation
- **Source A (Cards)**: 11 pairs → ~125.16 bits of entropy
- **Source B (Color)**: 7 bits → 7 bits of entropy
- **Total Real Entropy**: ~132.16 bits

### Resistance to Attacks
| Metric | Minimum Standard (128 bits) | Alternative Sato Method (132.16 bits) |
|--------|-----|-----|
| Keyspace | 3.4 × 10³⁸ | 6.07 × 10³⁹ |
| Security Factor | 1x | ~18x more secure |

**Conclusion**: Our method not only meets the BIP39 standard but exceeds it, guaranteeing your seed is mathematically unattackable by conventional means.

### The Scale of 2¹²⁸

2¹²⁸ = 340,282,366,920,938,463,463,374,607,431,768,211,456

This is an unimaginably large number—more than grains of sand on Earth, more stars in the observable universe. For current computers, guessing your specific seed via brute force would take thousands of billions of times the age of the universe.

---

## Final Verification: Confirming Your Seed

After calculating word 12, verify your seed using the **Ian Coleman BIP39 Tool** (open-source industry standard):

### How to Verify (Secure Mode)

1. **Prepare secure environment**: Use offline computer or isolated virtual machine
2. **Access tool**: Download from GitHub and open locally (no internet connection)
3. **Enter your seed**: In the "BIP39 Mnemonic" field, enter your 12 words separated by spaces
4. **Observe validation**:
   - ✔ If the tool shows no errors and generates Bitcoin addresses → Your seed is valid
   - ✘ If error message appears → Something went wrong; review your steps

### What the Tool Verifies
1. Reconstructs the 132-bit sequence
2. Extracts the last 4 bits as checksum
3. Calculates SHA256 of the first 128 bits
4. Compares the first 4 bits of the hash with your checksum
5. If match → **Valid seed**; if not → **Invalid seed**

---

## Key Insights

> **"I was told and I forgot; I saw and I understood; I did and I learned."** — Confucius

This ritual teaches through experience what abstract cryptography can only explain in theory:

- You understand **entropy** by creating it physically
- You learn **hashing** by seeing it transform data
- You grasp **checksums** by verifying your own work
- You achieve **true sovereignty** by understanding every step

---

## Next Steps

After completing this ritual:

1. **Keep the knowledge** - More valuable than any individual seed
2. **Evaluate tools confidently** - Detect risks and understand security
3. **Use a hardware wallet for real funds** - Now you understand *why* they're secure
4. **Share the knowledge** - Help others transition to safe custody practices
5. **Explore more** - Visit [Alternativa Sato](https://alternativasato.gitbook.io/alternativasato) for additional resources

---

## License

**"The Bitcoin Card Ritual"** © 2025 Diego Salazar Arias / Alternativa Sato

Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International** (CC BY-NC-ND 4.0)

View license: https://creativecommons.org/licenses/by-nc-nd/4.0/

---

## About Alternativa Sato

Bitcoin Education Portal focused on helping bitcoiners understand the fundamental principles of cryptographic sovereignty, private key management, and secure custody.

**Core Belief**: Freedom isn't given. It's understood, verified, and custodied, one bit at a time.

🌐 **Website**: [Alternativa Sato](https://alternativasato.gitbook.io/alternativasato)

---

## Final Reflection

> **Bitcoin is sovereignty. Sovereignty is responsibility. Responsibility begins with comprehension.**

You have forged your own master key to financial freedom. Most importantly: **you know what it's made of**.
